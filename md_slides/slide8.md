### Constructing animations

```ts
// implement from scratch:
function scaleA(
  x: Animation<number>): Animation<Scale> {
  return {
    type: "animation";
    fn: (time: Time) => scale(x.fn(t))); 
  };
}
// or lift existing functions to type Animation:
const always = lift0;
const scaleA = lift1(scale);

// the usage is the same:
scaleA(always(20));
```
