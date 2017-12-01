# AsyncStorage

- `getItem(key, (err, result) => {})`

  - ```javascript
    getStorage = async () => {
      try {
        const value = await AsyncStorage.getItem('@Route:initialPage');
      } catch (error) {
        console.log(error);
      }
    }
    this.getStorage().done();
    ```

- `setItem(key, value, (err, result) => {}))`

  - ```javascript
    setStorage = async () => {
      try {
        await AsyncStorage.setItem('@Route:initialPage', 'login');
      } catch (error) {
        console.log(error);
      }
    }
    this.setStorage().done();
    ```

- `removeItem(key, (err, result) => {}))`



#Realm

*  非官方

  ​