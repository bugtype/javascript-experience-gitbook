# declare global\(env\)



```typescript
declare global {
  namespace NodeJS {
    interface ProcessEnv {
      ENVIRONMENT: 'development' | 'production' | 'test';
      BASE_API: string;
      BASE_V2_API: string;
    }
  }
}

// If this file has no import/export statements (i.e. is a script)
// convert it into a module by adding an empty export statement.
export {};

```



