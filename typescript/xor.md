# XOR 타입



```text


type TestType = { name: string; age: number;} | { name?: never; age?: never; country: string;  } ;

const test2 : TestType = {
    name: "bug",
    age: 10,
}

const test3 : TestType = {
    country: 'korea;'
}
```



```text
type Without<T, U> = { [P in Exclude<keyof T, keyof U>]?: never };
type XOR<T, U> = (T | U) extends object ? (Without<T, U> & U) | (Without<U, T> & T) : T | U;
```

* [https://stackoverflow.com/questions/44425344/typescript-interface-with-xor-barstring-xor-cannumber](https://stackoverflow.com/questions/44425344/typescript-interface-with-xor-barstring-xor-cannumber)

