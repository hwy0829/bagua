# bagua
八卦图纯css手写
js部分--引入JQ版本

<script type="text/javascript" src="http://cdn.gbtags.com/jquery/1.11.1/jquery.min.js"></script>

html部分
<div id="container">
	<div class="rotate"></div>
</div>

css部分--css3属性

/*CSS源代码*/
body{
	background:#CFCFCF;
}
.rotate {
	width:0;
	height:400px;
	position:relative;
	margin:50px auto;
	border-left:200px solid #000;
	border-right:200px solid #fff;
	box-shadow:10px 10px 30px rgba(0,0,0,.5);
	border-radius:400px;
	animation:rotation 5s linear infinite;
	-webkit-animation:rotation 5s linear infinite;
	-moz-animation:rotation 5s linear infinite;
}
.rotate:before,
.rotate:after {
	position:absolute;content:"";display:block;
}
.rotate:before {
	width:200px;
	height:200px;
	top:0;
	left:-100px;
	text-align: center; 
	z-index:1;
	background-color:#fff;
	border-radius:50%;
	box-shadow:0 200px 0 #000;
}
.rotate:after {
	width:60px;
	height:60px;
	top:70px;
	left:-30px;
	z-index:2;
	background-color:#000;
	text-align: center;
	border-radius:50%;
	box-shadow:0 200px 0 #fff;
	}
span{
	z-index: 3;
	position: absolute;
	left:775px;
	animation:rotation 5s ease-out infinite;
	-moz-animation:rotation 5s ease-out infinite;
	-webkit-animation:rotation 5s ease-out infinite; 
	font-family: "微软雅黑";
	font-size: 14px;
	}
.bai{
	color: #fff;
	top:120px;
}
.hei{
	color: #000;
	top:340px;
}

@keyframes rotation {
    0% {
	transform: rotateY(0deg);
    }
    100% {
	transform: rotateY(-360deg);
    }
}
@-webkit-keyframes rotation {
    0% {
	-webkit-transform: rotateY(0deg); 
    }
    100% {
	-webkit-transform: rotateY(-360deg); 
    }
}

@-moz-keyframes rotation {
    0% {
	-moz-transform: rotateY(0deg);
    }
    100% {
	-moz-transform: rotateY(-360deg);
    }
}

//这个是没有时间限制的，如果需要可以自己添加事件
