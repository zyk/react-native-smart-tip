# react-native-smart-tip
React-native smart tip, including Toast、Modal、SnackBar

![GitHub license](https://img.shields.io/badge/license-MIT-green.svg)
[![npm](https://img.shields.io/npm/v/react-native-smart-tip.svg?style=flat)](https://npmjs.com/package/react-native-smart-tip)

### 2019.7 Remove the method in the componentWillMount method. Compatible with future React 17 versions, React-Native@0.6 version.

### Installation
```bash
yarn add react-native-smart-tip
or
npm i react-native-smart-tip --save 
```

### Features
![](https://user-gold-cdn.xitu.io/2019/3/11/1696a8fc48b1fad3?w=240&h=427&f=png&s=20479)
![](https://user-gold-cdn.xitu.io/2019/3/11/1696a916aeec0d6a?w=240&h=427&f=png&s=25778)

![](https://user-gold-cdn.xitu.io/2019/8/29/16cdb4875aa8ae10?w=320&h=533&f=gif&s=1109140)
![](https://user-gold-cdn.xitu.io/2019/8/29/16cdb4bf900275de?w=300&h=500&f=gif&s=162107)
![](https://user-gold-cdn.xitu.io/2019/8/29/16cdb4c3641f5870?w=300&h=500&f=gif&s=176895)

### Usage

##### WToast
```
import {WToast} from 'react-native-smart-tip'

// Base 
show = () => {
	WToast.show({data: 'hello world'})
}

// Other
show = () => {
	const toastOpts = {
	    data: 'Success',
	    textColor: '#ffffff',
	    backgroundColor: '#444444',
	    duration: WToast.duration.LONG, //1.SHORT 2.LONG
	    position: WToast.position.TOP, // 1.TOP 2.CENTER 3.BOTTOM
	    icon: <Image source={require('../data/img/success.png')} style={{width: 32,height: 32,resizeMode: 'contain'}}/>
	}
	
	WToast.show(toastOpts)
}

```
##### WToast API
 Props |	Type	  | Required	 | Default    | Description
-------| -------- | -------- | ----------- | -----------
data     | String  | true     | ' '| Displayed content
duration | Number | false | WToast.duration.SHORT | The duration of the toast
position | Number   | false  | WToast.position.BOTTOM | Displayed position
inEasing | Easing   | false  | Easing.elastic(1)| Admission animation
textColor| String | false |'white'| font color
backgroundColor| String | false | 'black' | background color
icon | Component | fasse | undefined | Image to be displayed

---

##### WSnackBar
```
import {WSnackBar} from 'react-native-smart-tip'

// Base 
show = () => {
	WSnackBar.show({data: 'hello world'})
}

// Other
show = () => {
	const snackBarOpts = {
	    data: 'Please check the network first.',
	    position: WSnackBar.position.BOTTOM, // 1.TOP 2.CENTER 3.BOTTOM
	    duration: WSnackBar.duration.LONG, //1.SHORT 2.LONG 3.INDEFINITE
	    textColor: '#ff490b',
	    backgroundColor: '#050405',
	    actionText: 'Sure',
	    actionTextColor: '#ff490b',
	    actionClick: ()=>{
	    	// Click Action
	    },
	}
	
	WSnackBar.show(snackBarOpts)
}

```

##### WSnackBar API
 Props |	Type	  | Required	 | Default    | Description
-------| -------- | -------- | ----------- | -----------
data     | String  | true     | ' '| Displayed content
statusBarHeight | Number | false | -1 | Prevent Android statusBar
height | Number | false | 44 | Height to display
duration | Number | false | WSnackBar.duration.SHORT | The duration of the toast
position | Number   | false  | WSnackBar.position.BOTTOM | Displayed position
inEasing | Easing   | false  | Easing.linear| Admission animation
textColor| String | false |'white'| font color
backgroundColor| String | false | 'black' | background color
actionText | String | false | undefined | action text
actionTextColor | String | false | 'white' | action text color
actionClick | Function | false |  undefined | listener click

---

##### WModal 
```
import {WModal} from 'react-native-smart-tip'

// Base 
show = () => {
	WModal.show({data: 'hello world'})
}

// Other
show = () => {
	const modalOpts = {
	    data: 'Loading',
	    textColor: '#fff',
	    backgroundColor: '#444444',
	    position: WModal.position.CENTER,
	    icon: <ActivityIndicator color='#fff' size={'large'}/>
	}
	
	WModal.show(modalOpts)
}

```
##### WToast API
 Props |	Type	  | Required	 | Default    | Description
-------| -------- | -------- | ----------- | -----------
data     | String  | true     | ' '| Displayed content
position | Number   | false  | WToast.position.BOTTOM | Displayed position
inEasing | Easing   | false  | Easing.elastic(1)| Admission animation
textColor| String | false |'white'| font color
backgroundColor| String | false | 'black' | background color
icon | Component | fasse | undefined | Image to be displayed
onRequestClose|Function|false| undefined| Android Back

##### MIT Licensed
