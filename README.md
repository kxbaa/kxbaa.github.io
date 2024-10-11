<html>
<meta charset="UTF-8">
	<body style="background-color: #1a1a1a;">
		<p style="font-size: 70px; font-family: Impact; color: #e8d917;" align="center">The Duck Site</p>
		<img src="duck_main.png" alt="" style="display: block; margin: auto; background-color: #1a1a1a;">
		<p></p>
		<button 
        style="background-color: #e8d917; 
            color: #1a1a1a; 
            font-family: Impact; 
            font-size: 30px; 
            padding: 20px 40px; 
            border: none; 
            cursor: pointer;
            display: block; margin: auto;"
        onclick="playSound(); alert('The duck has quacked!');">
        Quack!
    </button>

<audio id="quackSound" src="quack.mp3"></audio>

	<script>
        function playSound() {
            const sound = document.getElementById('quackSound');
            sound.play();
        }
    </script>
		
   </body>
</html>
