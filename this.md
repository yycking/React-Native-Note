# 調用該函式之物件

* 物件.函式()

  ```javascript
  var obj = {
  	x: 20,
  	f: function(){ console.log(this.x); }
  };

  obj.f(); //obj.x = 20

  obj.innerobj = {
  	x: 30,
  	f: function(){ console.log(this.x); }
  }

  obj.innerobj.f(); //obj.innerobj.x = 30
  ```




# 全域物件

* 函式()

  ```javascript
  var x = 10;
  var f = function(){
  	console.log(this.x);
  };

  f(); // global.x = 10
  ```

  ```javascript
  var x = 10;
  var obj = {
  	x: 20,
  	f: function(){
  		console.log(this.x); // obj.x = 20;
  		var foo = function(){ console.log(this.x); }
  		foo(); // global.x = 10
  	}
  };

  obj.f();
  ```

  ```javascript
  var x = 10;
  var obj = {
  	x: 20,
  	f: function(){
  		console.log(this.x); // obj.x = 20;
  		var that = this; // that = obj
      	var foo = function(){ console.log(that.x); }
  		foo(); // that.x = 20
  	}
  };

  obj.f();
  ```

  ```javascript
  var x = 10;
  var obj = {
  	x: 20,
  	f: function(){ console.log(this.x); }
  };

  obj.f(); // obj.x = 20
  var fOut = obj.f;
  fOut();  // global.x = 10
  var obj2 = {
  	x: 30,
  	f: obj.f
  }

  obj2.f(); // obj2.x = 30
  ```




# 更改this指派的物件

* (A物件.)函式.call(B物件,參數1,參數2,參數3, ......); //函式的this指向B物件(若B物件為null，則指向全域物件)

* (A物件.)函式.apply(B物件,[參數1,參數2,參數3, ......]); //函式的this指向B物件(若B物件為null，則指向全域物件)

  ```javascript
  var obj = {
  	x: 20;
  	f: function(){ console.log(this.x); }
  };

  var obj2 = {
  	x: 30;
  };

  obj1.f.call(obj2); // obj2.x = 30
  ```




# 新物件

* new 建構式();

  ```javascript
  function Monster(){
  	this.hp = 100;
  };

  var monster = new Monster();  // monster.hp = 100
  // 同下
  var monster = (
  	function(){
  		var _new = { constructor: Monster, __proto__: Monster.prototype };
  		_new.constructor();
  		return _new;
  	}
  )();
  ```




# 箭頭函式

* 函式內和外一樣

  ```javascript
  var x = 10;
  var obj = {
  	x: 20,
  	f: function(){
  		console.log(this.x); // obj.x = 20;
  		var foo = function(){ console.log(this.x); }
  		foo(); // global.x = 10
  	}
  };

  obj.f();
  ```

  ```javascript
  var x = 10;
  var obj = {
  	x: 20,
  	f: () => {
  		console.log(this.x); // global.x = 10;
  		var foo = function(){ console.log(this.x); }
  		foo(); // global.x = 10
  	}
  };

  obj.f();
  ```
  ```javascript
  var x = 10;
  var obj = {
  	x: 20,
  	f: function(){
  		console.log(this.x); // obj.x = 20;
  		var foo = () => console.log(this.x);
  		foo(); // obj.x = 20;
  	}
  };

  obj.f();
  ```

  ```javascript
  var x = 10;
  var obj = {
  	x: 20,
  	f: () => {
  		console.log(this.x); // global.x = 10
  		var foo = () => console.log(this.x);
  		foo(); // global.x = 10
  	}
  };

  obj.f();
  ```

  ​