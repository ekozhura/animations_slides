### What I really wanted

```ts
Animation
  .of('doomface', spriteData)
  .moveX(t => 100 * Math.sin(Math.PI * 2 * t / 6000))
  .scale(1.5)
  .speed(0.5)
  .run();
```

<p class="fragment">spoiler alert: the result won't be like this at the end</p>
<p class="fragment">...but close</p>