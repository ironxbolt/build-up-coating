# build-up-coating
welcome
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Website</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f4f4f4;
        }
        header {
            background: #333;
            color: #fff;
            padding: 15px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        header h1 {
            margin: 0;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-size: 18px;
        }
        .hero {
            height: 70vh;
            background: url('https://picsum.photos/1200/600') center/cover no-repeat;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            text-shadow: 2px 2px 5px #000;
            flex-direction: column;
        }
        .hero h2 {
            font-size: 3em;
            margin: 0;
        }
        .hero p {
            font-size: 1.3em;
        }
        .section {
            padding: 50px 40px;
            text-align: center;
        }
        .services {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        }
        .service-box {
            background: #fff;
            padding: 20px;
            width: 30%;
            min-width: 250px;
            margin: 15px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        footer {
            background: #333;
            color: #fff;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <h1>My Website</h1>
        <nav>
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Services</a>
            <a href="#">Contact</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h2>Welcome to My Website</h2>
        <p>Your tagline goes here...</p>
    </section>

    <!-- Services Section -->
    <section class="section">
        <h2>Our Services</h2>
        <div class="services">
            <div class="service-box">
                <h3>Service One</h3>
                <p>Short description of service one.</p>
            </div>
            <div class="service-box">
                <h3>Service Two</h3>
                <p>Short description of service two.</p>
            </div>
            <div class="service-box">
                <h3>Service Three</h3>
                <p>Short description of service three.</p>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" style="background: #fff;">
        <h2>About Us</h2>
        <p>
            This is a simple homepage template. You can customize it according to your project. 
            Add images, change text, and modify the layout as you like.
        </p>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2025 My Website | All Rights Reserved</p>
    </footer>

</body>
</html>
