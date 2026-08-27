- Técnica utilizada para dificultar a compreensão do código por seres humanos, mas permitindo que ele ainda funcione.

# Casos de Uso

- Desenvolvedores que desejam ocultar funcionalidades.
- Atacantes que ofuscam seu código para bypassar WAFs, IDS, IPS e etc.

# Minification

- Ter o código JS inteiramente em uma linha

```javascript
function log(){
console.log("jorge");
}
```

```javascript
function log(){console.log("jorge")}
```

- https://www.toptal.com/developers/javascript-minifier

# Packing

- Converte todas as palavras e símbolos em uma lista ou dicionário e consulta usando (p,a,c,k,e,d)

```javascript
console.log("jorge")
```

```javascript
eval(function(p,a,c,k,e,d){e=function(c){return c};if(!''.replace(/^/,String)){while(c--){d[c]=k[c]||c}k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1};while(c--){if(k[c]){p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c])}}return p}('0.1("2")',3,3,'console|log|jorge'.split('|'),0,{}))
```

- O packaging, pode ser reconhecido pelo (p,a,c,k,e,d) no começo

https://beautifytools.com/javascript-obfuscator.php

# Advanced

- Remove o clear text do código ofuscado

```javascript
console.log("jorge")
```

![[Pasted image 20260116224529.png]]

```javascript
function _0x5a6b(_0x55e5c1,_0x3a48bb){_0x55e5c1=_0x55e5c1-0xa7;var _0x29633d=_0x2963();var _0x5a6bf2=_0x29633d[_0x55e5c1];if(_0x5a6b['jrQnVh']===undefined){var _0x20a23c=function(_0x3a2bac){var _0x14992b='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';var _0xf1128a='',_0xd8b836='';for(var _0x1ea4f1=0x0,_0x4cf797,_0xcd869a,_0x3c3ce5=0x0;_0xcd869a=_0x3a2bac['charAt'](_0x3c3ce5++);~_0xcd869a&&(_0x4cf797=_0x1ea4f1%0x4?_0x4cf797*0x40+_0xcd869a:_0xcd869a,_0x1ea4f1++%0x4)?_0xf1128a+=String['fromCharCode'](0xff&_0x4cf797>>(-0x2*_0x1ea4f1&0x6)):0x0){_0xcd869a=_0x14992b['indexOf'](_0xcd869a);}for(var _0xe87633=0x0,_0x2b03d0=_0xf1128a['length'];_0xe87633<_0x2b03d0;_0xe87633++){_0xd8b836+='%'+('00'+_0xf1128a['charCodeAt'](_0xe87633)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0xd8b836);};_0x5a6b['JbOkjZ']=_0x20a23c,_0x5a6b['WCzYnh']={},_0x5a6b['jrQnVh']=!![];}var _0x20fae7=_0x29633d[0x0],_0x30e977=_0x55e5c1+_0x20fae7,_0x5d7ec7=_0x5a6b['WCzYnh'][_0x30e977];return!_0x5d7ec7?(_0x5a6bf2=_0x5a6b['JbOkjZ'](_0x5a6bf2),_0x5a6b['WCzYnh'][_0x30e977]=_0x5a6bf2):_0x5a6bf2=_0x5d7ec7,_0x5a6bf2;}var _0x3da643=_0x5a6b;(function(_0x4d2d30,_0x192474){var _0x2710b1=_0x5a6b,_0x2798bb=_0x4d2d30();while(!![]){try{var _0x1504ab=-parseInt(_0x2710b1(0xac))/0x1+-parseInt(_0x2710b1(0xad))/0x2+parseInt(_0x2710b1(0xa9))/0x3*(parseInt(_0x2710b1(0xaa))/0x4)+-parseInt(_0x2710b1(0xa8))/0x5*(parseInt(_0x2710b1(0xb4))/0x6)+-parseInt(_0x2710b1(0xab))/0x7*(-parseInt(_0x2710b1(0xaf))/0x8)+-parseInt(_0x2710b1(0xa7))/0x9*(parseInt(_0x2710b1(0xb2))/0xa)+-parseInt(_0x2710b1(0xae))/0xb*(-parseInt(_0x2710b1(0xb1))/0xc);if(_0x1504ab===_0x192474)break;else _0x2798bb['push'](_0x2798bb['shift']());}catch(_0xb34888){_0x2798bb['push'](_0x2798bb['shift']());}}}(_0x2963,0x3b1c2),console[_0x3da643(0xb3)](_0x3da643(0xb0)));function _0x2963(){var _0x200ddd=['mte4otqYmhnxvezbsa','nZK4BKnQq1nT','mZq2nZyYDMDktgTg','mZq2mJaYueTnvM5f','mtfys2HtuKu','odK0nfv2AvnNyq','AM9Yz2u','mtiZmZm2otzwtwXgvNa','mJGZmeT3tfrJAq','Bg9N','ntCZodrqALjJEgO','mta3mtbysuT0veu','mtG1uMDOrg96','m1vOtMXkua'];_0x2963=function(){return _0x200ddd;};return _0x2963();}
```

https://obfuscator.io/legacy-playground
