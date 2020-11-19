<h1>
    <s>Universal</s> Unibiased Coding Style
</h1>



## About

Universal is striked out due to the presumptuousness that any kind of universality pertains. Unibiased, then, is meant to mean inclined under a single, general direction.

The `Unibiased Coding Style` (`UCS`) acknowledges the diversity and difference between language, however it is intended at the same time to reduce the cognitive load over the polylinguist.

Nothing wrong in a language being written in a certain style, separating itself from the rest of the flock, however the `UCS` will imply certain assumptions even there.

As a general rule, the `UCS` has:

```
if a change is meant in a single place then it should be adequately reflected in the history control
```



## Example

The simplest example is parameter naming in a function's definition. Consider

``` typescript
function adder(A, b) {
    return A + b;
}
```

Let's suppose a rename of the conventionally misnamed parameter `A` into the correct form `a`.

``` typescript
> function adder(a, b) {
    return a + b;
}
```

The file history control will show the whole line as changed, whereas in fact it is only one character affected.

Therefore, the `UCS` proposes as a general shape each parameter on it's own line

``` typescript
function adder(
    a,
    b,
) {
    return a + b;
}
```

The renaming now is properly marked for only the affected line/character(s).

When calling a function, the arguments will be passed each on its own line

``` typescript
adder(
    5,
    7,
);
```
