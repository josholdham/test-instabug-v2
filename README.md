# test-instabug-v2

- npx react-native init testInstabugV2
- cd testInstabugV2
- yarn add instabug-reactnative
- react-native add-instabug
- cd ios
- pod install
- cd ../ 

**In App.js**

I added the following 

`import Instabug, { BugReporting, Surveys, FeatureRequests } from 'instabug-reactnative’;`

```
useEffect(() => {
  Instabug.startWithToken('95293e32354f2b336952fda40d70c138', [
    Instabug.invocationEvent.none,
  ]);
}, []);
```

```
<TouchableOpacity
  onPress={() => {
    Instabug.show();
  }}>
  <Text>Test Instabug</Text>
</TouchableOpacity>
```
