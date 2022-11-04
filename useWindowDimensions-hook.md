## useWindowDimensions Hook
***

**useWindowDimensions** is a react-native hook that we can get the devices **width**, **height**, **scale** and **font scale** values.

It **automatically**  updates width and height value when device screen changes.

```JS
const { height, width, scale, fontScale } = useWindowDimensions();
```
useWindowDimensions hook returns an object that includes height, width, scale, fontScale values on it. We can destructure it like on above code snippet.

### Example
```JS
import React from 'react';
import {View, StyleSheet, Text, useWindowDimensions} from 'react-native';

const App = () => {
  // We create an object using useWindowDimensions hook
  const window = useWindowDimensions();
  return (
    <View style={styles.container}>
      {/* Then we can get the height, width, scale and fontScale values */}
      <Text>{`
      Height: ${window.height}
      width: ${window.width}
      font scale: ${window.fontScale} 
      scale: ${window.scale}
`}</Text>
    </View>
  );
};
const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
  },
});

export default App;
```

