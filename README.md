<!DOCTYPE html>
<html lang="ms">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ixfan Barbershop</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Segoe UI',sans-serif;
}

body{
background:#111;
color:white;
}

.welcome{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
}

.logo{
font-size:90px;
margin-bottom:15px;
}

h1{
color:#d4af37;
font-size:55px;
margin-bottom:10px;
}

.tagline{
font-size:20px;
margin-bottom:30px;
color:#ddd;
}

.btn{
background:#d4af37;
color:black;
padding:15px 40px;
border:none;
border-radius:40px;
font-size:18px;
font-weight:bold;
cursor:pointer;
}

#potongan{
display:none;
padding:40px 20px;
text-align:center;
}

.card{
background:#1b1b1b;
max-width:450px;
margin:20px auto;
padding:25px;
border-radius:15px;
border:1px solid #333;
}

.card h2{
color:#d4af37;
margin-bottom:10px;
}

.card p{
margin-bottom:15px;
}

.result{
margin-top:30px;
padding:25px;
background:#1b1b1b;
max-width:500px;
margin-left:auto;
margin-right:auto;
border-radius:15px;
display:none;
}

.number{
font-size:60px;
color:#d4af37;
font-weight:bold;
}

.wait{
margin-top:10px;
font-size:22px;
}

</style>
</head>

<body>

<div class="welcome" id="welcome">

<div class="logo">💈</div>

<h1>IXFAN BARBERSHOP</h1>

<p class="tagline">
Selamat Datang Ke Ixfan Barbershop
</p>

<button class="btn" onclick="masuk()">
MASUK
</button>

</div>

<div id="potongan">

<h1>Pilih Potongan Rambut</h1>

<div class="card">
<h2>High Fade</h2>
<p>Potongan fade tinggi yang moden dan kemas.</p>
<button class="btn" onclick="ambilGiliran('High Fade')">
Pilih
</button>
</div>

<div class="card">
<h2>Mid Fade</h2>
<p>Potongan fade sederhana yang popular.</p>
<button class="btn" onclick="ambilGiliran('Mid Fade')">
Pilih
</button>
</div>

<div class="card">
<h2>Low Fade</h2>
<p>Potongan fade rendah yang profesional.</p>
<button class="btn" onclick="ambilGiliran('Low Fade')">
Pilih
</button>
</div>

<div class="result" id="result">

<h2>Potongan Dipilih</h2>

<p id="jenis"></p>

<p>Nombor Giliran Anda</p>

<div class="number" id="nombor"></div>

<div class="wait">
Sila tunggu sebentar...
</div>

</div>

</div>

<script>

let giliran = localStorage.getItem("ixfan_giliran");

if(!giliran){
giliran = 1;
}

function masuk(){

document.getElementById("welcome").style.display="none";
document.getElementById("potongan").style.display="block";

}

function ambilGiliran(style){

document.getElementById("jenis").innerHTML =
"<b>" + style + "</b>";

document.getElementById("nombor").innerHTML =
"#" + giliran;

document.getElementById("result").style.display="block";

giliran++;

localStorage.setItem("ixfan_giliran", giliran);

window.scrollTo({
top:document.body.scrollHeight,
behavior:'smooth'
});

}

</script>

</body>
</html>
