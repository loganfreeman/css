Links
---
- [Force Hardware Acceleration in WebKit with translate3d](https://davidwalsh.name/translate3d)


The WebKit CSS
---
```css
/* warp speed ahead */
.animClass {
	-webkit-transform: translate3d(0, 0, 0);
	/* more specific animation properties here */
}
```
The use of translate3d pushes CSS animations into hardware acceleration. Even if you're looking to do a basic 2d translation, use translate3d for more power! If your animation is still flickering after switching to the transform above, you can use a few little-known CSS properties to try to fix the problem:

```css
.animClass {
	-webkit-backface-visibility: hidden;
	-webkit-perspective: 1000;
}
```


```scss
	/* Force Hardware Acceleration in WebKit */
	@include transform(translateZ(0));
	@include backface-visibility(hidden);
 ```
