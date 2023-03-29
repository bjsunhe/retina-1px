# retina-1px


```

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no"/>
  <meta name="msapplication-tap-highlight" content="no" />
  <title>retina屏的1px</title>
</head>
<body>
  <div class="border_top1">border-top:1px</div>
  <div class="border_top2">border-top:0.5px<br />gradient</div>
  <div class="border_top3">border-top:0.5px<br />scale</div>
  <div class="border_top4">border-top:0.5px<br />image,base64</div>
  <div class="border1">border:1px</div>
  <div class="border2">border:0.5px<br />gradient</div>
  <div class="border3">border:0.5px<br />before,scale</div>
  <div class="border_svg">svg</div>
</body>



* {
  margin:0;
  padding:0;
}
div {
  width:200px;
  height:80px;
  margin:30px auto;
  background-color:#efefef;
}

/*border-top:1px*/
.border_top1,.border_top2,.border_top3,.border_top4 {
  border-top:1px solid #999;
}

@media(-webkit-min-device-pixel-ratio:2),(min-resolution:192dpi) {
	.border_top2 {
		background-image:-webkit-linear-gradient(top,transparent 50%,#999 50%);
		background-image:linear-gradient(to top,transparent 50%,#999 50%);
		background-size:100% 1px;
		background-repeat:no-repeat;
		background-position:top center;
		border-top:0 none;
		padding-top:1px;
	}
	.border_top3 {
    position:relative;
    padding-top:1px;
    border-top:0 none;
  }
  .border_top3:before {
    content:"";
    position:absolute;
    top:0;
    left:0;
    width:200%;
		border-top:1px solid #999;
		-webkit-transform:scale(0.5);
		-ms-transform:scale(0.5);
		transform:scale(0.5);
		-webkit-transform-origin:0 0;
		-ms-transform-origin:0 0;
		transform-origin:0 0;
		-webkit-box-sizing:border-box;
		box-sizing:border-box;
	}
	.border_top4 {
    padding-top:1px;
    border-top:0 none;
		background-image:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAACCAYAAACZgbYnAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAQSURBVBhXY5g5c+Z/BhAAABRcAsvqBShzAAAAAElFTkSuQmCC);
		background-position:0 0;
		background-repeat:repeat-x;
		background-size:1px 1px;
	}
}

/*border:1px*/
.border1,.border2,.border3 {
  border:1px solid #999;
}
@media(-webkit-min-device-pixel-ratio:2),(min-resolution:192dpi) {
	.border2 {
		background-image:-webkit-linear-gradient(top,transparent 50%,#999 50%),
		-webkit-linear-gradient(right,transparent 50%,#999 50%),
		-webkit-linear-gradient(bottom,transparent 50%,#999 50%),
		-webkit-linear-gradient(left,transparent 50%,#999 50%);
		background-image:linear-gradient(to top,transparent 50%,#999 50%),
		linear-gradient(to right,transparent 50%,#999 50%),
		linear-gradient(to bottom,transparent 50%,#999 50%),
		linear-gradient(to left,transparent 50%,#999 50%);
		background-size:100% 1px,1px 100%,100% 1px,1px 100%;
		background-repeat:no-repeat;
		background-position:top center,right center,bottom center,left center;
		border:0 none;
		padding:1px;
	}
	.border3 {
    position:relative;
    padding:1px;
    border:0 none;
  }
  .border3:before {
    content:"";
    position:absolute;
    top:0;
    left:0;
    width:200%;
    height:200%;
		border:1px solid #999;
		-webkit-transform:scale(0.5);
		-ms-transform:scale(0.5);
		transform:scale(0.5);
		-webkit-transform-origin:0 0;
		-ms-transform-origin:0 0;
		transform-origin:0 0;
		-webkit-box-sizing:border-box;
		box-sizing:border-box;
	}
}

/*border_svg*/
.border_svg {
  border-bottom:1px solid #999;
  border-left:1px solid #999;
}
@media(-webkit-min-device-pixel-ratio:2),(min-resolution:192dpi) {
	.border_svg {
		border-bottom:0 none;
    border-left:0 none;
		background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='100%' height='1'><rect fill='#999' x='0' y='0.5' width='100%' height='0.5' /></svg>"),url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1' height='100%'><rect fill='#999' x='0' y='0' width='0.5' height='100%' /></svg>");	
	 	background-position:0 100%,0 0;
	 	background-repeat:no-repeat;
	}
}

```
