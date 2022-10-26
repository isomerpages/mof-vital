---
title: Life in VITAL
permalink: /career/life-in-vital/
description: Life in VITAL
---
<html>
<head>
	<style>
		* {
			margin: 0;
		}

		body {
			background: lightgreen;
			min-height: 100vh;
		}

		.thumbnails {
			display: flex;
			flex-direction: column;
			width: 200px;
			height: 200px;
			position: absolute;
			left: 10%;
			top: 5%;
		}

		.thumbnails img {
			margin: 0 20px 20px;
			opacity: 1;
			transition: 0.3s;
		}

		img {
			max-width: 100%;
			max-height: 100%;
		}

		.mainDiv {
			padding: 40px 0;
			display: flex;
			flex-direction: row;
		}

		.figure {
			max-width: 800px;
			margin: 0 auto 40px;
			position: absolute;
			left: 28%;
			top: 5%;
		}

		.figure img {
			max-width: 100%;
			min-width: 100%;
			height: 650px;
			width: 650px;
		}
	</style>
	<script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js">
	</script>
</head>
<body>
	<div class="mainDiv">

		<!--div for left thumbanails-->
		<div class="thumbnails">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
		</div>

		<!--div for main image-->
		<div class="figure">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
		</div>

		<!--div for right thumbanails-->
		<div class="thumbnails" style="left:75%;">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
			<img src=
"/images/Media/InPersonTownhall2022_Image3.jpg">
		</div>
	</div>
	<script>
		// When webpage will load, everytime below
		// function will be executed
		$(document).ready(function () {

			// If user clicks on any thumbanil,
			// we will get it's image URL
			$('.thumbnails img').on({
				click: function () {
					let thumbnailURL = $(this).attr('src');

					// Replace main image's src attribute value
					// by clicked thumbanail's src attribute value
					$('.figure img').fadeOut(200, function () {
						$(this).attr('src', thumbnailURL);
					}).fadeIn(200);
				}
			});
		});
	</script>
</body>
</html>