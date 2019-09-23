### Lifting `GraphicAction` API

```ts
const varied = <T>(fn: (t: Time) => T): Animation<T> 
  => ({ fn, type: "animation" });
const always = lift0;

const scaleA = lift1(scale);
const moveA = lift2(move);
const andThenA = lift2(andThen);
```
