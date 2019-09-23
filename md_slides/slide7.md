### Runtime
No need to modify runtime, just extend it with new function `runAnimation`

```ts
function runAnimation(animation: Animation<GraphicAction>) {
  function loop(t) {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    ctx.save();

    runGraphic(ctx, animation.fn(t));
    
    ctx.restore();
    requestAnimationFrame(loop);
  }
  requestAnimationFrame(loop);
}
```