# ChinaCitySelect

![test](https://raw.githubusercontent.com/MrHuxu/img-repo/master/city-select/test.gif)

This is a plugin to make it easy to add a China region selector into your Angular app.

## Install

Install this plugin by using bower.

	# enter your asset directory
	bower install angular cn-city-select --save

## Usage

1. First of all you should load Angularjs in your page, and then load this plugin.
	
		<!-- place this code into your page -->
		<script type="text/javascript" src='/xxx/angular.min.js'></script>
		<script type="text/javascript" src='/xxx/cn-city-select.min.js'></script>
		<script type='text/javascript' src='/xxx/yourJS.js'></script>

2. Then create your own Angular module, controller and city-select div.

		<div ng-app='yourModule'>
			<div city-select></div>
		</div>

3. Import the module into your module, and then the plugin works!

		// place this code into yourJS.js
		angular.module('yourModule', ['cnCitySelect'])

4. There are two attributes belong to directive.
	
	- ```select-result```: This attribute will pass a name of variable and provide a data binding between the variable and select result.
	- ```select-class```: This attribute will pass a string which will be assigned to the ```class``` attribute of each ```select``` element.
		
## Sample

This is a small sample of this plugin.

	<html>
	<meta charset="UTF-8">
	<style>
	  .test-class {margin: 30px 0 0 30px; font-size: 30px}
	</style>
	<body>
	  <div ng-app='testModule'>
	    <div ng-controller='testCtrl'>
	      <div select-result='result' select-class='test-class' city-select></div>
	      <p>{{result}}</p>
	    </div>
	  </div>
	</body>
	<script src='./angular.min.js'></script>
	<script src='./cn-city-select.min.js'></script>
	<script>
	  angular.module('testModule', ['cnCitySelect']).controller('testCtrl', function ($scope) {});
	</script>
	</html>
	
![demo](https://raw.githubusercontent.com/MrHuxu/img-repo/master/city-select/demo.gif)
