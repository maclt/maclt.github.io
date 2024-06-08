<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scroll Move Example</title>
    <style>
        body {
            margin: 0;
        }
        .header {
            height: 25vh;
            background-color: lightcoral;
            position: sticky;
        }
        .component {
            background-color: greenyellow;
            height: 95vh;
            overflow: clip;
            transition: transform 0.3s;
        }
        span {
            font-size: x-large;
        }
        h1 {
            margin: 0;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>photo</h1>
    </div>
    <div class="component">
        <h1>title</h1>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
        <span>scrollable</br></span>
    </div>
    <script>
        document.addEventListener('scroll', () => {
            const component = document.querySelector('.component');
            const scrolled = window.scrollY;
            // height of display * (vh of component - vh of the header) / 100 - buffer
            const threshold = window.innerHeight * (95-75) / 100 - 5;
            if(scrolled >= threshold) {
                component.style.overflow = 'scroll';
            } else {
                component.style.overflow = 'clip';
            }
        });
    </script>
</body>
</html>
