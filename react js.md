## Examples 
* https://github.com/facebook/react/wiki/examples
* https://github.com/mzabriskie/react-example
* https://react.rocks/
* https://github.com/reasonml-community/reason-react-example
* https://github.com/reactjs/redux/tree/master/examples
* react-webrtc : https://github.com/roman01la/react-webrtc
* web rtc : https://github.com/srtucker22/glipchat
* webrtc : https://react.rocks/tag/WebRTC
* webrtc file share : https://react.rocks/example/filepizza
* redux tutorial (good) : http://www.thegreatcodeadventure.com/react-redux-tutorial-part-vi-the-edit-feature/
* updating with single object : https://forum.freecodecamp.org/t/reactjs-using-setstate-to-update-a-single-property-on-an-object/146772


## Tips 
* change size of element simply : https://github.com/Semantic-Org/Semantic-UI-React/issues/2435


## Example
* redux example : https://medium.com/@rajaraodv/step-by-step-guide-to-building-react-redux-apps-using-mocks-48ca0f47f9a
* simple things : https://camjackson.net/post/9-things-every-reactjs-beginner-should-know
* sample example : https://tylermcginnis.com/reactjs-tutorial-a-comprehensive-guide-to-building-apps-with-react/
* https://ihatetomatoes.net/react-tutorial-for-beginners/

## Material
* React JS : https://blog.andrewray.me/reactjs-for-stupid-people/
* Flux : https://blog.andrewray.me/flux-for-stupid-people/
* semantic ui react : https://react.semantic-ui.com/introduction


## mine
* simple es6 review 
  * http://alexband.tistory.com/37
* use redux!
* possible component pattern 
```
const MyComponent = React.createClass({
  render: function() {
    return <div className={this.props.className}/>;
  }
});
```

```
class MyComponent extends React.Component {
  render() {
    return <div className={this.props.className}/>;
  }
}
```

```
const MyComponent = props => (
  <div className={props.className}/>
);
```

```
const Todo = ({ onClick, completed, text }) => (
  <li
    onClick={onClick}
    style={{
      textDecoration: completed ? 'line-through' : 'none'
    }}
  >
    {text}
  </li>
)
```


* container for reduct and component for independent to redux 
   * https://github.com/reactjs/redux/tree/master/examples/todos
   * https://www.zerocho.com/category/React/post/57e1428c11a9b10015e803aa
