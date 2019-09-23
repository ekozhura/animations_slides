```js
function moveSomething(ctx, x, y) {
  ctx.translate(x, y);
}
function drawImage(ctx, el, ...coords) {
  ctx.drawImage(el, ...coords);
}
function clearCanvas(ctx, w, h) {
  ctx.clearRect(w, h);
}
```
<p class="fragment">
  <img src="assets/functional.jpg"/>
</p>