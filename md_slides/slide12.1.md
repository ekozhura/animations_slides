<img src="assets/emoji.gif" />

```ts
const moonEmoji = timeTrans(
  slowDown(5),
  drawEmojiA(
    moon.map(setChar).reverse()
  )
);

const clockEmoji = drawEmojiA(
  clock.map(setChar).reverse()
);

emojiRuntime(
  composeCharsA(moonEmoji, clockEmoji)
);
```