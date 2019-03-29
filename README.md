<p align="center">
<img src="https://pigjian.com/images/v-distpicker.png" alt="Powered By Jiajian Chan" width="160">
</p>

<p align="center">A flexible, highly available district selector for picking provinces, cities and districts of China.</p>

<p align="center">
  <br>
  <b>创造不息，交付不止</b>
  <br>
  <a href="https://www.yousails.com">
    <img src="https://yousails.com/banners/brand.png" width=350>
  </a>
</p>

# V - Distpicker

Here is [documents](http://distpicker.pigjian.com/)

## Installation

```javascript
npm install v-distpicker --save
```

Or

```javascript
yarn add v-distpicker --save
```

## Usage

**Register component**

Registe global component:

```javascript
import Distpicker from 'v-distpicker'

Vue.component('v-distpicker', Distpicker)
```

Registe component:

```javascript
import VDistpicker from 'v-distpicker'

export default {
  components: { VDistpicker }
}
```

**How to use**

Basic:

```javascript
<v-distpicker></v-distpicker>
```

Default Value:

```javascript
<v-distpicker province="广东省" city="广州市" area="海珠区"></v-distpicker>
```
Placeholders:

```javascript
<template>
  <v-distpicker :placeholders="placeholders"></v-distpicker>
<template>

<script>
import VDistpicker from 'v-distpicker'

export default {
  components: { VDistpicker },
  data() {
      return {
          placeholders: {
              province: '------- 省 --------',
              city: '--- 市 ---',
              area: '--- 区 ---',
          }
      }
  }
}
</script>
```

Hide Area:

```javascript
<v-distpicker hide-area></v-distpicker>
```

only-province:

```javascript
<v-distpicker only-province></v-distpicker>
```

Placeholders:

```javascript

```

Placeholders:

```javascript

```

Mobile:

```javascript
<v-distpicker type="mobile"></v-distpicker>
```
Attributes:

参数|说明|类型|可选值|默认值
---|:--:|---:|:--:|---:
province|	省份（选填）|	String|	省份名|	null
city|	城市（选填）|	String|	城市名|	null
area|	地区（选填）|	String|	地区名|	null
type|	类型（选填，默认 select）|	String|	mobile|	null
disabled|	是否禁用（选填，默认 false，且 type='mobile' 时无效）|	Boolean|	true, false|	false
hide-area|	隐藏地区（选填）|	Boolean	true, false	false
onlu-province|	只显示省份（选填）|	Boolean|	true, false|	false
static-placeholder|	是否将占位符显示为已经选择的项（仅 type='mobile' 时有效）|	Boolean|	true, false|	false
placeholders|	占位符（选填）|	Object|	province, city, area|	{ province: '省', city: '市', area: '区' }
wrapper|	外层 Class（选填）|	String|	customize|	address
address-header|	address-header 样式（选填，类型必须为 mobile）|	String|	customize|	address-header
address-container|	address-container 样式（选填，类型必须为 mobile）|String|	customize|	address-contaniner

Methods：

方法|说明|参数
---|:--:|---:
province|	选择省份|	返回省份的值
city|	选择城市|	返回城市的值
city|	选择地区|	返回地区的值
selected|	选择最后一项时触发|	返回省市区的值

## Contributors

- [Jiajian Chan](http://github.com/jcc)

## Thanks

- [Distpicker](https://github.com/fengyuanchen/distpicker)

## License

The plugin is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
