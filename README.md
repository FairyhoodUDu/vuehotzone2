## Introduction

A vue2 hotzone component

## 基于开源项目[vue-hotzone](https://github.com/OrangeXC/vue-hotzone)二次开发
## Install

```bash
npm i vuehotzone2 --save
# or
yarn add vuehotzone2
```

## Use

```js
// Use in component
import hotzone from 'vuehotzone2'

export default {
  components: {
    hotzone
  }
}

// Use in global
import hotzone from 'vuehotzone2'

Vue.component(hotzone.name, hotzone)

// or
Vue.use(hotzone)
```

```html
<hotzone [options]></hotzone>
```

## Options

### Attributes
You can set them to your data function

| Attribute | Type   | Description                      | Keys                                       |
|:----------|:-------|:---------------------------------|:-------------------------------------------|
| image     | String | image of hotzone(required: true) |                                            |
| max       | Number | max number of zones              |                                            |
| zonesInit | Array  | init zones                       | item(heightPer, leftPer, topPer, widthPer) |

### Events

| Event Name | Description                                                              | Parameters                      |
|:-----------|:-------------------------------------------------------------------------|:--------------------------------|
| change     | triggers when the zones changes                                          | the array of the zones          |
| add        | triggers when the zone add                                               | the add zone item               |
| remove     | triggers when the zone remove                                            | the index of the remove zone    |
| overRange  | triggers when zones number > max                                         | the index of the overRange zone |
| erase      | triggers when add zone overRange or smaller than the minimum area(48*48) | the index of the erase zone     |



## License

vuehotzone2 is [Apache licensed](https://github.com/FairyhoodUDu/vuehotzone2/blob/master/LICENSE).
