<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SV International Logistics</title>

<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial;background:#f4f6f8}
header{background:#0b3c5d;color:#fff;padding:15px;position:sticky;top:0}
nav{display:flex;justify-content:space-between;align-items:center}
nav a{color:#fff;text-decoration:none;margin:0 10px;font-weight:bold}

.hero{background:linear-gradient(rgba(0,0,0,.6),rgba(0,0,0,.6)),
url('https://images.unsplash.com/photo-1586528116311-ad8dd3c8310d');
background-size:cover;color:#fff;padding:100px 20px;text-align:center}

.section{padding:50px 20px;background:#fff}
h2{text-align:center;color:#0b3c5d}

.services{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:20px}
.card{background:#0b3c5d;color:#fff;padding:25px;border-radius:12px;text-align:center;cursor:pointer}
.card:hover{background:#08304a}

.calculator{display:none;max-width:600px;margin:40px auto;padding:25px;
background:#f9fbfd;border-radius:14px;box-shadow:0 8px 18px rgba(0,0,0,.15)}

input,button{width:100%;padding:12px;margin:8px 0;border-radius:6px;border:1px solid #ccc}
button{background:#0b3c5d;color:#fff;border:none;cursor:pointer}
button:hover{background:#08304a}

footer{background:#0b3c5d;color:#fff;text-align:center;padding:20px}
</style>
</head>

<body>

<header>
<nav>
<strong>SV International Logistics</strong>
<div>
<a href="#home">Home</a>
<a href="#services">Services</a>
</div>
</nav>
</header>

<section class="hero" id="home">
<h1>Courier & Freight Solutions</h1>
<p>Domestic • Express • Air Cargo • PTL</p>
</section>

<section class="section" id="services">
<h2>Our Services</h2>

<div class="services">
<div class="card" onclick="openCalc('domestic')">Domestic Courier</div>
<div class="card" onclick="openCalc('express')">Express</div>
<div class="card" onclick="openCalc('air')">Air Cargo</div>
<div class="card" onclick="openCalc('ptl')">Part Load (PTL)</div>
</div>

<div class="calculator" id="calculator">
<h3 id="calcTitle"></h3>

<h4>Route Details</h4>
<input id="fromPin" placeholder="From Pincode" maxlength="6" onblur="getPin('from')">
<input id="fromCity" placeholder="From City" readonly>
<input id="fromState" placeholder="From State" readonly>

<input id="toPin" placeholder="To Pincode" maxlength="6" onblur="getPin('to')">
<input id="toCity" placeholder="To City" readonly>
<input id="toState" placeholder="To State" readonly>

<input id="zone" placeholder="Zone (Auto)" readonly>

<h4>Shipment</h4>
<input id="weight" type="number" placeholder="Actual Weight (KG)">
<input id="l" type="number" placeholder="Length (CM)">
<input id="w" type="number" placeholder="Width (CM)">
<input id="h" type="number" placeholder="Height (CM)">

<button onclick="calculate()">Calculate Freight</button>
<div id="result"></div>
</div>
</section>

<footer>
© 2025 SV International Logistics
</footer>

<script>
let service='';

const zones={
NCR:['Delhi','Haryana'],
North:['Punjab','Rajasthan','Uttar Pradesh','Uttarakhand','Himachal Pradesh','Jammu and Kashmir','Chandigarh'],
West:['Maharashtra','Gujarat','Goa'],
South:['Tamil Nadu','Karnataka','Kerala','Telangana','Andhra Pradesh','Puducherry'],
East:['West Bengal','Odisha','Bihar','Assam','Jharkhand','Chhattisgarh','Tripura','Manipur','Meghalaya','Nagaland','Mizoram','Arunachal Pradesh','Sikkim']
};

function openCalc(t){
service=t;
calculator.style.display='block';
calcTitle.innerText=t.toUpperCase()+" FREIGHT";
window.scrollTo({top:calculator.offsetTop-50,behavior:'smooth'});
}

function findZone(state){
for(let z in zones){
if(zones[z].includes(state)) return z;
}
return 'Other';
}

function getPin(type){
let pin=document.getElementById(type+'Pin').value;
if(pin.length!==6) return;

fetch(`https://api.postalpincode.in/pincode/${pin}`)
.then(res=>res.json())
.then(data=>{
if(data[0].Status!=="Success"){alert("Invalid Pincode");return;}
let p=data[0].PostOffice[0];
document.getElementById(type+'City').value=p.District;
document.getElementById(type+'State').value=p.State;
zone.value=findZone(p.State);
});
}

function calculate(){
let wt=+weight.value||0;
let vol=(l.value*w.value*h.value)/5000;
let bill=Math.max(wt,vol);

let rateMap={
domestic:{NCR:40,North:45,West:55,South:50,East:60},
express:{NCR:150,North:160,West:180,South:170,East:190},
air:{Other:190},
ptl:{NCR:18,North:20,West:24,South:22,East:26}
};

if(service==='ptl' && bill<30){alert("Minimum 30 KG required");return;}

let z=zone.value;
let rate=rateMap[service][z] || rateMap[service]['Other'];
let amount=bill*rate;
let gst=amount*0.18;
let total=amount+gst;

result.innerHTML=`
<b>Chargeable Weight:</b> ${bill.toFixed(2)} KG<br>
<b>Base:</b> ₹${amount.toFixed(2)}<br>
<b>GST:</b> ₹${gst.toFixed(2)}<br>
<h3>Total: ₹${total.toFixed(2)}</h3>
`;

window.open("https://wa.me/918209490258","_blank");
}
</script>

</body>
</html>
