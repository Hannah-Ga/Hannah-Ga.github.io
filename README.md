# Hannah-Ga.github.io

<!DOCTYPE html>

<html>
<head>
	<title>Button YouTube Player with Image</title>
	<script src="https://www.youtube.com/iframe_api"></script>
	<script>
		var player;
		function onYouTubeIframeAPIReady() {
			player = new YT.Player('audio', {
				height: '0',
				width: '0',
				videoId: '7mBr6fet70U',
				events: {
					'onReady': onPlayerReady
				}
			});
		}
		function onPlayerReady(event) {
			event.target.setVolume(100);
		}
		function playAudio() {
			player.playVideo();
			document.getElementById('image').style.display = 'block';
			document.body.style.backgroundImage = "url('https://i.imgur.com/R57Jo1P.png')";
			document.body.style.backgroundSize = "cover";
		}
	</script>
	<style>
		#audio {
			position: absolute;
			top: -9999px;
			left: -9999px;
		}
	</style>
</head>
<body>
	<div style="text-align:center;">
		<button onclick="playAudio()">I Love You</button>
	</div>
	<div id="audio"></div>
	<div style="text-align:center;">
		<img id="image" style="display:none; width: 300px; height: auto;" onerror="console.log('Error loading image');">
	</div>
</body>
</html>
