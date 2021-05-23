# Svgr 스크립트



1. svg 파일을 컴포넌트로 만드는 스크립트
2. 만든 컴포넌트 파일을 index에서 export 해준다.



```text
#!bin/bash

# Anchor by bugtytpe(이재현)

iconPath='./src/components/icons/'

echo -e "\033[1;33m svgr을 이용하여 svg -> tsx로 변환중... 🏃‍🏃‍🏃‍ "
npx @svgr/cli@5.5.0 --typescript --memo --icon --replace-attr-values '#626262=currentColor' $iconPath/svg/*.svg --out-dir $iconPath/
echo "\033[1;32m ${iconPath}index.ts 파일 만드는 중... "
ls $iconPath | grep tsx | sed 's/\.[^.]*$//' | sed 's/.*/export { default as & } from ".\/&";/' | sed "s/\"/'/g" > $iconPath/index.ts
echo "\033[34m 작업완료 😄"
```

