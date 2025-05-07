# 🚀 rn-animated-header-api

A customizable animated header component for React Native that hides as you scroll, with support for background images, titles, back buttons, and custom FlatList content.

## ✨ Features

- Animated hide/show header on scroll
- Customizable header title and background
- Supports remote or local images
- Pass any FlatList data and render logic
- Reusable and easy to integrate

---

## 📦 Installation

```bash
npm install rn-animated-header-api


# | Prop            | Type       | Description                                                | Required | Default          |
# | --------------- | ---------- | ---------------------------------------------------------- | -------- | ---------------- |
# | `imageSource`   | `object`   | Image source for the background (`require()` or `{ uri }`) | ✅        | `undefined`      |
# | `headerTitle`   | `string`   | Title shown in the header                                  | ❌        | `"Header Title"` |
# | `onBackPress`   | `function` | Callback when back button is pressed                       | ❌        | `() => {}`       |
# | `data`          | `array`    | Data array for `FlatList`                                  | ✅        | `[]`             |
# | `renderItem`    | `function` | Render function for list items                             | ✅        | `undefined`      |
# | `flatListProps` | `object`   | Additional props passed to FlatList                        | ❌        | `{}`             |


# import React from 'react';
# import { Text, View } from 'react-native';
# import AnimatedHeader from 'react-native-animated-header';

# const App = () => {
#   const data = Array.from({ length: 20 }, (_, i) => `Item ${i + 1}`);

#   return (
#     <AnimatedHeader
#       imageSource={{ uri: 'https://picsum.photos/400/200' }}
#       headerTitle="My Header"
#       onBackPress={() => alert('Back button pressed')}
#       data={data}
#       renderItem={({ item }) => (
#         <View style={{ padding: 20, borderBottomWidth: 1, borderColor: '#ddd' }}>
#           <Text>{item}</Text>
#         </View>
#       )}
#       flatListProps={{
#         ListFooterComponent: () => <Text style={{ textAlign: 'center', padding: 10 }}>~ End of List ~</Text>,
#       }}
#     />
#   );
# };

# export default App;
