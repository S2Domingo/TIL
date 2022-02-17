# :__dirname is not defined in ES module scope.md

## Error
__dirname is not defined in ES module scope
---

## 해결한 방법


ES 모듈 파일에서 __dirname 글로벌 변수를 사용하려고 할 때 발생한다. `__dirname`이나 `__filename` 같은 글로벌 변수는 ECMAScript module files에서 사용할 수 없다.

```javascript
import path from 'path';
import {fileURLToPath} from 'url';

const __filename = fileURLToPath(import.meta.url);
const __dirname = path.dirname(__filename);

console.log('directory-name', __dirname);
console.log(path.join(__dirname, '/dist', 'index.html'));
```

`dirname()` 메서드를 `path` 모듈에서 가져와 사용한다. `dirname` 메서드는 `path`를 parameter로 사용하고, path의 디렉토리 이름을 리턴한다. 

filename을 받아오려면, `url` 모듈의 `fileURLToPath()` 메서드를 사용한다. `fileURLToPath` 메서드는 the fully-resolved platform-specific Node.js file path를 리턴한다. 이 메서드가 취하는 유일한 파라미터는 path로 전환되어야 하는 file URL string이다.

---


[Source](https://bobbyhadz.com/blog/javascript-dirname-is-not-defined-in-es-module-scope)