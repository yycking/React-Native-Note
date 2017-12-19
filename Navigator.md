# Navigator

* `import { Navigator } from 'react-native'`

* `renderScene`={(`route`, `navigator`) => {return \<View />}}

  * `route`

    頁面的資訊

  * `navigator`

    * `.push`
    * `.pop`

* `configureScene`={(`route`, `routeStack`) => { return Navigator.SceneConfigs.***}}

  * `route`
  * `routeStack`
    * Navigator.SceneConfigs.PushFromRight (default)
    * Navigator.SceneConfigs.FloatFromRight
    * Navigator.SceneConfigs.FloatFromLeft
    * Navigator.SceneConfigs.FloatFromBottom
    * Navigator.SceneConfigs.FloatFromBottomAndroid
    * Navigator.SceneConfigs.FadeAndroid
    * Navigator.SceneConfigs.SwipeFromLeft
    * Navigator.SceneConfigs.HorizontalSwipeJump
    * Navigator.SceneConfigs.HorizontalSwipeJumpFromRight
    * Navigator.SceneConfigs.HorizontalSwipeJumpFromLeft
    * Navigator.SceneConfigs.VerticalUpSwipeJump
    * Navigator.SceneConfigs.VerticalDownSwipeJump

* `navigationBar`={\<Navigator.NavigationBar routeMapper={} />}

  * Title: (route, navigator, index, navState) =>\<Text>title\</Text>
  * LeftButton: (route, navigator, index, navState) =>\<Text>title\</Text>
  * RightButton: (route, navigator, index, navState) =>\<Text>title\</Text>



# Router

* 非官方

* `import {Scene, Router} from 'react-native-router-flux';`

* ```javascript
  class App extends React.Component {
    render() {
      return <Router>
        <Scene key="root">
          <Scene key="home" component={Home} title="home" />
        </Scene>
      </Router>
    }
  }
  ```

* ```Actions.home({ desc: 'Hello React Native' })```

* ```Actions.home()```

  ​



# 