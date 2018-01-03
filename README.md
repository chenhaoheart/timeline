# timeline
html+css timeline

/* --------------------------------

Primary style

-------------------------------- */
@charset "utf-8";
/* CSS Document */
h1,h2,h3,h4,h5,h6,label
{margin:0;padding:0;border:0;outline:0;font-size:100%;vertical-align:baseline;background:transparent}
a{color:#007bc4/*#424242*/; text-decoration:none;outline: none;}
a:hover{text-decoration:underline}
a:focus {outline:none; -moz-outline:none;}
ol,ul{list-style:none}
table{border-collapse:collapse;border-spacing:0}
body{height:100%; font:14px/18px "Microsoft Yahei", Tahoma, Helvetica, Arial, Verdana, "\5b8b\4f53", sans-serif; color:#51555C;}
img{border:none}

#main{width:980px; min-height:600px; margin:30px auto 0 auto; border:1px solid #d3d3d3; background:#fff; -moz-border-radius:5px;-khtml-border-radius: 5px;-webkit-border-radius: 5px; border-radius:5px;}

#footer{height:60px;}
#footer p{ padding:10px 2px; line-height:24px; text-align:center}
#footer p a:hover{color:#51555C}
#stat{display:none}

.google_ad{width:728px; height:90px; margin:50px auto}
.ad_76090,.ad_demo{width:760px; height:90px; margin:40px auto}
.demo_topad{position:absolute; top:15px; right:0px; width:472px; height:60px;}

@media screen and (min-width: 320px) and (max-width : 480px) {
 html{-webkit-text-size-adjust: none;}
 #header{width:100%}
 .logo{width:60px; height:60px; margin: 10px auto; background:url(../images/logo.png) no-repeat 0 10px;text-indent:-999em;}
.logo a{display:block; width:60px; height:60px}
 #main{width:100%; margin:10px auto;  -moz-border-radius:0px;-khtml-border-radius: 0px;-webkit-border-radius: 0px; border-radius:0px;}
 .demo_topad{display:none}
 .google_ad{width:100%; margin:40px auto; text-align:center}
.ad_76090,.ad_demo{width:100%; height:auto; margin:40px auto;text-align:center}
.demo{width:98%; margin:10px auto}
}
html * {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

*, *:after, *:before {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

body {
  font-size: 100%;
  color: #7f8c97;
  background-color: #e9f0f5;
}



img {
  max-width: 100%;
}

/* --------------------------------

Modules - reusable parts of our design

-------------------------------- */
.cd-container {
  /* this class is used to give a max-width to the element it is applied to, and center it horizontally when it reaches that max-width */
  width: 90%;
  max-width: 1170px;
  margin: 0 auto;
}
.cd-container::after {
  /* clearfix */
  content: '';
  display: table;
  clear: both;
}

/* --------------------------------

Main components

-------------------------------- */

#cd-timeline {
  position: relative;
  padding: 2em 0;
  margin-top: 2em;
  margin-bottom: 2em;
}
#cd-timeline::before {
  /* this is the vertical line */
  content: '';
  position: absolute;
  top: 0;
  left: 18px;
  height: 100%;
  width: 4px;
  background: #d7e4ed;
}
@media only screen and (min-width: 1170px) {
  #cd-timeline {
    margin-top: 3em;
    margin-bottom: 3em;
  }
  #cd-timeline::before {
    left: 50%;
    margin-left: -2px;
  }
}

.cd-timeline-block {
  position: relative;
  margin: 2em 0;
}
.cd-timeline-block:after {
  content: "";
  display: table;
  clear: both;
}
.cd-timeline-block:first-child {
  margin-top: 0;
}
.cd-timeline-block:last-child {
  margin-bottom: 0;
}
@media only screen and (min-width: 1170px) {
  .cd-timeline-block {
    margin: 4em 0;
  }
  .cd-timeline-block:first-child {
    margin-top: 0;
  }
  .cd-timeline-block:last-child {
    margin-bottom: 0;
  }
}

.cd-timeline-img {
  position: absolute;
  top: 0;
  left: 0;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  box-shadow: 0 0 0 4px white, inset 0 2px 0 rgba(0, 0, 0, 0.08), 0 3px 0 4px rgba(0, 0, 0, 0.05);
}
.cd-timeline-img img {
  display: block;
  width: 24px;
  height: 24px;
  position: relative;
  left: 50%;
  top: 50%;
  margin-left: -12px;
  margin-top: -12px;
}
.cd-timeline-img.cd-picture {
  background: #75ce66;
}
.cd-timeline-img.cd-movie {
  background: #c03b44;
}
.cd-timeline-img.cd-location {
  background: #f0ca45;
}
@media only screen and (min-width: 1170px) {
  .cd-timeline-img {
    width: 60px;
    height: 60px;
    left: 50%;
    margin-left: -30px;
    /* Force Hardware Acceleration in WebKit */
    -webkit-transform: translateZ(0);
    -webkit-backface-visibility: hidden;
  }
  .cssanimations .cd-timeline-img.is-hidden {
    visibility: hidden;
  }
  .cssanimations .cd-timeline-img.bounce-in {
    visibility: visible;
    -webkit-animation: cd-bounce-1 0.6s;
    -moz-animation: cd-bounce-1 0.6s;
    animation: cd-bounce-1 0.6s;
  }
}

.cd-timeline-content {
  position: relative;
  margin-left: 60px;
  background: white;
  border-radius: 0.25em;
  padding: 1em;
  box-shadow: 0 3px 0 #d7e4ed;
}
.cd-timeline-content:after {
  content: "";
  display: table;
  clear: both;
}
.cd-timeline-content h2 {
  color: #303e49;
}
.cd-timeline-content p, .cd-timeline-content .cd-read-more, .cd-timeline-content .cd-date {
  font-size: 13px;
  font-size: 0.8125rem;
}
.cd-timeline-content .cd-read-more, .cd-timeline-content .cd-date {
  display: inline-block;
}
.cd-timeline-content p {
  line-height: 1.6;
}
.cd-timeline-content .cd-read-more {
  float: right;
  padding: .8em 1em;
  background: #acb7c0;
  color: white;
  border-radius: 0.25em;
}
.no-touch .cd-timeline-content .cd-read-more:hover {
  background-color: #bac4cb;
}
a.cd-read-more:hover{text-decoration:none; background-color: #424242;  }
.cd-timeline-content .cd-date {
  float: left;
  padding: .8em 0;
  opacity: .7;
}
.cd-timeline-content::before {
  content: '';
  position: absolute;
  top: 16px;
  right: 100%;
  height: 0;
  width: 0;
  border: 7px solid transparent;
  border-right: 7px solid white;
}
@media only screen and (min-width: 768px) {
  .cd-timeline-content h2 {
    font-size: 20px;
    font-size: 1.25rem;
  }
  .cd-timeline-content p {
    font-size: 16px;
    font-size: 1rem;
  }
  .cd-timeline-content .cd-read-more, .cd-timeline-content .cd-date {
    font-size: 14px;
    font-size: 0.875rem;
  }
}
@media only screen and (min-width: 1170px) {
  .cd-timeline-content {
    margin-left: 0;
    padding: 1.6em;
    width: 45%;
  }
  .cd-timeline-content::before {
    top: 24px;
    left: 100%;
    border-color: transparent;
    border-left-color: white;
  }
  .cd-timeline-content .cd-read-more {
    float: left;
  }
  .cd-timeline-content .cd-date {
    position: absolute;
    width: 100%;
    left: 122%;
    top: 6px;
    font-size: 16px;
    font-size: 1rem;
  }
  .cd-timeline-block:nth-child(even) .cd-timeline-content {
    float: right;
  }
  .cd-timeline-block:nth-child(even) .cd-timeline-content::before {
    top: 24px;
    left: auto;
    right: 100%;
    border-color: transparent;
    border-right-color: white;
  }
  .cd-timeline-block:nth-child(even) .cd-timeline-content .cd-read-more {
    float: right;
  }
  .cd-timeline-block:nth-child(even) .cd-timeline-content .cd-date {
    left: auto;
    right: 122%;
    text-align: right;
  }
  .cssanimations .cd-timeline-content.is-hidden {
    visibility: hidden;
  }
  .cssanimations .cd-timeline-content.bounce-in {
    visibility: visible;
    -webkit-animation: cd-bounce-2 0.6s;
    -moz-animation: cd-bounce-2 0.6s;
    animation: cd-bounce-2 0.6s;
  }
}

@media only screen and (min-width: 1170px) {
  /* inverse bounce effect on even content blocks */
  .cssanimations .cd-timeline-block:nth-child(even) .cd-timeline-content.bounce-in {
    -webkit-animation: cd-bounce-2-inverse 0.6s;
    -moz-animation: cd-bounce-2-inverse 0.6s;
    animation: cd-bounce-2-inverse 0.6s;
  }
}


<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>演示：HTML5+CSS3实现的响应式垂直时间轴</title>
<link rel="stylesheet" href="style.css" />
<style type="text/css">
</style>
</head>

<body>
<section id="cd-timeline" class="cd-container">
	<div class="cd-timeline-block">
		<div class="cd-timeline-img cd-picture">
      <div class="serial-number" style="display:flex">
        <span style="font-size:50px">1</span>
      </div>
		</div>
		<div class="cd-timeline-content">
			<p>特朗普通过美国新税务法案</p>
			<span class="cd-date">2015-01-06</span>
		</div>
	</div>
	<div class="cd-timeline-block">
		<div class="cd-timeline-img cd-picture">
		</div>

		<div class="cd-timeline-content">
			<p>美国加息</p>
			<span class="cd-date">2014-12-25</span>
		</div>
	</div>
	<div class="cd-timeline-block">
		<div class="cd-timeline-img cd-picture">

		</div>
		<div class="cd-timeline-content">
			<p>美国加息</p>
			<span class="cd-date">2014-12-20</span>
		</div>
	</div>

</section>

</body>
</html>
