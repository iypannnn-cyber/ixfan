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
font-family:Arial, sans-serif;
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

h1{
font-size:60px;
color:#d4af37;
margin-bottom:20px;
}

p{
font-size:20px;
margin-bottom:30px;
}

button{
background:#d4af37;
color:black;
border:none;
padding:15px 35px;
font-size:18px;
font-weight:bold;
border-radius:30px;
cursor:pointer;
}

#menu{
display:none;
padding:50px 20px;
text-align:center;
}

.card{
background:#1a1a1a;
max-width:400px;
margin:20px auto;
padding:25px;
border-radius:15px;
border:1px solid #333;
}

.card h2{
color:#d4af37;
margin-bottom:10px;
}

.card button{
margin-top:15px;
}

#pilihan{
margin-top:30px;
font-size:24px;
color:#d4af37;
}

</style>

</head>

<body>

<section class="welcome" id="welcome">

<h1>IXFAN BARBERSHOP</h1>

<p>
Selamat Datang Ke Ixfan Barbershop
</p>

<button onclick="masukWebsite()">
SELAMAT DATANG
</button>

</section>

<section id="menu">

<h1>Pilih Potongan Rambut</h1>

<div class="card">
<h2>High Fade</h2>
<p>Potongan fade tinggi yang moden dan kemas.</p>
<button onclick="pilih('High Fade')">
Pilih High Fade
</button>
</div>

<div class="card">
<h2>Mid Fade</h2>
<p>Potongan fade sederhana yang popular.</p>
<button onclick="pilih('Mid Fade')">
Pilih Mid Fade
</button>
</div>

<div class="card">
<h2>Low Fade</h2>
<p>Potongan fade rendah yang kemas dan profesional.</p>
<button onclick="pilih('Low Fade')">
Pilih Low Fade
</button>
</div>

<div id="pilihan"></div>

</section>

<script>

function masukWebsite(){

document.getElementById("welcome").style.display="none";

document.getElementById("menu").style.display="block";

}

function pilih(style){

document.getElementById("pilihan").innerHTML=
"Anda memilih: <b>" + style + "</b>";

}

</script>

</body>
</html>

            Terima kasih kerana memilih Ixfan Barbershop.
            Kami menyediakan perkhidmatan gunting rambut
            yang kemas, moden dan profesional untuk semua pelanggan.
            Kepuasan anda adalah keutamaan kami.
        </p>
