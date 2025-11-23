Made By Archit Badyal
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

