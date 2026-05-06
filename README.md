<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>FitAI Ultimate Fitness Dashboard</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family: Arial, sans-serif;
    background:
    radial-gradient(circle at top,#1e293b,#020617 60%);
    color:white;
    overflow-x:hidden;
}

/* SCROLLBAR */

::-webkit-scrollbar{
    width:10px;
}

::-webkit-scrollbar-thumb{
    background:#00ffae;
    border-radius:10px;
}

/* NAVBAR */

nav{
    width:100%;
    padding:20px 7%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    position:sticky;
    top:0;
    z-index:1000;
    backdrop-filter: blur(12px);
    background:rgba(0,0,0,0.25);
}

.logo{
    font-size:32px;
    font-weight:bold;
}

.logo span{
    color:#00ffae;
}

nav ul{
    display:flex;
    gap:30px;
    list-style:none;
}

nav ul li{
    cursor:pointer;
    transition:0.3s;
}

nav ul li:hover{
    color:#00ffae;
}

/* HERO */

.hero{
    padding:70px 7%;
    display:grid;
    grid-template-columns:1fr 1fr;
    align-items:center;
    gap:50px;
}

.hero-text h1{
    font-size:65px;
    line-height:1.1;
    margin-bottom:20px;
}

.hero-text span{
    color:#00ffae;
}

.hero-text p{
    color:#cbd5e1;
    line-height:1.8;
    margin-bottom:30px;
}

.hero-buttons{
    display:flex;
    gap:15px;
}

.btn{
    padding:14px 28px;
    border:none;
    border-radius:14px;
    cursor:pointer;
    font-weight:bold;
    transition:0.3s;
}

.primary{
    background:#00ffae;
    color:black;
}

.primary:hover{
    transform:translateY(-4px);
}

.secondary{
    background:rgba(255,255,255,0.08);
    color:white;
    border:1px solid rgba(255,255,255,0.1);
}

.secondary:hover{
    background:rgba(255,255,255,0.12);
}

/* GLASS CARD */

.glass{
    background:rgba(255,255,255,0.06);
    backdrop-filter: blur(15px);
    border:1px solid rgba(255,255,255,0.08);
    border-radius:25px;
    box-shadow:0 0 30px rgba(0,0,0,0.4);
}

/* FITNESS FORM */

.dashboard{
    padding:30px;
}

.dashboard h2{
    text-align:center;
    margin-bottom:25px;
    font-size:32px;
}

.grid-2{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:15px;
}

.input-group{
    margin-bottom:15px;
}

label{
    display:block;
    margin-bottom:8px;
    color:#e2e8f0;
}

input,select{
    width:100%;
    padding:14px;
    border:none;
    border-radius:14px;
    background:rgba(255,255,255,0.08);
    color:white;
    outline:none;
}

input::placeholder{
    color:#cbd5e1;
}

.calculate-btn{
    width:100%;
    padding:16px;
    border:none;
    border-radius:14px;
    margin-top:10px;
    background:linear-gradient(135deg,#00ffae,#00b4ff);
    color:black;
    font-size:17px;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}

.calculate-btn:hover{
    transform:scale(1.02);
}

/* RESULT SECTION */

.results{
    display:none;
    margin-top:25px;
}

.result-card{
    padding:20px;
    margin-bottom:18px;
    border-radius:20px;
    background:rgba(255,255,255,0.05);
}

.result-card h3{
    color:#00ffae;
    margin-bottom:10px;
}

.big{
    font-size:42px;
    font-weight:bold;
}

.small{
    color:#cbd5e1;
    line-height:1.7;
}

/* PROGRESS BAR */

.progress-container{
    width:100%;
    height:20px;
    background:rgba(255,255,255,0.08);
    border-radius:30px;
    overflow:hidden;
    margin-top:15px;
}

.progress-bar{
    height:100%;
    width:0%;
    background:linear-gradient(90deg,#00ffae,#00b4ff);
    transition:1s;
}

/* FEATURE SECTION */

.section{
    padding:70px 7%;
}

.section-title{
    text-align:center;
    margin-bottom:45px;
}

.section-title h1{
    font-size:48px;
}

.features{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.feature-card{
    padding:25px;
    transition:0.3s;
}

.feature-card:hover{
    transform:translateY(-6px);
}

.feature-card h3{
    margin-bottom:15px;
    color:#00ffae;
}

/* WORKOUT PLANS */

.workout-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:25px;
}

.workout-card{
    padding:25px;
}

.workout-card h2{
    color:#00ffae;
    margin-bottom:15px;
}

/* FOOTER */

footer{
    text-align:center;
    padding:40px;
    color:#cbd5e1;
}

/* MOBILE */

@media(max-width:950px){

.hero{
    grid-template-columns:1fr;
}

.hero-text h1{
    font-size:46px;
}

nav ul{
    display:none;
}

}

</style>
</head>

<body>

<!-- NAVBAR -->

<nav>

<div class="logo">
Fit<span>AI</span>
</div>

<ul>
<li>Home</li>
<li>Dashboard</li>
<li>Workouts</li>
<li>Nutrition</li>
<li>Contact</li>
</ul>

</nav>

<!-- HERO -->

<section class="hero">

<div class="hero-text">

<h1>
Your Ultimate
<span>AI Fitness</span>
Dashboard
</h1>

<p>
Track calories burned, BMI, body health,
water intake, protein intake, metabolism,
fitness score, workout intensity and more —
all in one modern AI-powered dashboard.
</p>

<div class="hero-buttons">

<button class="btn primary">
Start Tracking
</button>

<button class="btn secondary">
Explore Features
</button>

</div>

</div>

<!-- DASHBOARD -->

<div class="glass dashboard">

<h2>
🔥 Fitness Calculator
</h2>

<div class="grid-2">

<div class="input-group">
<label>Age</label>
<input type="number" id="age" placeholder="Enter age">
</div>

<div class="input-group">
<label>Weight (kg)</label>
<input type="number" id="weight" placeholder="Enter weight">
</div>

</div>

<div class="grid-2">

<div class="input-group">
<label>Height (cm)</label>
<input type="number" id="height" placeholder="Enter height">
</div>

<div class="input-group">
<label>Heart Rate</label>
<input type="number" id="hr" placeholder="Heart rate">
</div>

</div>

<div class="grid-2">

<div class="input-group">
<label>Workout Duration</label>
<input type="number" id="duration" placeholder="Minutes">
</div>

<div class="input-group">
<label>Gender</label>

<select id="gender">
<option value="male">Male</option>
<option value="female">Female</option>
</select>

</div>

</div>

<div class="grid-2">

<div class="input-group">
<label>Workout Intensity</label>

<select id="activity">
<option value="5">Light Exercise</option>
<option value="8">Moderate Workout</option>
<option value="10">Intense Workout</option>
<option value="12">Athlete Level</option>
</select>

</div>

<div class="input-group">
<label>Fitness Goal</label>

<select id="goal">
<option value="cut">Fat Loss</option>
<option value="maintain">Maintain</option>
<option value="bulk">Muscle Gain</option>
</select>

</div>

</div>

<button class="calculate-btn" onclick="calculateAll()">
Calculate Full Fitness Report
</button>

<!-- RESULTS -->

<div class="results" id="results">

<div class="result-card">
<h3>🔥 Calories Burned</h3>
<div class="big" id="calories">0</div>
</div>

<div class="result-card">
<h3>📊 BMI & Body Status</h3>
<div class="big" id="bmi">0</div>
<p class="small" id="bmiText"></p>
</div>

<div class="result-card">
<h3>⚡ Daily Metabolism</h3>
<p class="small" id="metabolism"></p>
</div>

<div class="result-card">
<h3>💪 Protein Intake</h3>
<p class="small" id="protein"></p>
</div>

<div class="result-card">
<h3>💧 Water Intake</h3>
<p class="small" id="water"></p>
</div>

<div class="result-card">
<h3>🏋️ Workout Recommendation</h3>
<p class="small" id="workout"></p>
</div>

<div class="result-card">
<h3>🧠 AI Health Tips</h3>
<p class="small" id="tips"></p>
</div>

<div class="result-card">
<h3>📈 Fitness Score</h3>

<div class="progress-container">
<div class="progress-bar" id="progress"></div>
</div>

<p class="small" id="scoreText"></p>

</div>

</div>

</div>

</section>

<!-- FEATURES -->

<section class="section">

<div class="section-title">
<h1>Powerful Features</h1>
</div>

<div class="features">

<div class="glass feature-card">
<h3>🔥 AI Calorie Prediction</h3>
<p>
Estimate calories using workout intensity,
heart rate and body metrics.
</p>
</div>

<div class="glass feature-card">
<h3>📊 BMI Analytics</h3>
<p>
Analyze body composition and health status instantly.
</p>
</div>

<div class="glass feature-card">
<h3>⚡ Metabolism Tracking</h3>
<p>
Calculate estimated BMR and calorie maintenance.
</p>
</div>

<div class="glass feature-card">
<h3>💧 Smart Hydration</h3>
<p>
Get personalized water intake recommendations.
</p>
</div>

<div class="glass feature-card">
<h3>🏋️ Workout Suggestions</h3>
<p>
Receive custom exercise recommendations instantly.
</p>
</div>

<div class="glass feature-card">
<h3>📱 Fully Responsive</h3>
<p>
Works perfectly on mobile, tablet and desktop.
</p>
</div>

</div>

</section>

<!-- WORKOUT PLANS -->

<section class="section">

<div class="section-title">
<h1>Workout Plans</h1>
</div>

<div class="workout-grid">

<div class="glass workout-card">
<h2>🔥 Fat Loss</h2>
<p>
• 30–45 min cardio<br>
• High protein diet<br>
• Calorie deficit<br>
• 8k–10k daily steps
</p>
</div>

<div class="glass workout-card">
<h2>💪 Muscle Gain</h2>
<p>
• Heavy strength training<br>
• Progressive overload<br>
• High protein intake<br>
• Proper sleep & recovery
</p>
</div>

<div class="glass workout-card">
<h2>⚡ Athlete Training</h2>
<p>
• Explosive workouts<br>
• HIIT training<br>
• Advanced endurance<br>
• Recovery optimization
</p>
</div>

<div class="glass workout-card">
<h2>⚡ Strength Training</h2>
<p>
• Increases muscle mass<br>
• Improve Bone Density<br>
• Boosts Metabolism<br>
• Helps in Fatloss
<p>
<div>

</section>

<footer>
© 2026 FitAI • Ultimate Fitness Dashboard
</footer>

<script>

function calculateAll(){

let age = parseInt(document.getElementById("age").value);
let weight = parseFloat(document.getElementById("weight").value);
let height = parseFloat(document.getElementById("height").value);
let hr = parseInt(document.getElementById("hr").value);
let duration = parseInt(document.getElementById("duration").value);
let gender = document.getElementById("gender").value;
let activity = parseFloat(document.getElementById("activity").value);
let goal = document.getElementById("goal").value;

if(!age || !weight || !height || !hr || !duration){

alert("Please fill all fields");
return;

}

/* Calories */

let calories;

if(gender === "male"){

calories =
((age * 0.2017)
- (weight * 0.09036)
+ (hr * 0.6309)
- 55.0969)
* duration / 4.184;

}

else{

calories =
((age * 0.074)
- (weight * 0.05741)
+ (hr * 0.4472)
- 20.4022)
* duration / 4.184;

}

calories = calories * (activity / 8);

/* BMI */

let bmi =
weight /
((height / 100) * (height / 100));

let bmiStatus = "";
let bmiAdvice = "";
let score = 0;

if(bmi < 18.5){

bmiStatus = "Underweight";
bmiAdvice = "Increase nutrition & strength training.";
score = 45;

}

else if(bmi < 25){

bmiStatus = "Normal";
bmiAdvice = "Excellent body composition.";
score = 90;

}

else if(bmi < 30){

bmiStatus = "Overweight";
bmiAdvice = "Focus on cardio and calorie control.";
score = 65;

}

else{

bmiStatus = "Obese";
bmiAdvice = "Improve activity and nutrition consistency.";
score = 35;

}

/* BMR */

let bmr;

if(gender === "male"){

bmr =
10 * weight +
6.25 * height -
5 * age + 5;

}

else{

bmr =
10 * weight +
6.25 * height -
5 * age - 161;

}

/* Protein */

let protein;

if(goal === "bulk") protein = weight * 2.2;
else if(goal === "cut") protein = weight * 1.8;
else protein = weight * 1.6;

/* Water */

let water = weight * 0.035;

/* Workout */

let workoutText = "";

if(goal === "bulk"){

workoutText =
"Focus on heavy compound lifts, progressive overload and recovery.";

}

else if(goal === "cut"){

workoutText =
"Add cardio, maintain protein intake and stay in calorie deficit.";

}

else{

workoutText =
"Maintain balanced workouts with strength and cardio.";

}

/* Tips */

let tips =
"Sleep 7–8 hours, stay hydrated, train consistently and maintain high protein intake for best recovery.";

/* SHOW RESULTS */

document.getElementById("results").style.display = "block";

document.getElementById("calories").innerHTML =
Math.round(calories) + " kcal";

document.getElementById("bmi").innerHTML =
bmi.toFixed(1);

document.getElementById("bmiText").innerHTML =
bmiStatus + " • " + bmiAdvice;

document.getElementById("metabolism").innerHTML =
"Estimated BMR: <b>" +
Math.round(bmr) +
" kcal/day</b>";
document.getElementById("protein").innerHTML =
"Recommended protein intake: <b>" +
Math.round(protein) +
"g/day</b>";

document.getElementById("water").innerHTML =
"Recommended water intake: <b>" +
water.toFixed(1) +
" liters/day</b>";

document.getElementById("workout").innerHTML =
workoutText;

document.getElementById("tips").innerHTML =
tips;

document.getElementById("progress").style.width =
score + "%";

document.getElementById("scoreText").innerHTML =
"Fitness Score: <b>" + score + "/100</b>";

}

</script>

</body>
</html>
