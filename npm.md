package.jsonが存在するプロジェクトにおいて、```npm install```を行うと、```node_modules```が作成される。

例

package.json

```
{
  "name": "npm-cli-sample",
  "version": "0.1.0",
  "private": true,
  "dependencies": {
    "typescript": ">=3.2.1 <4.0.0 || >=4.0.0 <5.0.0"
  },
  "scripts": {
    "start": ""
  }
}
```

このようなpackage.jsonが存在する状況で、```npm install```を実行すると、node_modulesディレクトリが作成され、その中に、package.jsonに記載されていたライブラリ？が作成されている。

<img width="298" alt="スクリーンショット 2024-06-18 21 08 31" src="https://github.com/Ryo-0912/React/assets/82032550/bf44d32c-c4c6-40ba-902c-d0b78ddb3e46">

ちなみに、```npm install jquery```などとパッケージを指定すると、packge.jsonやnode_modulesの中身も更新される。

```
{
  "name": "npm-cli-sample",
  "version": "0.1.0",
  "private": true,
  "dependencies": {
    "jquery": "^3.7.1",
    "typescript": ">=3.2.1 <4.0.0 || >=4.0.0 <5.0.0"
  },
  "scripts": {
    "start": ""
  }

}
```


jqueryディレクトリができている！！

<img width="297" alt="スクリーンショット 2024-06-18 21 10 42" src="https://github.com/Ryo-0912/React/assets/82032550/6cc10a45-9e37-4882-96fb-443f7cc52412">



