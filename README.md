<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>❤️ A Question ❤️</title>

<style>
body{
    margin:0;
    overflow:hidden;
    font-family:Arial,sans-serif;
    background:linear-gradient(135deg,#ffd6e7,#fff2f8);
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}

.card{
    text-align:center;
    background:white;
    padding:40px;
    border-radius:20px;
    box-shadow:0 10px 25px rgba(0,0,0,.15);
}

button{
    padding:15px 35px;
    font-size:22px;
    border:none;
    border-radius:40px;
    cursor:pointer;
    transition:.2s;
}

#yes{
    background:#ff4f8b;
    color:white;
    margin-right:20px;
}

#no{
    background:#ddd;
    color:black;
    position:fixed;
}
</style>
</head>

<body>

<div class="card">
    <h1> puwede ka ba ligawan </h1>
    <p>You'd make me really happy 🥹</p>

    <button id="yes">YES 💖</button>
    <button id="no">NO 🙈</button>
</div>

<script>
const yes=document.getElementById("yes");
const no=document.getElementById("no");

let size=1;

// Put No button in a visible position
no.style.left=(window.innerWidth/2+80)+"px";
no.style.top=(window.innerHeight/2+40)+"px";

function runAway(){
    const x=Math.random()*(window.innerWidth-no.offsetWidth);
    const y=Math.random()*(window.innerHeight-no.offsetHeight);

    no.style.left=x+"px";
    no.style.top=y+"px";

    size+=0.2;
    yes.style.transform=`scale(${size})`;
}

no.addEventListener("mouseenter",runAway);
no.addEventListener("touchstart",function(e){
    e.preventDefault();
    runAway();
});

yes.onclick=function(){
    document.body.innerHTML=`
    <div style="display:flex;justify-content:center;align-items:center;height:100vh;background:#ffe6f2;font-family:Arial;">
        <div style="text-align:center">
            <h1>🎉 YAY!! ❤️</h1>
            <h2>You just made my day! 🥹💕</h2>
        </div>
    </div>`;
};
</script>

</body>
</html>
