Instead define only a couple of higher-order functions:

```ts
function lift0<A>(a: A): Animation<A> {
  return { 
    fn: (t: Time) => a,
    type: "animation"
  };
}

function lift1<A, B>(f: (x: A) => B, a: Animation<A>): Animation<B> {
  return {
    fn: (t: Time) => f(a.fn(t)),
    type: "animation"
  };
};
// also for a -> b -> c, a -> b -> c -> d, etc.
```
