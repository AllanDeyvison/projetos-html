<!DOCTYPE html>

<html>
    <head>
        <title>Watch</title>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    </head>
    <script>

        function clock(){
            var time = new Date();
            var hours = time.getHours();
            var minutes = time.getMinutes();
            var seconds = time.getSeconds();
        
            if (hours < 10 ){ hours = '0' + hours; }
            if (minutes < 10 ){ minutes = '0' + minutes; }
            if (seconds < 10 ){ seconds = '0' + seconds; }

            document.getElementById("hours").textContent = hours;
            document.getElementById("minutes").textContent =  minutes;
            document.getElementById("seconds").textContent =  seconds;

        }

        watch = setInterval(clock);

    </script>


    <body>
        <div class="watch">

            <div>
                <span id="hours"></span>
                <span class="separator"></span>
                <span id="minutes"></span>
                <span class="separator"></span>
                <span id="seconds"></span>
            </div>

        </div>
    </body>

    <style>
        * {
        margin: 0;
        padding: 0;
        font-family: 'Open Sans', sans-serif;
        }

        body {
            height: 100vh;
            background-image: url('./assets/imagewall.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .watch {
        display: flex;
        align-items: center;
        justify-content: space-around;
        height: 250px;
        width: 550px;
        }

        .watch div {
        height: 0px;
        width: 0px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        color: rgb(0, 0, 0);
        background:  rgb(255, 255, 255);
        box-shadow: 0 10px 100px 100px rgb(255, 255, 255);
        backdrop-filter: blur(90px);
        border-radius: 25px;
        border: 10px; 
        }

        .watch span {
        font-weight: bold;
        font-size: 70px;
        }

        .watch span.separator::before {
        content: ":";
        margin: 5px; 
        }

        @media (max-width: 600px) {
        .watch {
            height: 200px;
            width: 370px;
        }
        .watch div {
            height: 140px;
            width: 100px;
        }
        .watch span {
            font-size: 50px;
        }
        
        }
    </style>

</html>
