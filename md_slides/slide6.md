### Animations

Each `GraphicAction` represents a single action. 

Animation can be thought as a series of such actions that runs over some time.

```ts
interface Animation<T> {
  type: "animation";
  fn(time: Time): T; 
}
```
`Animation` is a function from time `t` to values of type `T`.