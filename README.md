angularjs-toaster-fontawesome
=================

**angularjs-toaster-fontawesome** is an AngularJS port of the **toastr** non-blocking notification jQuery library. It requires AngularJS v1.2.6 or higher, angular-animate for the CSS3 transformations and Font Awesome for the icons 
(I would suggest to use /1.2.8/angular-animate.js, there is a weird blinking in newer versions.)

**angularjs-toaster-fontawesome** is basically **AngularJS Toaster**, but the hard-coded raster images have been replaced with equivalent Font Awesome icons. Apart from that, I made a few CSS tweaks to fix up some minor errors.

### Current Version 0.4.11

## Demo (for AngularJS Toaster)
- Simple demo is at http://plnkr.co/edit/HKTC1a
- Older versions are http://plnkr.co/edit/1poa9A or http://plnkr.co/edit/4qpHwp or http://plnkr.co/edit/lzYaZt (with version 0.4.5)
- Older version with Angular 1.2.0 is placed at http://plnkr.co/edit/mejR4h
- Older version with Angular 1.2.0-rc.2 is placed at http://plnkr.co/edit/iaC2NY
- Older version with Angular 1.1.5 is placed at http://plnkr.co/mVR4P4

## Getting started

Optionally: to install with bower, use:
```
bower install --save angularjs-toaster-fontawesome
```

* Add toaster container directive: 

```html
<toaster-container></toaster-container>
```

* Prepare the call of toaster method:

```js
    angular.module('main', ['toaster'])
    .controller('myController', function($scope, toaster) {
        $scope.pop = function() {
            toaster.pop('success', "title", "text");
        };

        $scope.someMoreExamples = function() {
            toaster.pop('success', "Title",   "Some descriptive text"      );
            toaster.pop('warning', "Title",   "Some descriptive text", 9000); // Disappear after 9 seconds
            toaster.pop('error',   "Title",   undefined,               9000); // Disappear after 9 seconds
            toaster.pop('wait',    undefined, "Description with no title"  );
            toaster.pop('info',    "Title"                                 );
        }
    });
```

* Call controller method on button click:

```html
<div ng-controller="myController">
    <button ng-click="pop()">Pop some toast!</button>
</div>
```

### Configuration Options

```html
// Change display position
<toaster-container toaster-options="{'position-class': 'toast-top-full-width'}"></toaster-container>
```

Other acceptable position-class values include: toast-top-full-width, toast-bottom-full-width, toast-top-left, toast-top-center, toast-top-right, toast-bottom-right, toast-bottom-center, toast-bottom-left, toast-center


### Animations
Unlike toastr, this library relies on ngAnimate and CSS3 transformations for animations.
		
## Author of AngularJS Toaster
**Jiri Kavulak**

## Credits
Inspired by http://codeseven.github.io/toastr/demo.html.

## Copyright
Copyright © 2013 [Jiri Kavulak](https://twitter.com/jirikavi).

## License
AngularJS-Toaster is under MIT license - http://www.opensource.org/licenses/mit-license.php
angularjs-toaster-fontawesome is under MIT license - http://www.opensource.org/licenses/mit-license.php

