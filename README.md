# React Native

Project to use Camera - mobile. Front camera and back camera


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



## Components

- ` <Image>` Render a image
- ` <Modal>` Component modal
- ` <View>` Just to show something in the screen
- ` <TouchableOpacity>` Create a button with effect after clicking it

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
    <Text style={styles.textTitle}>myCameraApp</Text>
  </View>
```
