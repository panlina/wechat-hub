# Quick Start
### 0. Apply Token
You need PadLocal token to run this demo. [How to Apply Token](https://github.com/padlocal/wechaty-puppet-padlocal/wiki/How-to-Apply-Token)

### 1. Prepare Node Environment
[Install Node](https://nodejs.org/), 12/14 LTS version is recommended.
```
$ node --version // >= v12.0.0
``` 
### 2. Clone the [wechat-hub](https://github.com/panlina/wechat-hub) project.

```
$ git clone git@github.com:panlina/wechat-hub.git
```
Then install Node dependencies.
```
$ cd wechat-hub
$ npm install
``` 

### 3. Set you PadLocal Token in `main.ts`
```ts
const puppet = new PuppetPadlocal({
    token: "YOUR_PADLOCAL_TOKEN"
})
```

### 4. Add plugins in `plugins.ts`
```ts
import { DingDong, EventLogger } from 'wechaty-plugin-contrib'
export = [
    DingDong(),
    EventLogger(['login', 'ready', 'message'])
];
```
You may need `npm install` additional packages where your plugins are.

Then run it:
```
$ npm start
```
![carbon](https://user-images.githubusercontent.com/64943823/117439626-a6cde080-af65-11eb-85a5-815aa422b5c5.png)
