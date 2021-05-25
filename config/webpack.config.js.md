# webpack.config.js

웹팩은 기본적으로 여러 개의 자바스크립트 모듈을 하나의 파일로 묶어내는 번들러입니다.

웹팩은 이 `Entry` 속성에 명시된 파일을 기준으로 **의존성 트리**를 만들어 **하나의 번들 파일**을 만들어 내게 됩니다. `Entry` 설정의 기본값은 `./src/index.js`이고, 예제 프로젝트에서는 이를 간단하게 `./script.js`로 변경해보도록 하겠습니다.

```javascript
// 기존 번들파일을 지우고 싶을 때
const CleanWebpackPlugin = require("clean-webpack-plugin");

module.exports = {
  entry: "./script.js",
  output: {
    path: __dirname,
    filename: "build.js",
  },
  module: {
    rules: [
      {
        test: /\.css$/,
        // 웹팩은 자바스크립트 뿐만 아니라, Loader를 이용하여 CSS나 이미지, 웹폰트, JSX, VUE 등 다양한 종류의 파일을 함께 번들링할 수 있습니다. 
        use: ["style-loader", "css-loader"],
      },
    ],
  },
  plugins: [new CleanWebpackPlugin("build.js")],
};
```



참고

* [https://www.daleseo.com/webpack-config/](https://www.daleseo.com/webpack-config/)
* 
