```jsx
/*react*/
<script>
  export default class Application extends React.Component {
    constructor(props) {
      super(props)
      this.state = {
        color: 'blue'
      }
      this.globalVariable = globalVariable
    }
    render() {
      return (
        <div>
          <div className='wrapper' ref={el => this.el = el}>
            <label className="test-label">
                <input className='test-input' />
                <p className="test">author: {this.globalVariable}</p>
                <button style={{color: this.state.color}} className='test-button' onClick={e => {alert('author: ' + this.globalVariable); this.setState({color: 'red'})}}>test</button>
            </label>
          </div>
        </div>
      )
    }
  }
</script>
```

open the browser console, run the following js:
```js
document.querySelector('.test-button').click()
```
The button is clicked, just same as manully click


run the following js:
```js
document.querySelector('.test-input').click()
```

```js
document.querySelector('.test-input').focus()
```
The input can not be focused, why these happens? How to explain?
