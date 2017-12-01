# View

* `import { View } from 'react-native';`

* UIView

* android.view

* `style={{ width: 50, height: 50 }}`

* ```javascript
  <View style={{ flex: 1 }}>
    <View style={{ flex: 1}} />
    <View style={{ flex: 2}} />
  </View>
  ```

  ┍┑
  ┝┥
  ││
  ┕┙

* ```javascript
  export default class HelloReactNative extends Component {
    render() {
      return (
        <View />
      );
    }
  }
  ```

  ->

  ```javascript
  export default (props) => (
    <View />
  );
  ```

  ​



# Text

* `import { Text } from 'react-native';`
* Text內，可頰Text
  * NSAttributedString
  * SpannableString




# Image

* `import { Image } from 'react-native';`

* `<Image source={require('./check.png')} />`

* ```javascript
  <Image 
    source={{
      uri: 'https://facebook.github.io/react/img/logo_og.png',
    }}
    style={{ width: 400, height: 400 }} 
  />
  ```

  * 針對網路上的圖片，必須在 `Image` 上面先指定好長寬

* resizeMode

  * cover
    * 保持寬高比的縮放圖片，直到寬度和高度都大於等於容器
  * contain
    * 保持寬高比的縮放圖片，直到寬度和高度都小於等於容器
  * stretch
    * 拉伸且不維持寬高比，直到寬高都填滿容器
  * repeat
    * 重複平鋪
  * center
    * 居中




# Touchables*

* `import { TouchableOpacity } from 'react-native';`

* UIView

* TouchableHighlight

  * 被 Touch 之後會有一個 Highlight 的效果，而 Highlight 的顏色可以透過 `underlayColor` 改變。

  * ```javascript
    <TouchableHighlight
      onPress={() => {}}
      underlayColor="red"
    >
      <View style={styles.btn}>
        <Text style={styles.text}>按鈕</Text>
      </View>
    </TouchableHighlight>
    ```

* TouchableOpacity

  * 被 Touch 之後會有一個透明度改變的效果




# Button

* `import { Button } from 'react-native';`

* UIButton

* ```javascript
  <Button
    onPress={function(){ console.log('按到我了') }}
    title="Learn More"
    color="#841584" 
  />
  ```




# ScrollView



# ListView

* `import { ListView } from react-native;`

* dataSource: ListView.DataSource

* renderRow:

* rowHasChanged:

* ```javascript
  class ListViewBasics extends Component {
    // Initialize the hardcoded data
    constructor(props) {
      super(props);
      const ds = new ListView.DataSource({
        rowHasChanged: (r1, r2) => r1 !== r2,
      });
      this.state = {
        dataSource: ds.cloneWithRows([
          '帶給各位！',
          '滿滿的！',
          '大平台！'
        ])
      };
    }
    render() {
      return (
        <View style={{ flex: 1, paddingTop: 22 }}>
          <ListView
            dataSource={this.state.dataSource}
            renderRow={(rowData) => <Text>{rowData}</Text>}
          />
        </View>
      );
    }
  }
  ```




# TextInput

* `import { TextInput } form react-native;`

  * ```javascript
    <TextInput
    onChangeText={(text) => this.setState({text})}
    value={this.state.text}
    />
    ```

* `import { Keyboard } from 'react-native';`

  * ```javascript
    <TouchableWithoutFeedback onPress={Keyboard.dismiss}>
      <View>
        <View />
        <TextInput
          onSubmitEditing={Keyboard.dismiss}
        />
      </View>
    </TouchableWithoutFeedback>
    ```

  * `EventEmitter`

    * Keyboard.addListener(eventName, callback)
    * Keyboard.removeListener(eventName, callback)

  * eventName

    * keyboardWillShow
    * keyboardDidShow
    * keyboardWillHide
    * keyboardDidHide
    * keyboardWillChangeFrame
    * keyboardDidChangeFrame




# 跨平臺

* 後輟
  * .ios.js
  * .android.js
  * `import Sample from './src/Sample';`

* 平臺判斷 `Platform.OS === 'ios'`

* ```javascript
  var styles = F8StyleSheet.create({
    container: {
      ios: {
        paddingBottom: 6,
      },
      android: {
        paddingLeft: 60,
      },
    },
  };
  ```

  ​

  ​

