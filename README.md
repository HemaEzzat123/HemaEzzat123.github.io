<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Menu Effect</title>
    <style>
        * {
    margin: 0px;
    padding: 0px;
    }

body {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    height: 100vh;
    background-image: linear-gradient(#01012e, #240019);
}

section {
    background: url(stars1.png);
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

ul {
    text-align: center;
    position: relative;
    z-index: 10;
}

ul:hover li a {
    opacity: 0;
}

ul li {
    list-style: none;
    margin: 14px 0;
}

ul li::before {
    content: '';
    width: 200px;
    height: 100px;
    border-radius: 50%;
    background-color: white;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, 80%);
    opacity: 0;
    transition: 0.5s;
    box-shadow: 0 0 100px orangered;
}

ul li:hover::before {
    opacity: 0.5;
    width: 100px;
}

ul li::after {
    content: attr(data-text);
    color: white;
    letter-spacing: 50px;
    font-size: 80px;
    font-weight: 900;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: 0.5s;
    pointer-events: none;
    text-transform: uppercase;
    opacity: 0;
}

ul li:hover::after {
    letter-spacing: 5px;
    opacity: 0.5;

}

ul li a {
    color: white;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 20px;
    font-weight: 500;
    padding: 6px 15px;
    letter-spacing: 2px;
    border-radius: 20px;
    background-color: darkblue;
    display: inline-block;
    width: 120px;
    transition: .5s;
    position: relative;
    z-index: 10;
}

ul li a:hover {
    background-color: darkmagenta;
    transform: scale(1.5);
    opacity: 1;
}
    </style>
</head>

<body>
    <section>
        <ul>
            <li data-text="sun"><a href="#">sun</a></li>
            <li data-text="mercury"><a href="#">mercury</a></li>
            <li data-text="venus"><a href="#">venus</a></li>
            <li data-text="earth"><a href="#">earth</a></li>
            <li data-text="jupiter"><a href="#">jupiter</a></li>
            <li data-text="uranus"><a href="#">uranus</a></li>
            <li data-text="neptune"><a href="#">neptune</a></li>
        </ul>
    </section>
</body>

</html>

