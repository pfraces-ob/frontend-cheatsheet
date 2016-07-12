Angular 1
=========

Devtools
--------

### Load services

```js
window.require = function (service) {
  var appElement = document.querySelector('[ng-app]');
  return angular.element(appElement).injector().get(service);
};
```

### Update `$scope`

```js
window.scope = function (element) {
  var $scope = angular.element(element).scope();
  setTimeout($scope.$apply.bind($scope), 0);
  return $scope;
};
```

Usage

```js
scope($0).title = 'foo';
```

### Access controller's `$scope`

```js
window.ctrl = function (name, alias) {
  if (alias) { name += ' as ' + alias; }
  var ctrlElement = document.querySelector('[ng-controller="' + name + '"]');
  var scope = angular.element(ctrlElement).scope();
  if (alias) { scope = scope[alias]; }
  return scope;
};
```

Usage

```js
ctrl('myCtrl').exposedFunction();       // ng-controller="myCtrl"
ctrl('myCtrl', 'vm').exposedFunction(); // ng-controller="myCtrl as vm"
```

Source: <http://stackoverflow.com/a/13744085/1815446>
