```js
_startProgress : function() {

	setTimeout( $.proxy( function() {
		this.$progress.css( { transition : 'width ' + this.options.interval + 'ms linear', width : '100%' } );
	}, this ), 25 );

},
_resetProgress : function() {
	this.$progress.css( { transition : 'none', width : '0%' } );
},
 ```
 
 
 ```css
 .cbp-qtprogress {
	position: absolute;
	background: #47a3da;
	height: 1px;
	width: 0%;
	top: 0;
	z-index: 1000;
}
```
