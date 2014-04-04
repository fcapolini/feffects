# FEffects

![Flash example](http://mromecki.fr/blog/post/24/chips.swf)

FEffects is a library that enables you to create visual transitions like motion-tweens for example.

The package contains a Tween class and Robert Penners' easings.

It can be used the same way, in your Flash, javascript, neko and cpp projects. You can of course use it in a NME project too (windows, linux, OSX, android, iOS, HTML5).

## Usage

	import feffects.Tween;

	using feffects.Tween.TweenObject;
	...

	var mySprite = new Sprite();
	mySprite.graphics.beginFill( 0 );
	mySprite.graphics.drawCircle( 0, 0, 20 );
	mySprite.graphics.endFill();

	Lib.current.addChild( mySprite );

	function update ( n : Float ) {
			trace( n );
	}

	function finish() {
			trace( "end" );
	}

	new Tween( 0, 100, 1000, update, finish, true );

	OR

	mySprite.tween( { x : 100, y : 200 }, 1000 ).onFinish( finish).start();

	OR

	mySprite.tween( { x : 100, y : 200 }, 1000, finish, true );
	
## Examples

[Javascript example](http://mromecki.fr/blog/post/36/testTweenJS.html)
	
[Flash example](http://mromecki.fr/blog/post/36/flash9+.swf)
	
[Another Javascript example](http://mromecki.fr/blog/post/25/projectJS.html)
	
[Another Flash example](http://mromecki.fr/blog/post/25/projectSWF.html)