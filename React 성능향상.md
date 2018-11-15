## 핵심은 불필요한 render() 줄이기
* 라이브러리로 확인 https://github.com/maicki/why-did-you-update

아래와 같이 코드에 적용하면 알아서 불필요하게 render되는  찾아줌
```
import React from 'react';

if (process.env.NODE_ENV !== 'production') {
  const {whyDidYouUpdate} = require('why-did-you-update');
  whyDidYouUpdate(React);
}
```
* 혹은 프로파일러도 사용

## 방법
### React.PureComponent 사용 
* https://reactjs.org/docs/react-api.html#reactpurecomponent
* React.Component대신 쓰면 알아서 props state에 대해서 shallow check 해줌
* shallow compare로 충분할 경우에 쓸만함

### shouldComponentUpdate 사용
* 가장 최후의 수단으로 써야할 녀석 (매뉴얼하게 render를 직접 관리)
```
shouldComponentUpdate(nextProps) {
        return (nextProps.ids !== this.props.ids
             || nextProps.data !== this.props.data);
    }
```

### Component구성
* 컴포넌트를 잘 자른다.
* 필요한 컴포넌트만 render될수 있도록

### recompose 혹은 hook 활용 (잘활용하면 state나 props 변경이 덜되게 사용 가능) 
* reompose는 더이상 개발 안될듯 : https://github.com/acdlite/recompose
* hook : https://reactjs.org/docs/hooks-overview.html


### Redux를 잘 사용하기 
* 필요한 props만 잘 추가하기 
* 혹은 reselect 사용하기 : https://github.com/reduxjs/reselect



## 참조
* https://marmelab.com/blog/2017/02/06/react-is-slow-react-is-fast.html
* https://www.robinwieruch.de/react-prevent-rerender-component/
