---
layout: post
title: hopes and dreams store
categories: testing
tags: [html]
---

<!DOCTYPE html>
<html>
<head>
<title>Hopes and Dreams Store</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>

@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono&display=swap');

* {
font-family: 'Roboto Mono', monospace;
}

.topnav {
	top: 0px;
	background-color: #333;
	padding: 15px;
	align-items : center;
	display: flex;
	font-size: 25px;
	margin: 0px;
	position: sticky;
	z-index: 1;
}

.topnav a:link {
	color: white;
	background-color: transparent;
	text-decoration: none;
	font-family: Courier New;
}

.topnav a:visited {
	color: white;
	background-color: transparent;
	text-decoration: none;
}
.topnav a:hover {
	color: #848785;
	background-color: transparent;
	text-decoration: none;
}
.topnav a:active {
	color: #848785;
	background-color: transparent;
	text-decoration: none;
}

.normal {
	margin-left: 30px;
	margin-right: 30px;
}

.footer {
	background-color: #333;
	padding: 5px;
	align-items : center;
	display: flex;
	position: relative;
	bottom: 0px;
	color: white;
}

.footer * {
	margin-left: 12px;
	font-size: 15px;
	font-family: Courier New;
}

.title {
	background-color: #515751;
	padding: 10px;
	position: static;
	pointer-events: none
}

.title a:hover {
	color: #C2C1A5;
	background-color: transparent;
	text-decoration: none;
}

.title a:link {
	color: #F5F9E9;
	background-color: transparent;
	text-decoration: none;
}

.title a:visited {
	color: #C2C1A5;
	background-color: transparent;
	text-decoration: none;
}

.title a:active {
	color: #C2C1A5;
	background-color: transparent;
	text-decoration: none;
}

.center {
  margin-left: auto;
  margin-right: auto;
}

.products {
	style: border=0;
	margin-left: auto;
	margin-right: auto;
}
</style>
</head>

<body style="margin:0px">
<div class="topnav">
	<a href="index.html"><img src="goofydog.png" alt="Home" width="100" height="50"></a>
	<a href="index.html">Home </a>
	<a href="Products.html">Products </a>
	<a href="About.html">About </a>
</div>

</body>

<body>
<script>
var TxtType = function(el, toRotate, period) {
        this.toRotate = toRotate;
        this.el = el;
        this.loopNum = 0;
        this.period = parseInt(period, 10) || 2000;
        this.txt = '';
        this.tick();
        this.isDeleting = false;
    };

    TxtType.prototype.tick = function() {
        var i = this.loopNum % this.toRotate.length;
        var fullTxt = this.toRotate[i];

        if (this.isDeleting) {
        this.txt = fullTxt.substring(0, this.txt.length - 1);
        } else {
        this.txt = fullTxt.substring(0, this.txt.length + 1);
        }

        this.el.innerHTML = '<span class="wrap">'+this.txt+'</span>';

        var that = this;
        var delta = 200 - Math.random() * 100;

        if (this.isDeleting) { delta /= 2; }

        if (!this.isDeleting && this.txt === fullTxt) {
        delta = this.period;
        this.isDeleting = true;
        } else if (this.isDeleting && this.txt === '') {
        this.isDeleting = false;
        this.loopNum++;
        delta = 500;
        }

        setTimeout(function() {
        that.tick();
        }, delta);
    };

    window.onload = function() {
        var elements = document.getElementsByClassName('typewrite');
        for (var i=0; i<elements.length; i++) {
            var toRotate = elements[i].getAttribute('data-type');
            var period = elements[i].getAttribute('data-period');
            if (toRotate) {
              new TxtType(elements[i], JSON.parse(toRotate), period);
            }
        }
        // INJECT CSS
        var css = document.createElement("style");
        css.type = "text/css";
        css.innerHTML = ".typewrite > .wrap { border-right: 0.08em solid #fff}";
        document.body.appendChild(css);
    };
</script>

<center>
<div>
<h1 class="title">
  <a href="javascript:void(0)" class="typewrite" data-period="2000" data-type='[ "Hopes and Dreams Store" ]'>
    <span class="wrap"></span>
  </a>
</h1>
</div>
</center>


<em><h1 style="text-align: center">New Arrivals</h1></em>




<tr>
<a href="Products.html">
<table class="products">
<TD><img src="happ.png" width="300px"></TD>
<TD><img src="quack.webp" width="400px"></TD>	
<TD><img src="gaming.jpg" width="400px"></TD>
</tr>
</table>
</a>

<img src="4090.jpg" alt="RTX 4090 Image" width="100%">
<h1 class="normal" style="text-align:center">Newest, Fastest, Coolest.</h1>
<h3 class="normal" style="text-align:center">Level up your ROBLOX gaming experience with the latest generation of Nvidia GPUs. Now available with our line of ASUSSY systems.</h3>
<footer class="footer">
<div>
  <p>&#169;2022 Christopher Tan</p>
</div>
</footer> 
</body>
</html>


<!-- https://coolors.co/36453b-596869-515751-f5f9e9-c2c1a5 -->
