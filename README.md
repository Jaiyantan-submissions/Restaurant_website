# Ex.07 Restaurant Website
# Date: 27/11/2024
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:

# index.html:-
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>TasteLAB | Redefining Dining</title>
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
        <style>
            /* General Reset */
            * {
                margin: 0;
                padding: 0;
                box-sizing: border-box;
            }

            body {
                font-family: 'Poppins', sans-serif;
                background-color: #0a0a0a;
                color: #f5f5f5;
                overflow-x: hidden;
            }

            /* Header */
            header {
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 20px 5%;
                background-color: #151515;
                box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
                position: fixed;
                width: 100%;
                z-index: 1000;
                transition: background-color 0.3s ease, box-shadow 0.3s ease;
            }

            header:hover {
                background-color: #1f1f1f;
                box-shadow: 0 6px 15px rgba(0, 0, 0, 0.4);
            }

            .logo-container {
                display: flex;
                align-items: center;
            }

            .logo-container img {
                width: 50px;
                height: 50px;
                margin-right: 10px;
                border-radius: 50%;
                border: 2px solid #4CAF50;
            }

            header h1 {
                font-family: 'Dancing Script', cursive; /* Cursive font for header */
                font-size: 40px;
                font-weight: 700;
                color: #FFD700; /* Gold color */
                letter-spacing: 1.2px;
            }

            nav {
                display: flex;
                gap: 20px;
            }

            nav a {
                text-decoration: none;
                color: #f5f5f5;
                font-size: 16px;
                font-weight: 400;
                padding: 10px 20px;
                border-radius: 5px;
                background: #4CAF50;
                transition: transform 0.3s, background 0.3s ease;
            }

            nav a:hover {
                background: #3e8e41;
                transform: translateY(-3px);
            }

            /* Hero Section */
            .hero {
                text-align: center;
                padding: 150px 20px 80px;
                background: url('steak.jpeg') no-repeat center center;
                background-size: cover;
                color: #f5f5f5;
                position: relative;
            }

            .hero::after {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background: rgba(0, 0, 0, 0.4);
            }

            .hero h2 {
                font-family: 'Dancing Script', cursive; /* Cursive font for hero heading */
                font-size: 2.5em;
                margin: 20px 0 10px;
                font-weight: 700;
                letter-spacing: 1.5px;
                position: relative;
                z-index: 2;
                color: #FFD700; /* Gold color */
            }

            .hero p {
                font-size: 1.2em;
                margin-top: 10px;
                color: #bfbfbf;
                position: relative;
                z-index: 2;
            }

            /* Grid Section */
            .grid {
                display: flex;
                justify-content: space-between;
                gap: 20px;
                padding: 40px 5%;
            }

            .grid div {
                background: #151515;
                border-radius: 10px;
                padding: 20px;
                text-align: center;
                transition: transform 0.3s ease, box-shadow 0.3s ease;
                flex: 1;
            }

            .grid div:hover {
                transform: translateY(-10px);
                box-shadow: 0 10px 30px rgba(0, 255, 128, 0.3);
            }

            .grid img {
                max-width: 100%;
                height: auto;
                border-radius: 8px;
                margin-bottom: 15px;
            }

            .grid h3 {
                font-family: 'Dancing Script', cursive; /* Cursive font for grid headings */
                font-size: 1.5em;
                margin-bottom: 10px;
                color: #FFD700; /* Gold color */
            }

            .grid p {
                font-size: 1em;
                color: #bfbfbf;
            }

            /* Button */
            .btn-more {
                display: inline-block;
                margin: 30px auto;
                padding: 12px 30px;
                background: #4CAF50;
                border: none;
                border-radius: 5px;
                color: white;
                font-size: 18px;
                font-weight: 600;
                cursor: pointer;
                text-align: center;
                text-decoration: none;
                transition: transform 0.3s ease, background 0.3s ease;
            }

            .btn-more:hover {
                background: #3e8e41;
                transform: scale(1.1);
            }

            /* Footer */
            footer {
                background: #151515;
                padding: 20px 5%;
                text-align: center;
                color: #bfbfbf;
                margin-top: 40px;
            }

            footer a {
                color: #4CAF50;
                text-decoration: none;
                font-weight: 600;
            }

            footer a:hover {
                text-decoration: underline;
            }
        </style>
    </head>
    <body>
        <header>
            <div class="logo-container">
                <img src="logo.png" alt="Restaurant Logo"> <!-- Replace with your logo -->
                <h1>TasteLAB</h1>
            </div>
            <nav>
                <a href="#home">Home</a>
                <a href="menu.html">Menu</a>
                <a href="booking.html">Book</a>
                <a href="about.html">About</a>
                <a href="admin.html">Admin</a>
            </nav>
        </header>

        <div class="hero">
            <h2>Exciting Tongue-Devouring Dishes</h2>
            <p>Experience the art of taste, crafted with passion and precision.</p>
        </div>

        <section class="grid">
            <div>
                <img src="turkey.jpg" alt="Roasted Turkey">
                <h3>Our Royal Elegance</h3>
                <p>Delight in the finest roasted turkey.</p>
            </div>
            <div>
                <img src="dinner.png" alt="Dinner Table">
                <h3>Book a Table</h3>
                <p>Reserve a table for a luxurious dining experience.</p>
            </div>
            <div>
                <img src="eventhall.jpeg" alt="Event Hall">
                <h3>Book an Event Hall</h3>
                <p>Host your events in our beautifully decorated hall.</p>
            </div>
            <div>
                <img src="cheftopping.jpeg" alt="Chef Toppings">
                <h3>Opening Hours</h3>
                <p>Meet our chefs and enjoy the finest toppings.</p>
            </div>
        </section>

        <footer>
            <p>© 2024 TasteLAB | Designed by Jaiyantan S</p>
        </footer>
    </body>
    </html>

# admin.html:
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Chefs</title>
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@700&family=Pacifico&display=swap" rel="stylesheet">
        <style>
            body {
                font-family: Arial, sans-serif;
                margin: 0;
                padding: 0;
                background-color: #0d0d0d; /* Dark theme */
                color: white;
            }

            /* Header Section */
            header {
                display: flex;
                align-items: center;
                justify-content: space-between;
                padding: 20px 30px;
                background: #1a1a1a;
                box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.3);
            }

            header h1 {
                font-family: "Caveat", cursive;
                font-size: 50px;
                color: white;
                margin: 0;
            }

            nav {
                display: flex;
                gap: 20px;
            }

            nav a {
                text-decoration: none;
                color: white;
                padding: 10px 20px;
                background: #4CAF50;
                border-radius: 4px;
                transition: background 0.3s;
            }

            nav a:hover {
                background: #3e8e41;
            }

            /* Chef Profiles Section */
            .chefs-container {
                display: grid;
                grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
                gap: 20px;
                padding: 40px;
                max-width: 1200px;
                margin: auto;
            }

            .chef-card {
                background-color: #1a1a1a;
                border-radius: 10px;
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
                overflow: hidden;
                text-align: center;
                transition: transform 0.3s ease, box-shadow 0.3s ease;
            }

            .chef-card:hover {
                transform: translateY(-5px);
                box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            }

            .chef-card img {
                width: 100%;
                object-fit: cover;
                max-height: 300px;
            }

            .chef-details {
                padding: 20px;
            }
            .chef-details h1 {
        font-family: "Pacifico", cursive; /* Cursive font */
        font-size: 22px;
        color: #FFD700; /* Golden color */
        margin: 10px 0;
    }


            .chef-details h2,
            .chef-details h3 {
                font-size: 16px;
                color: #ddd;
                margin: 5px 0;
            }

            /* Footer Section */
            footer {
                text-align: center;
                padding: 20px;
                background: #1a1a1a;
                position: fixed;
                bottom: 0;
                width: 100%;
            }

            footer p {
                margin: 0;
                color: #bbb;
            }
        </style>
    </head>
    <body>

        <!-- Header Section -->
        <header>
            <h1>Our Chefs</h1>
            <nav>
                <a href="index.html">Home</a>
                <a href="menu.html">Menu</a>
                <a href="booking.html">Book</a>
                <a href="about.html">About</a>
                <a href="admin.html">Admin</a>
            </nav>
        </header>

        <!-- Chefs Profiles Section -->
        <div class="chefs-container">
            <div class="chef-card">
                <img src="chef1.jpeg" alt="Chef Nancy Jewel McDonie">
                <div class="chef-details">
                    <h1>Miss Nancy Jewel McDonie</h1>
                    <h2>Designation: Sous Chef</h2>
                    <h3>Experience: 3 years</h3>
                </div>
            </div>
            <div class="chef-card">
                <img src="chef2.jpeg" alt="Chef Harris">
                <div class="chef-details">
                    <h1>Mr. Harris</h1>
                    <h2>Designation: Executive Chef</h2>
                    <h3>Experience: 7 years</h3>
                </div>
            </div>
            <div class="chef-card">
                <img src="cheftopping.jpeg" alt="Chef Andrew Maguire">
                <div class="chef-details">
                    <h1>Mr. Andrew Maguire</h1>
                    <h2>Designation: Saucier Chef</h2>
                    <h3>Experience: 2 years</h3>
                </div>
            </div>
            <div class="chef-card">
                <img src="chef6.jpg" alt="Chef Ana de Armas">
                <div class="chef-details">
                    <h1>Miss Ana</h1>
                    <h2>Designation: Pastry Chef</h2>
                    <h3>Experience: 3 years</h3>
                </div>
            </div>
            <div class="chef-card">
                <img src="chef5.jpeg" alt="Chef Jennie Kim">
                <div class="chef-details">
                    <h1>Mr Kim</h1>
                    <h2>Designation: Pantry Chef</h2>
                    <h3>Experience: 4 years</h3>
                </div>
            </div>
            <div class="chef-card">
                <img src="chef4.jpg" alt="Chef Dwayne Johnson">
                <div class="chef-details">
                    <h1>Mr. Dwayne Johnson</h1>
                    <h2>Designation: Butcher Chef, Fish Chef</h2>
                    <h3>Experience: 4 years</h3>
                </div>
            </div>
        </div>

        <!-- Footer Section
        <footer>
            <p>&copy; 2024 Foodie's Paradise. All rights reserved.</p>
        </footer> -->

    </body>
    </html>


# OUTPUT:
# Home Page
!['Result_image'](image1.png)

# Menu Page
!['result_image'](image3.png)

# Admin Page
!['result'](image2.png)
# RESULT:
The program for designing restaurant website using HTML and CSS is completed successfully.
