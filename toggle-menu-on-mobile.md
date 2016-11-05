js
```js
	$('.cd-main-nav').on('click', function(event){
		if($(event.target).is('.cd-main-nav')) $(this).children('ul').toggleClass('is-visible');
	});
```
css
```
.cd-header {
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: $header-height-S;
	background: $color-1;
	box-shadow: 0 1px 3px rgba(#000, .2);
	z-index: index($elements, navigation); // see partials > _variables.scss
	@include clearfix;

	#cd-logo {
		float: left;
		margin: 13px 0 0 5%;

		img {
			display: block;
		}
	}

	@include MQ(M) {
		height: $header-height-M;

		#cd-logo {
			margin: 23px 0 0 5%;
		}
	}
}

.cd-main-nav {
	float: right;
	margin-right: 5%;
	width: 44px;
	height: 100%;
	background: url('../img/cd-icon-menu.svg') no-repeat center center;
	background-size: 44px 44px;
	cursor: pointer;

	ul {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		@include transform(translateY(-100%));

		&.is-visible {
			@include transform(translateY($header-height-S));
		}
	}

	a {
		display: block;
		height: $header-height-S;
		line-height: $header-height-S;
		padding-left: 5%;
		background: $background;
		border-top: 1px solid lighten($background, 3%);
		color: #FFF;
	}

	@include MQ(M) {
		width: auto;
		height: auto;
		background: none;
		cursor: auto;

		ul {
			position: static;
			width: auto;
			@include transform(translateY(0));
			line-height: $header-height-M;

			&.is-visible {
				@include transform(translateY(0));
			}
		}

		li {
			display: inline-block;
			margin-left: 1em;
		}

		a {
			display: inline-block;
			height: auto;
			line-height: normal;
			background: transparent;
			padding: .6em 1em;
			border-top: none;
			@include font-size(13px);
			font-weight: bold;
			text-transform: uppercase;
		}
	}
}
```
