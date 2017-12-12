# react-native-vector-icons-slds
Icon and color definitions for Salesforce Lightning Design System Icons for use with `react-native-vector-icons`

Compatible with Winter ’18 (SLDS 2.4.6) release.

## Installation

```shell
$ yarn add react-native-vector-icons-slds
```

Follow the instructions [here](https://github.com/oblador/react-native-vector-icons#installation) to add `react-native-vector-icons` and the font to your platform.

If you are using Expo, follow the instructions [here](https://docs.expo.io/versions/latest/guides/using-custom-fonts.html) to add the font. `react-native-vector-icons` is already included with Expo.

## Usage

Import one or more of the json files, and use them with `createIconSet`. 

```ts
import { createIconSet } from 'react-native-vector-icons'

const glyphMap_action = require('node_modules/react-native-vector-icons-slds/SLDS-action.json')
const glyphMap_custom = require('node_modules/react-native-vector-icons-slds/SLDS-custom.json')
const glyphMap_standard = require('node_modules/react-native-vector-icons-slds/SLDS-standard.json')
const glyphMap_utility = require('node_modules/react-native-vector-icons-slds/SLDS-utility.json')

const Icon = createIconSet({
  ...glyphMap_action, 
  ...glyphMap_custom, 
  ...glyphMap_standard, 
  ...glyphMap_utility
}, 'SalesforceDesignSystemIcons')
```

Now, you can use the icons:

```jsx
<Icon name='action_add_contact' size={24} color='#000'>
```

You can find an Expo Snack with a demo of all the icons here: https://snack.expo.io/@agartha/react-native-icons-slds-demo

## Colors

This library also contains the standard icon background colors from the Lightning Design System. This Expo Snack contains an example of how to use them: https://snack.expo.io/@agartha/slds-icon-colors-demo