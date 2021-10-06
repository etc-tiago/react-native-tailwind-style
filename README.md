# React Native Tailwind Style

A compositor of tailwind for React Native Styles

## How to use

Import `react-native-tailwind-style` module and use any of the [supported utilities](#supported-utilities) from [Tailwind CSS](https://tailwindcss.com) in your [React Native](https://reactnative.dev) views.

### Configure

1. Install the package: `npm i react-native-tailwind-style -D` or `yarn add react-native-tailwind-style -D`

2. Add tailwind.config.js on root folder

3. Add the script on package.json

```json
{
	"scripts": {
		"build-tailwind": "./node_modules/.bin/rnts"
	}
}
```

3. Execute `yarn build-tailwind` now and every time that tailwind.config.js change.

### Use on React Native

```js
import React from "react";
import { SafeAreaView, View, Text } from "react-native";
import tailwind from "react-native-tailwind-style";

const App = () => (
	<SafeAreaView style={tailwind("h-full")}>
		<View style={tailwind("pt-12 items-center")}>
			<View style={tailwind("bg-blue-200 px-3 py-1 rounded-full")}>
				<Text style={tailwind("text-blue-800 font-semibold")}>
					Hello Tailwind
				</Text>
			</View>
		</View>
	</SafeAreaView>
);

export default App;
```
