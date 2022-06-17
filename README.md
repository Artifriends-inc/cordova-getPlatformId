# cordova-getPlatformId

Get platform id in cordova



[![NPM Version][npm-version-image]][npm-url]

[![NPM Install Size][npm-install-size-image]][npm-install-size-url]

[![NPM Downloads][npm-downloads-image]][npm-downloads-url]

```javascript
'use strict';

export class GetPlatformId {
    // browser, android, ios, electron
    static getId = () => {
        let result = '';

        // platform is browser
        if(location.href.substring(0, 4) === 'http'){
            // browser
            if(window.cordova === undefined) result = 'browser';
            // live reload
            else result = window.cordova.platformId;
        }
        // platform is cordova android or ios or electron
        else result = window.cordova.platformId;

        return result;
    }
}

console.log(GetPlatformId.getId()); // browser, ios, android, electron
```



## Installation

For typical cordova projects, copy and use the code above appropriately


How to install with Frontle

```shell
$ frontle install-original cordova-getplatformid
```



## People

The original author of frontle-modal is [MushStory](https://github.com/MushStory)



## License

[MIT](LICENSE)



[npm-downloads-image]: https://badgen.net/npm/dm/cordova-getplatformid
[npm-downloads-url]: https://npmcharts.com/compare/cordova-getplatformid?minimal=true
[npm-install-size-image]: https://badgen.net/packagephobia/install/cordova-getplatformid
[npm-install-size-url]: https://packagephobia.com/result?p=cordova-getplatformid
[npm-url]: https://npmjs.org/package/cordova-getplatformid
[npm-version-image]: https://badgen.net/npm/v/cordova-getplatformid
