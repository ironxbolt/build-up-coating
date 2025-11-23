Made By Archit Badyal
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;

    /* Tablet pharma background */
    background: 
        linear-gradient(rgba(255,255,255,0.65), rgba(255,255,255,0.65)),
        url('https://i.imgur.com/j2wQd3M.jpg'); /* pharma coating image */

    background-size: cover;
    background-position: center;
    background-attachment: fixed;
}
background: 
    linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)),
    url('https://i.imgur.com/j2wQd3M.jpg');
background:
    linear-gradient(rgba(255,255,255,0.6), rgba(255,255,255,0.6)),
    url('https://i.imgur.com/0B6o2jY.jpeg');


<html>
<head>
    <title>Pharma Tablet Coating Calculator</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background: #eef2f7;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 65%;
            margin: auto;
            background: #fff;
            padding: 25px;
            margin-top: 40px;
            border-radius: 12px;
            box-shadow: 0 0 15px rgba(0,0,0,0.15);
        }
        h2 {
            text-align: center;
            color: #0d47a1;
            margin-bottom: 20px;
        }
        .section-title {
            background: #1565c0;
            color: white;
            padding: 12px;
            border-radius: 8px;
            margin-bottom: 20px;
            font-size: 20px;
        }
        .input-group {
            margin-bottom: 15px;
        }
        label {
            font-weight: bold;
            display: block;
            margin-bottom: 5px;
        }
        input {
            width: 100%;
            padding: 12px;
            border-radius: 6px;
            border: 1px solid #ccc;
            font-size: 16px;
        }
        button {
            width: 100%;
            padding: 14px;
            background: #0d47a1;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background: #08306b;
        }
        .result-box {
            margin-top: 20px;
            padding: 15px;
            background: #e3f2fd;
            border-left: 6px solid #0d47a1;
            border-radius: 6px;
            font-size: 18px;
        }
    </style>
</head>
<body>

<div class="container">

    <h2>Pharma Tablet Coating – Build-Up Calculator</h2>

    <div class="section-title">Section: Check Build During Spraying</div>

    <div class="input-group">
        <label>Reading of Prewarming Tablets (mg/tablet):</label>
        <input type="number" id="prewarm" step="0.01">
    </div>

    <div class="input-group">
        <label>Reading 1 (grams for 20 tablets):</label>
        <input type="number" id="r1" step="0.0001">
    </div>

    <div class="input-group">
        <label>Reading 2 (grams for 20 tablets):</label>
        <input type="number" id="r2" step="0.0001">
    </div>

    <div class="input-group">
        <label>Reading 3 (grams for 20 tablets):</label>
        <input type="number" id="r3" step="0.0001">
    </div>

    <button onclick="calculateBuild()">Calculate % Build-Up</button>

    <div class="result-box" id="result" style="display:none;"></div>

</div>

<script>
function calculateBuild() {
    let P = parseFloat(document.getElementById('prewarm').value);
    let r1 = parseFloat(document.getElementById('r1').value);
    let r2 = parseFloat(document.getElementById('r2').value);
    let r3 = parseFloat(document.getElementById('r3').value);

    if (!P || !r1 || !r2 || !r3) {
        alert("Please enter all values!");
        return;
    }

    let total = r1 + r2 + r3;
    let total_mg = total * 1000;
    let avg_spray = total_mg / 60;

    let gain = avg_spray - P;
    let buildup = (gain / P) * 100;

    document.getElementById("result").style.display = "block";
    document.getElementById("result").innerHTML =
        "<b>Average Weight During Spraying:</b> " + avg_spray + " mg<br>" +
        "<b>Weight Gain:</b> " + gain + " mg<br>" +
        "<b>% Build-Up:</b> " + buildup + "%";
}
</script>

</body>
</html>

