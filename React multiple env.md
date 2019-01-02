## react-create-app으로 생성한 프로젝트를 여러개의 설정으로 관리하기 (development/production으로 충분치 않아서)

```
set "REACT_APP_ENV=abcdef" && npm start      // window
REACT_APP_ENV=abcdef npm start               // others

```
* 참고: https://facebook.github.io/create-react-app/docs/adding-custom-environment-variables

* package.json
```
    "start": "react-scripts start",
    "build": "react-scripts build",
    "build:prod": "set \"REACT_APP_ENV=production\" && react-scripts build",
    "build:prod-mac": "REACT_APP_ENV=production react-scripts build",
```
