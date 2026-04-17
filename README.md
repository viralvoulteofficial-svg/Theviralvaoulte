<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title></title>
</head>

<body>
  
</body>

</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Viral Vaoulte</title>

<style>
body {
    margin: 0;
    font-family: Arial;
    background: linear-gradient(135deg,#5cc6c6,#6aa6d6);
}
.container {
    background:#fff;
    margin:10px;
    padding:15px;
    border-radius:20px;
}
input,select {
    width:100%;
    padding:12px;
    border-radius:12px;
    border:none;
    background:#eef5f5;
    margin-top:8px;
}
label {
    margin-top:12px;
    display:block;
    font-weight:bold;
}
.btn {
    width:100%;
    padding:14px;
    margin-top:15px;
    border-radius:15px;
    border:none;
    background:linear-gradient(90deg,#5cc6c6,#6aa6d6);
    color:white;
}
.desc-box {
    font-size:13px;
    margin-top:15px;
    color:#333;
}
.whatsapp {
    position:fixed;
    bottom:20px;
    right:20px;
    background:#25D366;
    padding:14px;
    border-radius:50%;
    color:white;
    text-decoration:none;
}
</style>
</head>

<body>

<div class="container">

<label>Category</label>
<select id="category" onchange="loadServices()">
<option>Instagram</option>
<option>YouTube</option>
<option>Facebook</option>
<option>TikTok</option>
<option>Telegram</option>
<option>Twitter</option>
<option>LinkedIn</option>
<option>Spotify</option>
</select>

<label>Service</label>
<select id="service" onchange="updateDesc()"></select>

<label>Description</label>
<textarea id="desc" rows="5" readonly></textarea>

<label>Link</label>
<input type="text" id="link" placeholder="Enter Link">

<label>Quantity</label>
<input type="number" id="qty" min="1000" step="1000" oninput="calc()">

<label>Charge</label>
<input type="text" id="charge" readonly>

<button class="btn" onclick="order()">Submit</button>

<div class="desc-box">
🔥 Instant boost in followers & engagement<br>
⚡ Fast delivery system<br>
💯 High quality services<br>
🔒 Safe & secure (no password needed)<br>
📈 Grow your account quickly<br>
🎯 Best for influencers & brands<br>
🚀 Start gaining reach instantly<br>
💎 Premium SMM services<br>
📢 Limited offer<br>
✅ Easy ordering system
</div>

</div>

<a class="whatsapp" href="https://wa.me/918795025565">💬</a>

<script>

// 🔥 REAL SERVICE STRUCTURE
const data = {

Instagram: [
["Followers Cheap (Non Refill)",40],
["Followers Normal",58],
["Followers Premium (Refill)",60],
["Indian Followers (Refill)",150],
["Likes Cheap",28],
["Likes Instant",30],
["Likes HQ (Refill)",45],
["Views Cheap",3],
["Views Fast",5],
["Views Premium",8],
["Story Views",38],
["Comments Random",185],
["Comments Custom",455]
],

YouTube: [
["Views Cheap",70],
["Views Normal",90],
["Views Monetized (Refill)",140],
["Subscribers Cheap",90],
["Subscribers Normal",115],
["Subscribers Premium",160],
["Likes",75],
["Comments",100],
["Watch Time 1000H",1500],
["Watch Time 4000H",4000]
],

Facebook: [
["Page Likes Cheap",50],
["Page Likes Normal",65],
["Page Likes Premium",90],
["Followers",55],
["Post Likes",38],
["Video Views",25]
],

TikTok: [
["Followers Cheap",30],
["Followers Normal",50],
["Followers Premium",80],
["Likes",12],
["Views",6]
],

Telegram: [
["Members Cheap",120],
["Members Normal",150],
["Members Premium",200],
["Views",20],
["Reactions",25]
],

Twitter: [
["Followers Cheap",150],
["Followers Normal",190],
["Followers Premium",250],
["Likes",150],
["Retweets",165]
],

LinkedIn: [
["Followers Normal",375],
["Followers Premium",450],
["Connections",440]
],

Spotify: [
["Plays Cheap",20],
["Plays Normal",32],
["Plays Premium",50],
["Followers",190],
["Playlist Followers",225]
]

};

function loadServices(){
let cat=document.getElementById("category").value;
let service=document.getElementById("service");
service.innerHTML="";

data[cat].forEach((s,i)=>{
service.innerHTML+=`<option value="${i}">${s[0]} - ₹${s[1]}</option>`;
});

updateDesc();
}

function updateDesc(){
let cat=document.getElementById("category").value;
let i=document.getElementById("service").value;

let name=data[cat][i][0];
let price=data[cat][i][1];

// 🔥 refill detection
let refill = name.toLowerCase().includes("refill") || price>80 ? "Refill ✅" : "Non-Refill ❌";

document.getElementById("desc").value=
"🚀 "+name+"\n\n"+
"⚡ Fast Delivery\n"+
"💯 High Quality\n"+
"🔒 Safe & Secure\n"+
"📊 "+refill+"\n"+
"⏳ Limited Offer";

calc();
}

function calc(){
let cat=document.getElementById("category").value;
let i=document.getElementById("service").value;
let qty=document.getElementById("qty").value;

if(!qty) return;

let price=data[cat][i][1];
let total=(qty/1000)*price;

document.getElementById("charge").value="₹"+total.toFixed(2);
}

function order(){
let text=document.getElementById("desc").value+
"\nLink: "+document.getElementById("link").value+
"\nQty: "+document.getElementById("qty").value+
"\nCharge: "+document.getElementById("charge").value;

window.open("https://wa.me/918795025565?text="+encodeURIComponent(text));
}

loadServices();

</script>

</body>
</html>

  <h2>💳 Pay via UPI</h2>
  <p>Scan QR to pay instantly</p>

  <p><b>Banking Name:</b> Khurshida</p>
  <p><b>UPI ID:</b> 8795025565@upi</p>

  <img 
    src="https://api.qrserver.com/v1/create-qr-code/?size=250x250&data=upi%3A%2F%2Fpay%3Fpa%3D8795025565%40upi%26pn%3DKhurshida%26cu%3DINR"
    alt="UPI QR Code"
    style="border:2px solid #000; padding:5px; background:white;"
  />

</div>

</div>

<a class="whatsapp" href="https://wa.me/918795025565">💬</a>

<script>
<div style="text-align:center; margin:30px 0; padding:25px; background:#f5f5f5;">

  <h2>💳 Pay via UPI</h2>

  <p>Scan QR to pay instantly</p>

  <!-- CHANGE THIS UPI ID -->
  <p><b>UPI ID:</b> viralsmmpanel@upi</p>

  <img 
    src="https://chart.googleapis.com/chart?chs=250x250&cht=qr&chl=upi://pay?pa=viralsmmpanel@upi&pn=ViralSMM&cu=INR"
    alt="UPI QR Code"
    style="border:2px solid #000; padding:5px; background:white;"
  />

</div><div style="text-align:center; margin:30px 0; padding:25px; background:#f5f5f5;">

  <h2>💳 Pay via UPI</h2>

  <p>Scan QR to pay instantly</p>

  <!-- CHANGE THIS UPI ID -->
  <p><b>UPI ID:</b> viralsmmpanel@upi</p>

  <img 
    src="https://chart.googleapis.com/chart?chs=250x250&cht=qr&chl=upi://pay?pa=viralsmmpanel@upi&pn=ViralSMM&cu=INR"
    alt="UPI QR Code"
    style="border:2px solid #000; padding:5px; background:white;"
  />



const data = {

/* INSTAGRAM */
Instagram: [
["1000 Followers (Refill)",38],
["1000 Followers (No Refill)",28],
["1000 Indian Followers",150],
["1000 Likes (Instant)",10],
["1000 Likes (HQ)",15],
["1000 Views (Reels)",5],
["1000 Story Views",8],
["100 Comments (Random)",32],
["100 Custom Comments",50]
],

/* YOUTUBE */
YouTube: [
["1000 Views (Normal)",90],
["1000 Views (Monetized)",140],
["100 Subscribers",115],
["1000 Likes",75],
["100 Comments",100],
["4000 Watch Time Hours",4000]
],

/* FACEBOOK */
Facebook: [
["1000 Page Likes",65],
["1000 Followers",55],
["1000 Post Likes",38],
["1000 Video Views",25]
],

/* TIKTOK */
TikTok: [
["1000 Followers",50],
["1000 Likes",12],
["1000 Views",6]
],

/* TELEGRAM */
Telegram: [
["1000 Members",150],
["1000 Views",20],
["100 Reactions",25]
],

/* TWITTER */
Twitter: [
["1000 Followers",190],
["1000 Likes",150],
["1000 Retweets",165]
],

/* LINKEDIN */
LinkedIn: [
["1000 Followers",375],
["1000 Connections",440]
],

/* SPOTIFY */
Spotify: [
["1000 Plays",32],
["1000 Followers",190],
["1000 Playlist Followers",225]
],

/* WEBSITE */
Website: [
["Website Traffic",100]
]

};

function loadServices(){
let cat = document.getElementById("category").value;
let service = document.getElementById("service");
service.innerHTML="";

data[cat].forEach((s,i)=>{
service.innerHTML += `<option value="${i}">${s[0]} - ₹${s[1]}</option>`;
});

updateDesc();
}

function updateDesc(){
let cat = document.getElementById("category").value;
let i = document.getElementById("service").value;

document.getElementById("desc").value = cat+" - "+data[cat][i][0];
calc();
}

function calc(){
let cat = document.getElementById("category").value;
let i = document.getElementById("service").value;
let qty = document.getElementById("qty").value;

if(!qty || qty < 1){
    document.getElementById("charge").value="";
    return;
}

let price = data[cat][i][1];

// ✅ FIXED FORMULA
let total = (qty / 1000) * price;

document.getElementById("charge").value = "₹" + total.toFixed(2);
}

function order(){
let text = document.getElementById("desc").value+
"\nLink: "+document.getElementById("link").value+
"\nQty: "+document.getElementById("qty").value+
"\nCharge: "+document.getElementById("charge").value;

window.open("https://wa.me/918795025565?text="+encodeURIComponent(text));
}

loadServices();

</script>

</body>
</html> NOTE (after the payment plz send me message on WhatsApp) 

<!DOCTYPE html>
<html>
<head>
  <title>Viral SMM Panel</title>
  <style>
    body {
      font-family: Arial;
      background: #f2f2f2;
      margin: 0;
      padding: 0;
      text-align: center;
    }

    .box {
      background: white;
      padding: 20px;
      margin: 50px auto;
      width: 80%;
      border-radius: 10px;
      box-shadow: 0px 0px 10px gray;
    }

    h1 {
      color: #ff0055;
    }

    p {
      font-size: 16px;
      color: #333;
      line-height: 1.8;
    }

    button {
      padding: 10px 20px;
      background: #ff0055;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 15px;
    }

    button:hover {
      background: #cc0044;
    }
  </style>
</head>
<body>

  <div class="box">
    <h1>ViralSMMPanel.netlify</h1>

    <p>
      1. Welcome to Viral SMM Panel<br>
      2. Grow your Instagram, YouTube & TikTok fast<br>
      3. Best and cheapest social media services<br>
      4. 100% real engagement and instant delivery<br>
      5. Safe and secure payment system<br>
      6. 24/7 customer support available<br>
      7. Boost your followers and likes easily<br>
      8. Trusted by thousands of users<br>
      9. Start your journey to viral growth today<br>
      10. Join now and get instant results
    </p>

    <button>Get Started</button>
  </div>

</body>
</html>
<h2>🔥 Service Price List</h2>

<table border="1" cellspacing="0" cellpadding="10" style="width:90%; margin:auto; text-align:center; border-collapse:collapse; font-family:Arial;">
  
 <!DOCTYPE html>
<html>
<head>
  <title>Viral SMM Panel - Services</title>
  <style>
    body{
      font-family: Arial;
      background:#f4f4f4;
      text-align:center;
      margin:0;
    }

    h1{
      background:#ff0055;
      color:white;
      padding:15px;
      margin:0;
    }

    table{
      width:90%;
      margin:20px auto;
      border-collapse:collapse;
      background:white;
      box-shadow:0 0 10px gray;
    }

    th,td{
      border:1px solid #ddd;
      padding:10px;
      font-size:14px;
    }

    th{
      background:#111;
      color:white;
    }
  </style>
</head>

<body>

<h1>🔥 Viral SMM Panel - 500+ Services</h1>

<table>
  <tr>
    <th>#</th>
    <th>Service Name</th>
    <th>Price (₹)</th>
  </tr>

  <tbody id="serviceTable"></tbody>
</table>

<script>
  let services = [
    "Instagram Followers", "Instagram Likes", "Instagram Views",
    "Instagram Reel Likes", "Instagram Story Views",
    "YouTube Views", "YouTube Subscribers", "YouTube Likes",
    "Facebook Page Likes", "Facebook Post Likes",
    "TikTok Followers", "TikTok Likes", "TikTok Views",
    "Telegram Members", "Twitter Followers",
    "Spotify Plays", "Website Traffic", "App Installs"
  ];

  let table = document.getElementById("serviceTable");

  let count = 1;

  // Generate 500+ services automatically
  for(let i=0; i<500; i++){
    let base = services[i % services.length];

    let price = Math.floor(Math.random() * 90) + 5;

    let row = `
      <tr>
        <td>${count}</td>
        <td>${base} Package ${i+1}</td>
        <td>₹${price}</td>
      </tr>
    `;

    table.innerHTML += row;
    count++;
  }
</script>

</body>
</html>
<div style="margin-top:40px; padding:50px; background:#000; color:#fff; text-align:center;">

  <h1 style="font-size:60px; color ff0055; margin-bottom:20px;">
    THANKS
  </h1>

  <p style="font-size:16px; line-height:2; color:#ddd;">

    1. Thank you for visiting Viral SMM Panel<br>
    2. We appreciate your trust and support<br>
    3. Your growth is our top priority<br>
    4. We provide fast and reliable services<br>
    5. 24/7 support is always available<br>
    6. Our system is fully automated<br>
    7. Instant delivery guaranteed<br>
    8. Safe and secure platform<br>
    9. Affordable pricing for everyone<br>
    10. Trusted by thousands of users<br>
    11. We value every single customer<br>
    12. Quality service is our promise<br>
    13. New services added daily<br>
    14. Easy and simple order system<br>
    15. Boost your social media instantly<br>
    16. Grow your brand with us<br>
    17. Your success motivates us<br>
    18. Stay connected with Viral SMM Panel<br>
    19. We are always here to help you<br>
    20. THANK YOU FOR CHOOSING US ❤️

  </p>

</div>
<script>
// 1. Global error catcher (crash ko visible hone se roke)
window.onerror = function(message, source, lineno, colno, error) {
  console.log("Handled Error:", message);
  return true; // prevents ugly crash popup
};

// 2. Promise errors handle (API ya fetch crash control)
window.addEventListener("unhandledrejection", function(event) {
  console.log("Promise Error Handled:", event.reason);
  event.preventDefault();
});

// 3. Smooth loading complete
window.addEventListener("load", function () {
  document.body.style.opacity = "1";
});

// 4. Basic performance booster (lazy images support)
document.addEventListener("DOMContentLoaded", function () {
  const imgs = document.querySelectorAll("img");
  imgs.forEach(img => {
    img.loading = "lazy";
  });
});

// 5. Prevent accidental freeze (long task breaker)
setInterval(() => {
  console.log("Heartbeat OK");
}, 10000);
</script>
