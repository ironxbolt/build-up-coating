<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pharma Manufacturing | Tablet Coating & Compression</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #eef2f7;
        }

        /* ----------- HEADER ----------- */
        .header {
            background: url('https://i.imgur.com/0Y4F8aR.jpg') center/cover no-repeat;
            height: 330px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-shadow: 0 3px 6px rgba(0,0,0,0.3);
        }
        .header h1 {
            font-size: 42px;
            font-weight: bold;
        }

        /* ----------- NAV BAR ----------- */
        .navbar {
            display: flex;
            justify-content: center;
            background: #0d47a1;
            padding: 12px;
        }

        .navbar a {
            color: white;
            margin: 0 20px;
            font-size: 17px;
            text-decoration: none;
            font-weight: bold;
        }
        .navbar a:hover {
            color: #90caf9;
        }

        /* ----------- MAIN SECTION ----------- */
        .section {
            padding: 40px 10%;
        }

        .section-title {
            font-size: 30px;
            font-weight: bold;
            color: #0d47a1;
            margin-bottom: 20px;
            border-left: 6px solid #0d47a1;
            padding-left: 10px;
        }

        .cards {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
        }

        .card {
            width: 30%;
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.15);
            overflow: hidden;
            transition: 0.3s;
        }

        .card:hover {
            transform: scale(1.04);
        }

        .card img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .card h3 {
            padding: 15px;
            color: #0d47a1;
        }

        .card p {
            padding: 0 15px 20px 15px;
            color: #444;
            font-size: 15px;
        }

        /* ----------- FOOTER ----------- */
        .footer {
            background: #0d47a1;
            color: white;
            padding: 15px;
            text-align: center;
            margin-top: 40px;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <div class="header">
        <h1>Pharma Tablet Manufacturing & Coating</h1>
    </div>

    <!-- Navigation -->
    <div class="navbar">
        <a href="#">Home</a>
        <a href="#">Tablet Compression</a>
        <a href="#">Coating</a>
        <a href="#">R&D</a>
        <a href="#">Contact</a>
    </div>

    <!-- Main Content -->
    <div class="section">
        <div class="section-title">Our Pharma Expertise</div>

        <div class="cards">

            <!-- Card 1 -->
            <div class="card">
                <img src="https://i.imgur.com/Gy7qC23.jpeg" alt="Tablet Compression">
                <h3>Tablet Compression</h3>
                <p>
                    High-precision tablet press machines ensuring uniform hardness, thickness and friability.
                </p>
            </div>

            <!-- Card 2 -->
            <div class="card">
                <img src="https://i.imgur.com/9ERyUjO.jpeg" alt="Tablet Coating">
                <h3>Tablet Coating</h3>
                <p>
                    Advanced coating technologies: Film coating, sugar coating, enteric coating and more.
                </p>
            </div>

            <!-- Card 3 -->
            <div class="card">
                <img src="https://i.imgur.com/kVvF7d3.jpeg" alt="Chemical Ingredients">
                <h3>API & Excipients</h3>
                <p>
                    Premium quality Active Pharmaceutical Ingredients and excipients for formulation.
                </p>
            </div>

        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        © 2025 Pharma Manufacturing Solutions | All Rights Reserved
    </div>

</body>
</html>


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

