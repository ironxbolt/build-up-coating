<!DOCTYPE html>
<html>
<head>
    <title>Tablet Coating Weight Calculator - Pharma Tool</title>
</head>
<body>

    <!-- Header -->
    <h1 align="center">Pharma Tablet Coating Weight Calculator</h1>
    <hr>

    <!-- Navigation -->
    <center>
        <a href="#">Home</a> |
        <a href="#">Calculator</a> |
        <a href="#">About</a> |
        <a href="#">Contact</a>
    </center>
    <hr>

    <!-- Hero Section -->
    <h2 align="center">Welcome to Pharma Tablet Coating Calculator</h2>
    <p align="center">
        A simple tool for estimating tablet weight before and after coating.
    </p>

    <!-- Features -->
    <h3>Features</h3>
    <ul>
        <li>Calculate pre- and post-coating weight</li>
        <li>Enter tablet specifications easily</li>
        <li>Useful for R&D, QC, and production teams</li>
    </ul>

    <!-- Calculator Preview Section -->
    <h3>Start Your Calculation</h3>
    <p>This section is a preview of the calculator inputs (HTML only, no working formula yet):</p>

    <form>
        <label>Tablet Name:</label><br>
        <input type="text" name="tablet"><br><br>

        <label>Pre-Coating Weight (mg):</label><br>
        <input type="text" name="preweight"><br><br>

        <label>Expected % Weight Gain:</label><br>
        <input type="text" name="gain"><br><br>

        <label>Batch Description:</label><br>
        <textarea rows="3" cols="30"></textarea><br><br>

        <input type="submit" value="Calculate (Not Functional)">
    </form>

    <hr>

    <!-- Footer -->
    <center>
        <p>© 2025 Pharma Calculator | All Rights Reserved</p>
    </center>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
    <title>Tablet Prewarming Weight Calculator</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: #f3f6fb;
        }
        .container {
            width: 60%;
            margin: auto;
            background: white;
            padding: 25px;
            margin-top: 40px;
            border-radius: 10px;
            box-shadow: 0 0 12px rgba(0,0,0,0.1);
        }
        h2 {
            text-align: center;
            color: #1a237e;
        }
        .section-title {
            background: #3949ab;
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
        }
        input {
            width: 100%;
            padding: 10px;
            margin-top: 6px;
            border-radius: 6px;
            border: 1px solid #bbb;
            font-size: 16px;
        }
        button {
            width: 100%;
            background: #1e88e5;
            padding: 12px;
            color: white;
            font-size: 18px;
            border: none;
            border-radius: 6px;
            margin-top: 15px;
            cursor: pointer;
        }
        button:hover {
            background: #1565c0;
        }
        .result-box {
            margin-top: 20px;
            padding: 15px;
            background: #e3f2fd;
            border-left: 6px solid #1565c0;
            font-size: 20px;
            border-radius: 6px;
        }
    </style>

</head>
<body>

<div class="container">

    <h2>Pharma Tablet Weight Calculator</h2>

    <div class="section-title">Section 1: Weight of Tablets After Prewarming</div>

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

    <button onclick="calculate()">Calculate Average Tablet Weight</button>

    <div id="result" class="result-box" style="display:none;"></div>

</div>

<script>
function calculate() {
    let r1 = parseFloat(document.getElementById('r1').value) || 0;
    let r2 = parseFloat(document.getElementById('r2').value) || 0;
    let r3 = parseFloat(document.getElementById('r3').value) || 0;

    let total = r1 + r2 + r3;          // Sum of 3 readings
    let mg = total * 1000;             // Convert to mg
    let final = mg / 60;               // Divide by 60 tablets

    document.getElementById('result').style.display = "block";
    document.getElementById('result').innerHTML =
        "<b>Average Prewarming Tablet Weight:</b> " + final.toFixed(2) + " mg";
}
</script>

</body>
</html>

