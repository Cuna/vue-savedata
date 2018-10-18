## Requirements

* [Vue.js](https://vuejs.org) (v2.0.0+)
* [Vuex](http://vuex.vuejs.org) (v2.0.0+)

## Installation

```bash
$ npm install vuex-savedata
```

## Usage


```js
import createPersist from 'vuex-savedata'

const store = new Vuex.Store({
  // ...
  plugins: [createPersistedState()],
})
```
## API

### `createPersistedState([options])`

Creates a new instance of the plugin with the given options. The following options
can be provided to configure the plugin for your specific needs:

* `saveName <String>`: 本地save的key  默认： savedata
* `SS <Object>`: {storePath: xx, module: xx } storePath  在store 上的路径   module     需要 本地存的 模块
* `SL <Object>`: {storePath: xx, module: xx }  同上
* `getState <Function>`:  取本地时调用的方法  可自定义（SS,SL也会调用此方法）
* `setState <Function>`:  存本地时调用的方法  同上

## License

[MIT](https://github.com/robinvdvleuten/vuex-persistedstate/blob/master/LICENSE) © [Robin van der Vleuten](https://www.robinvdvleuten.nl)