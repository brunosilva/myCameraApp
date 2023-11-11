# React Native

Project to use Camera - mobile


## Create a new project

```js
  yarn create expo-app myCameraApp
```


## Start the project

```js
  yarn add expo expo-camera
  yarn add expo expo-contacts
  yarn add expo expo-sensors
```



## App screenshot
https://github.com/brunosilva/health/issues/1#issue-1977908691
https://github.com/brunosilva/health/issues/2#issue-1977909401
https://github.com/brunosilva/health/issues/3#issue-1977909562



## Components

- ` <Text>` Render a new text
- ` <TextInput>` Create a new field to input information
- ` <View>` Just to show something in the screen
- ` <TouchableOpacity>` Create a button with effect after clicking it
- ` <FlatList>` Render just data in view
  ```js
    // data: array of data (reverse to render descending order)
    // renderItem: create formatted text to display
    // keyExtractor: unique key of list item
    <FlatList
      style={style.listImc}
      data={imcList.reverse()}
      renderItem={({item}) => {
        return (
          <Text style={style.resultImcItem}>
            <Text style={style.textResultItemList}>Resultado IMC: </Text>
            {item.imc}
          </Text>
        )
      }}
      keyExtractor={(item) => {item.id}}
    />
  ```




## API's

- ` Vibration` actived vibration when call it ` Vibration.vibrate()`
- ` Share` share with ex.: Whatsapp
  ```js
    const onShare = async () => {
      const result = await Share.share({
        message: `Meu imc hoje é: ${props.resultImc}`
      })
    }
  ```
- ` Pressable` is possible clickable and with an other api ` keyboard` you can hide the keyboard
  ```js
    <Pressable onPress={Keyboard.dismiss} ...>
      ...
    </Pressable>
  ```


## StyleSheet

Define the new file stylesheet with Css-in-Js, name like ` style.js` and the code here always have be camelCase pattern syntax.
```js
import { StyleSheet } from 'react-native';

const styles = StyleSheet.create({
  boxTitle: {
    alignItems: "center",
    justifyContent: "center",
    padding: 10,
  },
  textTitle: {
    color: "#FF0043",
    fontSize: 24,
    fontWeight: "bold",
  }
});

export default styles
```

After, import on your `index.js`.
```js
  import styles from "./style";

  ...

  <View style={styles.boxTitle}>
    <Text style={styles.textTitle}>Health 2.0</Text>
  </View>
```
