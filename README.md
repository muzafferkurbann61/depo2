
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>ISMIN'in Kırık Kalbi</title>

<style>
body{
    margin:0;
    padding:0;
    background: radial-gradient(circle, #111, #000);
    height:100vh;
    overflow:hidden;
    font-family: Arial, sans-serif;
    color:white;
    text-align:center;
}

.container{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
}

h1{
    font-size:40px;
    color:#ff4d4d;
}

p{
    font-size:16px;
    color:#ccc;
    max-width:400px;
    margin:auto;
    line-height:1.6;
}

.heart{
    position:absolute;
    color:red;
    font-size:20px;
    animation:fall 6s linear infinite;
}

@keyframes fall{
    0%{
        transform:translateY(-10vh);
        opacity:1;
    }
    100%{
        transform:translateY(110vh);
        opacity:0;
    }
}
</style>
</head>

<body>

<div class="container">
<h1>ISMIN'in Kırık Kalbi 💔</h1>

<p>
Bazı insanlar hayatına gelmez…  
sadece kalbinde bir iz bırakır.  

Ben hâlâ aynı yerdeyim.  
Ama içimdeki biri artık eskisi gibi değil.
</p>

</div>

<audio autoplay loop>
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<script>

function createHeart(){
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML="💔";

    heart.style.left = Math.random()*100 + "vw";
    heart.style.animationDuration = (3 + Math.random()*5) + "s";
    heart.style.fontSize = (15 + Math.random()*25) + "px";

    document.body.appendChild(heart);

    setTimeout(()=>{
        heart.remove();
    },7000);
}

setInterval(createHeart,300);
</script>

</body>
</html>