# Branded-collection
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navbar with Hero Slider, Moral, and My Collection</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }

        /* Navbar container */
        .navbar {
            background-color: #87CEEB; /* Sky blue */
            position: sticky;
            top: 0; /* Sticks to the top */
            z-index: 1000; /* Ensures it stays above other elements */
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
        }

        /* Logo */
        .logo {
            color: #003366; /* Deep blue */
            font-size: 36px;
            font-weight: bold;
        }

        /* Navbar links */
        .nav-links {
            display: flex;
            gap: 20px;
        }

        .nav-links a {
            text-decoration: none;
            color: black; /* Black text for links */
            font-size: 18px;
            cursor: pointer;
        }

        /* Service button */
        .service-button {
            background-color: black;
            color: white;
            padding: 8px 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .service-button:hover {
            background-color: #333;
        }

        /* Hero Section */
        .hero {
            position: relative;
            width: 100%;
            height: 1080px; /* Set height to 1080px for desktop-size images */
            overflow: hidden;
        }

        .carousel-item {
            height: 100vh; /* Full viewport height */
            background-size: cover;
            background-position: center;
        }

        .carousel-caption {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
        }

        .carousel-caption h1 {
            font-weight: bold;
            font-size: 3rem;
        }

        .carousel-caption p {
            font-size: 1.25rem;
        }

        .carousel-caption .btn {
            background-color: #003366;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
        }

        .carousel-control-prev-icon,
        .carousel-control-next-icon {
            background-color: black;
            border-radius: 50%;
        }

        /* Black overlay for slider */
        .carousel-item::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5); /* Black with transparency */
        }

        /* Business Moral */
        .moral {
            text-align: center;
            font-size: 20px;
            font-style: italic;
            margin: 20px 0;
        }

        /* My Collection Section */
        .my-collection {
            padding: 20px;
        }

        .collection-title {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
            text-align: center;
        }

        .collection-grid {
            display: flex;
            justify-content: space-between;
            gap: 20px;
        }

        .collection-column {
            width: 48%; /* Each column takes up 48% of the container width */
            display: flex;
            flex-direction: column;
            gap: 20px; /* Space between items within the column */
        }

        .collection-item {
            position: relative;
            text-align: center;
        }

        .collection-item img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 5px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .collection-item p {
            margin-top: 5px;
            font-size: 16px;
            font-weight: bold;
        }

        /* Contact Section */
        .contact {
            margin: 40px auto;
            padding: 20px;
            text-align: center;
            border: 2px solid #87CEEB; /* Highlighted border for service */
            border-radius: 10px;
            max-width: 600px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .contact h2 {
            font-size: 24px;
            margin-bottom: 10px;
        }

        .contact p {
            font-size: 18px;
            margin: 5px 0;
        }
    </style>
</head>
<body>

    <!-- Navbar -->
    <div class="navbar">
        <!-- Logo -->
        <div class="logo">『ᴧ𝓶』</div>

        <!-- Nav Links -->
        <div class="nav-links">
            <a href="#home" onclick="scrollToTop()">Home</a>
        </div>

        <!-- Service Button -->
        <button class="service-button" onclick="scrollToService()">Service</button>
    </div>

    <!-- Hero Section - Carousel -->
    <div id="heroCarousel" class="carousel slide carousel-fade" data-bs-ride="carousel">
        <div class="carousel-indicators">
            <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
            <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
            <div class="carousel-item active" style="background-image: url('images.jpeg');">
                <div class="carousel-caption text-center">
                    <h1>Welcome to Our Service</h1>
                    <p>We provide the best services in the industry. Let us help you grow your business.</p>
                    <a href="#readmore" class="btn">Read More</a>
                </div>
            </div>
            <div class="carousel-item" style="background-image: url('images (1).jpeg');">
                <div class="carousel-caption text-center">
                    <h1>Innovative Solutions</h1>
                    <p>We offer innovative and customized solutions to meet your business needs.</p>
                    <a href="#readmore" class="btn">Read More</a>
                </div>
            </div>
            <div class="carousel-item" style="background-image: url('images (3).jpeg');">
                <div class="carousel-caption text-center">
                    <h1>Your Success, Our Priority</h1>
                    <p>Join us and experience unparalleled growth and success in your business journey.</p>
                    <a href="#readmore" class="btn">Read More</a>
                </div>
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#heroCarousel" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#heroCarousel" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>

    <!-- Business Moral -->
    <div class="moral">
        "Success in business is about creating value, not just making profit."
    </div>

    <!-- My Collection Section -->
    <div class="my-collection">
        <div class="collection-title">My Collection</div>
        <div class="collection-grid">
            <!-- Left Column -->
            <div class="collection-column">
                <div class="collection-item">
                    <a href="detals.html" target="_Blank">
                        <img src="2a0650b6abc53d169e953b2641393ec3.jpg" alt="Mustung GT">
                    </a>
                    <p>Mustung GT</p>
                </div>
                <div class="collection-item">
                    <a href="details.html" target="_blank">
                        <img src="g310-rr-left-front-three-quarter-5.jpeg" alt="G310 RR">
                    </a>
                    <p>BMW 310 RR</p>
                </div>
                <div class="collection-item">
                    <a href="details3.html" target="_blank">
                        <img src="images (7).jpeg" alt="The Fling Car">
                    </a>
                    <p>The Fling Car</p>
                </div>
                <div class="collection-item">
                    <a href="blue_angel.html" target="_blank">
                        <img src="images (6).jpeg" alt="Blue Angel">
                    </a>
                    <p>Blue Angel</p>
                </div>
                <div class="collection-item">
                    <a href="gt_650.html" target="_blank">
                        <img src="images (5).jpeg" alt="GT 650">
                    </a>
                    <p>GT 650</p>
                </div>
            </div>

            <!-- Right Column -->
            <div class="collection-column">
                <div class="collection-item">
                    <a href="black_horse.html" target="_blank">
                        <img src="joshua-koblin-IdwBbPRc2FU-unsplash.jpg" alt="Black Horse">
                    </a>
                    <p>Black Horse</p>
                </div>
                <div class="collection-item">
                    <a href="blue_pari.html" target="_blank">
                        <img src="images (6).jpeg" alt="Blue Pari">
                    </a>
                    <p>Blue Pari</p>
                </div>
                <div class="collection-item">
                    <a href="cheta.html" target="_blank">
                        <img src="images (8).jpeg" alt="Cheta">
                    </a>
                    <p>Cheta</p>
                </div>
                <div class="collection-item">
                    <a href="gangstar.html" target="_blank">
                        <img src="images (10)(1).jpeg" alt="Gangstar">
                    </a>
                    <p>Gangstar</p>
                </div>
                <div class="collection-item">
                    <a href="powerfull.html" target="_blank">
                        <img src="images (9)(1).jpeg" alt="Power Full">
                    </a>
                    <p>Power Full</p>
                </div>
            </div>
        </div>
    </div>
<!-- Branded Cars and Bikes Section -->
<div class="branded-collection">
    <div class="collection-title">Branded Cars & Bikes</div>
    <div class="branded-grid">
        <!-- Row 1 of Logos and Names -->
        <div class="branded-item">
            <img src="images (16).jpeg" alt="BMW Logo">
            <p>BMW</p>
        </div>
        <div class="branded-item">
            <img src="images (11).jpeg" alt="Lamborghini Logo">
            <p>LAMBORGINI</p>
        </div>
        <div class="branded-item">
            <img src="images (12).jpeg" alt="Mercedes Logo">
            <p>MERCEDES</p>
        </div>
        <div class="branded-item">
            <img src="images (14).jpeg" alt="Yamaha Logo">
            <p>YAMAHA</p>
        </div>
        <div class="branded-item">
            <img src="images (15).jpeg" alt="Rolls Royce Logo">
            <p>ROLLS ROYCE</p>
        </div>
        <div class="branded-item">
            <img src="images (10).jpeg" alt="Ford Logo">
            <p>FORD</p>
        </div>
        <!-- Row 2 of Logos and Names -->
        <div class="branded-item">
            <img src="images (13).jpeg" alt="Audi Logo">
            <p>AUDI</p>
        </div>
        <div class="branded-item">
            <img src="images (9).jpeg" alt="Ferrari Logo">
            <p>FERRARI</p>
        </div>
    </div>
</div>
    
<!-- Contact Section -->


<style>
    /* Branded Cars and Bikes Section */
    .branded-collection {
        padding: 20px;
    }

    .collection-title {
        font-size: 24px;
        font-weight: bold;
        margin-bottom: 20px;
        text-align: center;
    }

    .branded-grid {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        justify-content: center;
    }

    .branded-item {
        width: 22%; /* Each item takes 22% of the width, so we have space for 4 items per row */
        text-align: center;
    }

    .branded-item img {
        width: 100%;
        max-width: 150px; /* Size of the logos */
        height: auto;
        margin-bottom: 10px;
    }

    .branded-item p {
        font-size: 16px;
        font-weight: bold;
    }
</style>
    <!-- Contact Section -->
    <div class="contact" id="contact">
        <h2>Contact Information</h2>
        <p><strong>Phone:</strong> 7872-663-998</p>
        <p><strong>Email:</strong> asifmandal@gmail.com</p>
        <p><strong>Address:</strong> Karimpur, Nadia, West Bengal</p>
    </div>

    <script>
        // Scroll to top function
        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Scroll to Service (Contact Section)
        function scrollToService() {
            document.querySelector('#contact').scrollIntoView({ behavior: 'smooth' });
        }
    </script>

    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.min.js"></script>
</body>
</html>
