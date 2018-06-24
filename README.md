# Vuetify.js confirm dialog

This module extends vuetify confirm dialog.

## Setup

Install the package from npm

```npm
npm install vuetify-confirm
```

```javascript
import VuetifyConfirm from 'vuetify-confirm'
Vue.use(VuetifyConfirm)
```
Install with options or any of them:

```javascript
import VuetifyConfirm from 'vuetify-confirm'
Vue.use(VuetifyConfirm, {
  buttonTrueText: 'Delete',
  buttonFalseText: 'Cancel',
  buttonTrueColor: 'warning',
  buttonFalseColor: 'black',
  headerColor: 'warning',
  headerIcon: 'warning',
  headerTitle: 'Warning',
  width: 300,
  property: '$confirm'
})
```

property: '$confirm' will create property with this name in Vue prototype

## Usage

```js
this.$confirm('Do you really want to exit?').then(res => {
})
```

```js
let res = await this.$confirm('Do you really want to exit?', {title: 'Warning'})
if (res) {
  ...
}
```
*res* will be true or false

You can format your message with arbitrary HTML - make sure you don't include any user-provided content here:

```js
this.$confirm('Please do not do this.<br>Do you really want to exit?').then(res => {
})
```
