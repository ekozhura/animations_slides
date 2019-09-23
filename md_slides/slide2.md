### Start the design with data types 

```ts
type GraphicAction = 
    EmptyAction
  | Move 
  | Scale 
  | DrawImage 
  | ComposeAction;
```

keywords: `algebraic data type`, `discriminated union`, `variant type`
