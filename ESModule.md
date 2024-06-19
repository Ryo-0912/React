# Moduleのimport,export

- export

  ```
  export const hello = () => {
    console.log("hello!");
  };
  
  const funcB = () => {
    console.log("funcB output");
  };
  
  export default funcB;
  
  class User {
    constructor(name) {
      this.name = name;
    }

    hello() {
      console.log(this.name);
    }
  }
  
  export { User }
  ```


  
- import

  ```
  import { hello } from "./module.js";
  import { User } from "./module.js";
  
  //同じファイルからimportしているので、まとめられる
  import { hello, User } from "./module.js";
  
  // デフォルトエクスポート呼び出す際、名前を変更できる(デフォルトエクスポートは各ファイルに一つしかないため)
  import functionB from "./module.js";
  
  
  hello();
  
  const user = new User('Tom');
  user.hello();
  
  functionB();
  ```

# デフォルトエクスポート

各jsファイル内で一度だけ使える。

```
export default funcB;

```
