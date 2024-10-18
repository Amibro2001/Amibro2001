
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Marche Afghan Pamir</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
        }

        header {
            background-color: #004d40; /* Dark green (temporary color, update to your color scheme later) */
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 24px;
        }

        nav {
            display: flex;
            justify-content: center;
            background-color: #00796b; /* Slightly lighter shade */
            padding: 15px;
        }

        nav a {
            margin: 0 15px;
            color: white;
            text-decoration: none;
            font-size: 18px;
        }

        /* Slider Section */
        .slider {
            position: relative;
            overflow: hidden;
            height: 60vh;
        }

        .slides {
            display: flex;
            width: 300%;
            height: 100%;
            transition: all 1s ease-in-out;
        }

        .slide {
            width: 100%;
            flex: 1;
        }

        .slide img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Button Styling */
        .prev, .next {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            padding: 10px;
            cursor: pointer;
            border: none;
            font-size: 24px;
        }

        .prev {
            left: 10px;
        }

        .next {
            right: 10px;
        }

        /* Add responsiveness */
        @media (max-width: 768px) {
            nav a {
                font-size: 14px;
            }

            header {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>

    <header>
        Marche Afghan Pamir
    </header>

    <nav>
        <a href="#">Home</a>
        <a href="#">Products</a>
        <a href="#">Afghani Foods</a>
        <a href="#">Contact</a>
    </nav>

    <section class="slider">
        <div class="slides">
            <div class="slide">
                <img src="https://via.placeholder.com/1200x600" alt="Afghan Spices">
            </div>
            <div class="slide">
                <img src="https://via.placeholder.com/1200x600" alt="Fresh Produce">
            </div>
            <div class="slide">
                <img src="https://via.placeholder.com/1200x600" alt="Afghani Cuisine">
            </div>
        </div>
        <button class="prev" onclick="moveSlides(-1)">&#10094;</button>
        <button class="next" onclick="moveSlides(1)">&#10095;</button>
    </section>

    <script>
        let index = 0;
        const slides = document.querySelector('.slides');
        const totalSlides = document.querySelectorAll('.slide').length;

        function moveSlides(direction) {
            index += direction;
            if (index < 0) {
                index = totalSlides - 1;
            } else if (index >= totalSlides) {
                index = 0;
            }
            slides.style.transform = `translateX(${-index * 100}%)`;
        }
    </script>

</body>
</html>
