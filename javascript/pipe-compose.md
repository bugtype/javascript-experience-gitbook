# pipe, compose





```typescript
const pipe = <A, B>(fn: (a: A) => B) => {
    return {
        f: function<C>(g: (x: B) => C) { return pipe((arg: A) => g(fn(arg)))},
        build: () => fn
    }
}

const compose = <A, B>(fn: (a: A) => B) => {
    return {
        f: function<C>(g: (x: C) => A) { return compose((arg: C) => fn(g(arg)))},
        build: () => fn
    }
}


const add = (x: number) => (y: number) => x + y
const multiply = (x: number) => (y: number) => x * y
const format = (n: number) => `value: ${n.toString()}`
const upper = (s: string) => s.toUpperCase()

const process = pipe(add(2))
  .f(multiply(3))
  .f(format)
  .f(upper)
  .build() // (6+2)*3


const process2 = compose(upper)
  .f(format)
  .f(add(2))
  .f(multiply(3))
  .build() // (6*3)+2

console.log(process(6)) // VALUE: 24
console.log(process2(6))// VALUE: 20
```

