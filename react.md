# JSX

* `TEXT` -> `<TEXT/>`

* ```javascript
  function Article() {
    return React.createElement(
      "div",
      { className: "article" },
      React.createElement(
        "h1",
        { className: "article-title" },
        "Title"
      )
    );
  }
  ```
  -> 
  ```javascript
  function Article() { 
    return (
      <div className="article">
        <h1 className="article-title">Title</h1>
      </div>
    );
  }
  ```

* prop

  * normal

    className=`{styles.button}`

  * function

    onClick=`{() => console.log('clicked!')}`

  * inline

    style=`{{ fontSize: 20, textAlign: 'center', margin: 10 }}`

  * mix

    style=`{[ styles.welcome, { color: 'red' } ]}`


# Commponent

* 寫法，依新到舊

  * Functional

    ```javascript
    const App = () => <div />;
    ```

  * ES6 Class

    ```javascript
    class App extends React.Component {
      render() {
        return <div />;
      }
    }
    ```

  * classic

    ```javascript
    const App = React.createClass({
      render() {
        return <div />;
      },
    });
    ```




# State

```javascript
class Counter extends React.Component {
  state = {
    count: 0,
  };
  handleClick = () => {
    this.setState({
      count: this.state.count + 1,
    });
  };
  render() {
    return (
      <div>
        {this.state.count}
        <button 
          onClick={this.handleClick}
        >+1</button>
      </div>
    );
  }
}
```



