Use `Animation` in a different context

```ts
type EmojiAction = SingleChar | ComposedChar;

function runEmoji(tr: EmojiAction) {
  switch(tr.type) {
    case "singleChar": return tr.char;
    case "composedChar": return tr.charA.char + tr.charB.char;
  }
}

let emojiRuntime = function (action: Animation<EmojiAction>) {
  function loop(t: Time) {
    location.hash = runEmoji(action.fn(t));
    requestAnimationFrame(loop);
  }
  requestAnimationFrame(loop);
};
```
the idea is taken from [here](https://matthewrayfield.com/articles/animating-urls-with-javascript-and-emojis/)