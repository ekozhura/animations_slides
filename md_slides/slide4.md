Define functions that construct values of `GraphicAction` type:

```ts
function moveXY(x: number, y: number): Move {

  return { type: "move", x, y };

}
...
function andThen(
  actionA: GraphicAction, actionB: GraphicAction
): ComposeAction {

  return { type: "compose", actionA, actionB };

}
...
```