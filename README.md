# JavaScript
## Array
#### 加入元素
```javascript
var array = [];
array.push('newElement');
```
#### 包含某元素
```javascript
array.includes('newElement');
```
:warning: IE 瀏覽器不支援 ```includes()``` 方法
#### 元素索引
```javascript
array.indexOf('newElement');
```
#### 刪除特定元素
```javascript
array.splice(array.indexOf(value), 1);
```

## Map
```javascript
var map = new Map()
map.set(key, value);
map.forEach(function(value, key) {
  console.log(key + '-' + value);
});
```
:warning: IE10 及以下不支援 ```Map``` 對象

## Date
#### 取得目前時間
```javascript
var date = new Date();
var now = date.getTime();
```
#### 時間比較
```javascript
if (now.valueOf() > Date.parse(end).valueOf())
  console.log('late');
else
  console.log('early');
```

## Browser
#### 判斷是否為 IE 瀏覽器
```javascript
function isIE() {
  return (navigator.appName == 'Microsoft Internet Explorer') ||     // IE 10 以下
        (new RegExp('Trident/.*rv:([0-9]{1,}[\.0-9]{0,})').exec(navigator.userAgent) != null);    // IE 11
}
```
#### IE 瀏覽器版本
```javascript
function IEVersion() {
  return parseInt(navigator.appVersion.split(';')[1].replace(/[ ]/g, '').replace('MSIE', ''));
}
```

## HTML elements
#### 取得 element
```javascript
var element = document.getElementById('Id');
var element = document.getElementsByClassName('ClassName');    // 回傳 array
```
#### 屬性值
```javascript
element.getAttribute('attribute');
element.setAttribute('attr', 'value');
element.className += ' newClass';    // 加入新的 class
```
#### 加入 HTML
```javascript
element.innerHTML = 'html';
```
#### CSS
```javascript
element.style
```
