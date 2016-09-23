# AngularJS

Sources are:

- http://campus.codeschool.com/courses/shaping-up-with-angular-js/


## Basics


![image](https://docs.angularjs.org/img/guide/concepts-databinding1.png)


### Modules
Create a new module named gemStore
	
	var app = angular.module('gemStore', []);
	
### Controller

	myApp.controller('GreetingController', function($scope) {
		$scope.greeting = 'Hola!';
	});
	
`$scope` is a global variable that keeps the application scope.

In the HTML File, you add the controller to a tag via

	  <body ng-controller="GreetingController as gc">

Now, gc is available in all tags inside of the body tag. 

####Directives

* ng-show

		<div ng-hide="product.isAllowedToOrder">
* ng-hide
	
		<div ng-hide="product.isOutOfStock">
	If you want to show or hide something, depending on an array that has 0 or >1 elements, just use `product.images.lengtt` as an expression.
* ng-repeat 
 
 		<div ng-repeat="product in store.products"></div>

* ng-src is used for image-tags. You need this, because otherwise the browser would try to load the image before the angular code is executed.

		<img ng-src = "{{product.images[1]}}" />
		

## Dynamic Stuff

A two way data binding means, that if one status is change, the 

####Directives

* ng-class

		 <li ng-class=" { active:tab.isSet(3)  } ">
* ng-click

		<a href ng-click="tab.setTab(3)">Reviews</a></li>


		
### Filters
You can add a filter after an expression or in a directive.

For example: 
	
	{{product.price | currency }}
	
formats the product.price as a currency. Othder filters are _uppercase_, _limitTo:8_, _date:'MM/dd/yyyy @ h:mma'_, _orderBy='-price'_

Another example:

	<li ng-repeat="products in product | orderBy='-price'">
	
### Tabbing


## Models
