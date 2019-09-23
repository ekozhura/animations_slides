### Usage

```ts
let startAt = 
  (x: number, y: number) => moveA(always(x), always(y));

let moveAndScale = andThenA(
  moveA(varied(periodicFn), always(0)),
  scaleA(1.5)
);

const animation = andThenA(
  startAt(0, 0), 
  andThenA(
    moveAndScale,
    renderSprites
  )
);

runAnimation(animation);
```