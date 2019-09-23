### Improvements

Organize under the class `AnimationLibrary`

```ts
const animation = AnimationLibrary
  .of(startAt(0, 0))
  .chain(
    moveA(varied(periodicFn), always(0))
  )
  .chain(scaleA(1.5))
  .chain(renderSprites);

runAnimation(animation);
```