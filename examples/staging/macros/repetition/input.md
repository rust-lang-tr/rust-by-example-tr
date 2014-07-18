Macros can also match and return repeated patterns. This is similar but
different from a regex. `$($x:expr),+` is a matching example. It uses the
`$()` grouping operator to mark `x` as repeatable. `+` or `*` denotes
repetition amount; one or more and zero or more respectively. `,`
is the only separator token available.

```rust
// The separator only checks separation; this is
// not a regex.
$($x:expr),+ // matches `1, 2, 3` but not `1, 2,`
```

When returned, it uses a similar notation: `$($x:expr),+` => `$($x),+`
however, a returned list will not be re-expanded whereas, matching
will find the whole thing.

```rust
#![feature(macro_rules)]

macro_rules! echo_broken {
    // Attempt to match and return with one compact expression
    ($($x:expr),+) => { $($x),+ };
}

macro_rules! echo_works {
    ($x:expr) => { $x }; // one element list
    // $x is the first element. `$($y:expr),+` is the tail
    ($x:expr, $($y:expr),+) => {
        // pass the tail to `echo_works` so it can be expanded
        ($x, echo_works!($($y),+))
    };
}

fn main() {
    println!("{}", echo_broken!(1u)); // Works for single elements

    // Errors: `,` ignored. A list is never re-expanded so when
    // the `,` is reached, the rest of the line is ignored.
    // Rust does not allow incomplete expansion, so it errors. To
    // handle this, recursion is needed.
    //println!("{}", echo_broken!(1u, 2u));

    println!("{}", echo_works!(1u));
    // Would like it flat but it nests the results...
    println!("{}", echo_works!(1u, 2u, 3u, 4u, 5u, 6u));
}
```

Another example making a min macro:
{repeat.play}
