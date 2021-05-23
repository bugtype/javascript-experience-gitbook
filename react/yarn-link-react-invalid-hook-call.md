# Yarn link 관련 에러 \( react invalid hook call\)



![](../.gitbook/assets/image.png)

자신이 만든 라이브러리와, 프로젝트의 React가 충돌이 나서 생기는 증상이다.



현재 자신이 만드는 모듈

```bash
yarn link
cd node_modules/react && yarn link
cd node_modules/react-dom && yarn link
```



현재 자신이 작업중인 프로젝트

```bash
yarn link your-module
yarn link react
yarn link react-dom

yarn # install
```

