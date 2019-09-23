I do this:
```js
let imageEl = document.getElementById('doomfaces') 
let canvasElement = document.getElementById('canvasId');
let context = canvas.getContext('2d');
context.globalCompositeOperation = 'multiply';
context.imageSmoothingEnabled = false;
let sprites = Object.values(spriteData);
function loop() {
  context.clearRect(0,0, canvas.width, canvas.height);
  context.save();
  context.translate(100 * Math.sin(Math.PI * 2 * t / 6000), 0);
  let d = sprites[Math.ceil(t / 600) % sprites.length];
  context.drawImage(imageEl, 
    d.sx, d.sy, d.sw, d.sh, 0, 0, d.dw, d.dh);
  context.restore();
  requestAnimationFrame(loop);  
}
requestAnimationFrame(loop); 
```