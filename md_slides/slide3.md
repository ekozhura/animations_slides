Something similar to this:
```js
...
ctx.translate(20, 20);
ctx.scale(2, 2);
ctx.drawImage(imageElement);
...
```

with data types can be expressed as:
```ts
ComposeAction(
  DrawImage(imgId),
  ComposeAction(
    Move(20, 20),
    Scale(2)
  )
)
```