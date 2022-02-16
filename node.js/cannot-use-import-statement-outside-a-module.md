# Cannot use import statement outside a module

### Error 

(node:14580) Warning: To load an ES module, set "type": "module" in the package.json or use the .mjs extension.
(Use `node --trace-warnings ...` to show where the warning was created)
C:\Users\jgim7\Documents\Zoom\src\server.js:1
import express from "express";
^^^^^^

SyntaxError: Cannot use import statement outside a module
    at Object.compileFunction (node:vm:352:18)
    at wrapSafe (node:internal/modules/cjs/loader:1032:15)
    at Module._compile (node:internal/modules/cjs/loader:1067:27)


`"type": "module",`을 package.json 맨 윗줄에 추가한다.

---

package.json의 "type" 필드에 아무 값이 없거나 "commonjs"로 설정되어있을 경우, 모듈 처리 방식이 require을 사용하는 commonjs 방식으로 설정되기 때문에 에러가 발생함.

`"type": "module"` 을 추가해주면 require로 불러오둔 모듈을 import를 사용하는 방식으로 변경된다.