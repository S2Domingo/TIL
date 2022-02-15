# 'babel-node' is not recognized as an internal or external command, operable program or batch file.

### Error
'babel-node' is not recognized as an internal or external command, operable program or batch file.

---

### 해결한 방법

1. 
`npm uninstall @babel/cli`
기존에 설치한 @babel/cli -D를 지운다. (개발에 사용할 모듈 devDependencies에만 나타나게 설치한 것)

2. 
`npm install -g babel-cli` 
글로벌 패키지로 다시 설치해준다.