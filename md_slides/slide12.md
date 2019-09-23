<section>

Use `Animation` in a different context

```ts
type EmojiAction = SingleChar | ComposedChar;
...
let emojiRuntime = function (action: Animation<EmojiAction>) {
  function loop(t: Time) {
    location.hash = runEmoji(action.fn(t));
    requestAnimationFrame(loop);
  }
  requestAnimationFrame(loop);
};
```
the idea is taken from [here](https://matthewrayfield.com/articles/animating-urls-with-javascript-and-emojis/)
</section>
<section>
<img src="assets/emoji.gif" />

```ts
const moonEmoji = timeTrans<SingleChar>(
  slowDown(5),
  drawEmojiA(moon.map(setChar).reverse())
);
const clockEmoji = drawEmojiA(
  clock.map(setChar).reverse()
),

emojiRuntime(
  composeCharsA(moonEmoji, clockEmoji)
);
```
</section>