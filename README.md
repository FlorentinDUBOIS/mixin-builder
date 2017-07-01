# mixin-builder [![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg?style=flat-square)](https://www.webcomponents.org/element/FlorentinDUBOIS/mixin-builder) [![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

A simple mixin builder created to works well as a web components.

## Installation

As it is usually to use bower and soon yarn to install web components. Just add to your bower install the `mixin-builder` dependency, as follow:

```bash
$ bower install --save mixin-builder
```

## Usage

To access it, simply use the html import standart to include it in your web component or page.

```html
<link rel="import" src="bower_components/mixin-builder/mixin-builder.html" />
```

To use it, simply give your mother class to the `MixinBuilder` function and Mixin(s) to herit to the `with` method, as follow:

```JavaScript
/**
 * A basic mixin
 * @param  {class} pSuperClass the super class
 * @return {class}             the child one
 */
function myMixin(pSuperClass) {
  return class extends pSuperClass {
    // your stuff here
  }
}

/**
 * A second basic mixin
 * @param  {class} pSuperClass the super class
 * @return {class}             the child one
 */
function mySecondMixin(pSuperClass) {
  return class extends pSuperClass {
    // your stuff here
  }
}

/**
 * A casual class or not ;P
 * @type {class}
 */
class MyPowerClass {}

/**
 * My new casual class or not with access to myMixin's
 * and mySecondMixin's attributes and methods
 * @type {class}
 */
const MyPowerClassWithMixin = MixinBuilder(MyPowerClass).with(myMixin, mySecondMixin)
```

## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

MIT License

Copyright (c) 2017 Florentin DUBOIS

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
