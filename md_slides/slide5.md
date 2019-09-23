### Runtime

```ts
function runGraphic(ctx, action: GraphicAction): void {
  switch(action.type) {
    case "empty": break;
    // ... handle 'scale' and 'move'
    case "drawImage": 
      const { sprite } = action;
      ctx.drawImage(action.imageEl, ...sprite); break;
    case "compose": 
      runGraphic(ctx, action.actionA);
      runGraphic(ctx, action.actionB);
      break;
  }
}

runGraphic(ctx, ourGraphicScript);
```