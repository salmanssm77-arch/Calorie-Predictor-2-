<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>AI Fitness & Calorie Tracker</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family: Arial, sans-serif;
    background:
    radial-gradient(circle at top left,#1f4d68,#0f172a 35%),
    radial-gradient(circle at bottom right,#1b4332,#081018 45%);
    color:white;
    min-height:100vh;
    overflow-x:hidden;
}

/* NAVBAR */

nav{
    width:100%;
    padding:20px 8%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    backdrop-filter: blur(10px);
    position:sticky;
    top:0;
    z-index:1000;
    background:rgba(0,0,0,0.2);
}

.logo{
    font-size:28px;
    font-weight:bold;
    letter-spacing:1px;
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
    width:100%;
    padding:70px 8%;
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:40px;
    align-items:center;
}

.hero-text h1{
    font-size:58px;
    line-height:1.1;
    margin-bottom:20px;
}

.hero-text h1 span{
    color:#00ffae;
}

.hero-text p{
    color:#d1d5db;
    line-height:1.7;
    margin-bottom:30px;
}

.hero-btns{
    display:flex;
    gap:15px;
}

.btn{
    padding:14px 24px;
    border:none;
    border-radius:12px;
    cursor:pointer;
    font-weight:bold;
    transition:0.3s;
}

.primary{
    background:#00ffae;
    color:black;
}

.primary:hover{
    transform:translateY(-3px);
}

.secondary{
    background:rgba(255,255,255,0.08);
    color:white;
    border:1px solid rgba(255,255,255,0.15);
}

.secondary:hover{
    background:rgba(255,255,255,0.12);
}

/* GLASS CARD */

.glass{
    background:rgba(255,255,255,0.07);
    border:1px solid rgba(255,255,255,0.08);
    backdrop-filter: blur(15px);
    border-radius:24px;
    box-shadow:0 0 30px rgba(0,0,0,0.35);
}

/* FORM SECTION */

.predictor{
    padding:25px;
}

.predictor h2{
    margin-bottom:20px;
    text-align:center;
    font-size:28px;
}

.input-group{
    margin-bottom:15px;
}

label{
    display:block;
    margin-bottom:8px;
    color:#e5e7eb;
}

input,select{
    width:100%;
    padding:14px;
    border:none;
    outline:none;
    border-radius:12px;
    background:rgba(255,255,255,0.08);
    color:white;
    font-size:15px;
}

input::placeholder{
    color:#d1d5db;
}

.grid-2{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:15px;
}

.calculate-btn{
    width:100%;
    margin-top:10px;
    padding:15px;
    border:none;
    border-radius:14px;
    background:linear-gradient(135deg,#00ffae,#00c3ff);
    color:black;
    font-size:17px;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}

.calculate-btn:hover{
    transform:scale(1.02);
}

/* RESULT */

.result{
    margin-top:25px;
    display:none;
}

.result-card{
    padding:20px;
    border-radius:20px;
    margin-bottom:15px;
    background:rgba(255,255,255,0.06);
}

.result-card h3{
    margin-bottom:10px;
    color:#00ffae;
}

.big-number{
    font-size:42px;
    font-weight:bold;
}

.small{
    color:#cbd5e1;
    line-height:1.6;
}

/* STATS SECTION */

.stats{
    padding:30px 8%;
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:20px;
}

.stat-box{
    padding:25px;
    text-align:center;
}

.stat-box h2{
    color:#00ffae;
    margin-bottom:10px;
    font-size:40px;
}

/* FEATURES */

.features{
    padding:50px 8%;
}

.section-title{
    text-align:center;
    margin-bottom:40px;
}

.section-title h1{
    font-size:42px;
}

.feature-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.feature-card{
    padding:25px;
    transition:0.3s;
}

.feature-card:hover{
    transform:translateY(-5px);
}

.feature-card h3{
    margin-bottom:15px;
    color:#00ffae;
}

/* FOOTER */

footer{
    text-align:center;
    padding:30px;
    color:#cbd5e1;
}

/* MOBILE */

@media(max-width:900px){

.hero{
    grid-template-columns:1fr;
}

.hero-text h1{
    font-size:42px;
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
    <div class="logo">Fit<span>AI</span></div>

    <ul>
        <li>Home</li>
        <li>Calculator</li>
        <li>Fitness</li>
        <li>Nutrition</li>
        <li>About</li>
    </ul>
</nav>

<!-- HERO -->

<section class="hero">

<div class="hero-text">

    <h1>
        Smart AI Based
        <span>Calorie Tracker</span>
    </h1>

    <p>
        Track calories burned, calculate BMI,
        estimate protein intake, water intake,
        and improve your fitness using smart
        body analytics.
    </p>

    <div class="hero-btns">
        <button class="btn primary">Get Started</button>
        <button class="btn secondary">Learn More</button>
    </div>

</div>

<!-- CALCULATOR -->

<div class="glass predictor">

    <h2>🔥 Fitness Calculator</h2>

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

    <div class="input-group">

        <label>Workout Intensity</label>

        <select id="activity">
            <option value="5">Light Exercise</option>
            <option value="8">Moderate Workout</option>
            <option value="10">Intense Workout</option>
            <option value="12">Athlete Level</option>
        </select>

    </div>

    <button class="calculate-btn" onclick="calculateFitness()">
        Calculate Fitness Stats
    </button>

    <!-- RESULT -->

    <div class="result" id="result">

        <div class="result-card">
            <h3>🔥 Calories Burned</h3>
            <div class="big-number" id="caloriesResult">0</div>
        </div>

        <div class="result-card">
            <h3>📊 BMI Status</h3>
            <div class="big-number" id="bmiResult">0</div>
            <p class="small" id="bmiText"></p>
        </div>

        <div class="result-card">
            <h3>💪 Protein Recommendation</h3>
            <p class="small" id="proteinResult"></p>
        </div>

        <div class="result-card">
            <h3>💧 Daily Water Intake</h3>
            <p class="small" id="waterResult"></p>
        </div>

        <div class="result-card">
            <h3>🧠 Fitness Advice</h3>
            <p class="small" id="tips"></p>
        </div>

    </div>

</div>

</section>

<!-- STATS -->

<section class="stats">

<div class="glass stat-box">
    <h2>98%</h2>
    <p>User Satisfaction</p>
</div>

<div class="glass stat-box">
    <h2>24/7</h2>
    <p>Fitness Tracking</p>
</div>

<div class="glass stat-box">
    <h2>AI</h2>
    <p>Smart Predictions</p>
</div>

<div class="glass stat-box">
    <h2>100+</h2>
    <p>Workout Combinations</p>
</div>

</section>

<!-- FEATURES -->

<section class="features">

<div class="section-title">
    <h1>Why Choose FitAI?</h1>
</div>

<div class="feature-grid">

<div class="glass feature-card">
    <h3>🔥 Smart Calorie Analysis</h3>
    <p>
        Calculate calories burned based on body metrics,
        duration and exercise intensity.
    </p>
</div>

<div class="glass feature-card">
    <h3>📊 BMI & Health Tracking</h3>
    <p>
        Get instant BMI analysis and body health status.
    </p>
</div>

<div class="glass feature-card">
    <h3>💪 Fitness Recommendations</h3>
    <p>
        Receive workout and nutrition advice instantly.
    </p>
</div>

<div class="glass feature-card">
    <h3>⚡ Fast & Responsive</h3>
    <p>
        Optimized for desktop, tablet and mobile devices.
    </p>
</div>

</div>

</section>

<footer>
    © 2026 FitAI • Advanced Fitness Analytics Platform
</footer>

<script>

function calculateFitness(){

    let age = parseInt(document.getElementById("age").value);
    let weight = parseFloat(document.getElementById("weight").value);
    let height = parseFloat(document.getElementById("height").value);
    let hr = parseInt(document.getElementById("hr").value);
    let duration = parseInt(document.getElementById("duration").value);
    let gender = document.getElementById("gender").value;
    let activity = parseFloat(document.getElementById("activity").value);

    if(!age || !weight || !height || !hr || !duration){
        alert("Please fill all fields.");
        return;
    }

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

    // BMI

    let bmi =
    weight /
    ((height / 100) * (height / 100));

    let bmiStatus = "";
    let bmiAdvice = "";

    if(bmi < 18.5){

        bmiStatus = "Underweight";
        bmiAdvice = "Increase calorie intake and strength training.";

    }

    else if(bmi < 25){

        bmiStatus = "Normal";
        bmiAdvice = "Great shape! Maintain your routine.";

    }

    else if(bmi < 30){

        bmiStatus = "Overweight";
        bmiAdvice = "Add more cardio and improve diet quality.";

    }

    else{

        bmiStatus = "Obese";
        bmiAdvice = "Focus on gradual fat loss and consistency.";

    }

    // Protein

    let protein = (weight * 1.8).toFixed(0);

    // Water

    let water = (weight * 0.035).toFixed(1);

    // Show results

    document.getElementById("result").style.display = "block";

    document.getElementById("caloriesResult").innerHTML =
    Math.round(calories) + " kcal";

    document.getElementById("bmiResult").innerHTML =
    bmi.toFixed(1);

    document.getElementById("bmiText").innerHTML =
    bmiStatus + " • " + bmiAdvice;

    document.getElementById("proteinResult").innerHTML =
    "Recommended protein intake: <b>" +
    protein +
    "g/day</b>";

    document.getElementById("waterResult").innerHTML =
    "Recommended water intake: <b>" +
    water +
    " Liters/day</b>";

    document.getElementById("tips").innerHTML =
    "Train consistently, sleep 7–8 hours, maintain protein intake and stay hydrated for better recovery and muscle growth.";

}

</script>

</body>
</html>
