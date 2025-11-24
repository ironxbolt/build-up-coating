
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ONCO Tablet Coating | PRE 376</title>

    <style>
        body {
            margin: 0;
            background: #f0f4fa;
            font-family: Arial, sans-serif;
        }

        /* HEADER */
        .header {
            background: linear-gradient(145deg, #0d47a1, #1a73e8);
            padding: 55px;
            text-align: center;
            color: white;
            border-radius: 0 0 40px 40px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.25);
        }

        .header h1 {
            margin: 0;
            font-size: 46px;
            font-weight: bold;
        }

        .header p {
            margin-top: 12px;
            font-size: 22px;
            opacity: 0.9;
        }

        /* CARD SECTION */
        .main-box {
            width: 60%;
            margin: 60px auto;
            background: white;
            border-radius: 22px;
            padding: 40px;
            text-align: center;
            box-shadow: 0 6px 25px rgba(0,0,0,0.1);
        }

        .main-box h2 {
            font-size: 32px;
            color: #0d47a1;
        }

        .owners-box {
            margin-top: 25px;
            background: #1565c0;
            padding: 25px;
            border-radius: 14px;
            color: white;
            font-size: 22px;
            font-weight: bold;
            letter-spacing: 1px;
            line-height: 1.7;
        }

        /* FOOTER */
        .footer {
            margin-top: 50px;
            background: #0d47a1;
            color: white;
            padding: 18px;
            text-align: center;
            font-size: 15px;
        }
    </style>
</head>
<body>

    <!-- HEADER -->
    <div class="header">
        <h1>ONCO Tablet Coating</h1>
        <p>PRE 376 – Advanced Coating Technology</p>
    </div>

    <!-- MAIN CONTENT -->
    <div class="main-box">
        <h2>Owners & Operators</h2>

        <div class="owners-box">
           Kamal Sharma <br>
            &amp; <br>
            Archit Badyal
        </div>
    </div>

    <!-- FOOTER -->
    <div class="footer">
        © 2025 ONCO Coating | PRE 376
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

