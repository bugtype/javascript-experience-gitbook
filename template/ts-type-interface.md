# \[TS\] Type, Interface





```typescript
type NonEmptyArray<T> = [T, ...T[]];

type ObjectLiteral = {
  slice?: undefined; // array check용
  [key: string]: any;
};

type Without<T, U> = { [P in Exclude<keyof T, keyof U>]?: never };
type XOR<T, U> = (T | U) extends object ? (Without<T, U> & U) | (Without<U, T> & T) : T | U;


type Badge = XOR<{ rightOption?: 'none' | 'arrowIcon' }, { rightOption: 'badge'; badge: string }>;



```

