<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>POE2 New Season Countdown</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background: url('https://www.coolyouoa.cn/storage/banner/202504/gkz1wCKMkwdDAiC3GgWhjZjiY78xUcPcy52Q1ouH.jpg') no-repeat center center fixed;
            background-size: cover;
            color: #fff;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center; /* Center content vertically */
        }
        h1 {
            margin: 100px 0;
            font-size: 6em;
            text-shadow: 0px 0px 0px rgba(0,0,0,0.7);
        }
        #countdown {
            font-size: 6em;
            font-weight: bold;
            padding: 10px;
            background-color: rgba(0, 0, 0, 0.6);
            border-radius: 10px;
            display: inline-block;
            animation: fadeIn 2s ease-in-out;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.9);
            position: relative;
            top: 15%; /* Move countdown 30% down */
        }
        #countdown span {
            display: block;
            margin: 10px 0;
        }
        .footer {
            position: fixed;
            bottom: 20px;
            width: 100%;
            text-align: center;
            font-size: 1.2em;
        }
        .footer a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
    <script>
        function updateCountdown() {
            const targetDate = new Date("2025-04-04T19:00:00Z").getTime();
            const now = new Date().getTime();
            const distance = targetDate - now;

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById("countdown").innerHTML = 
                `<span>${days} days</span><span>${hours} hours</span><span>${minutes} minutes</span><span>${seconds} seconds</span>`;

            if (distance < 0) {
                clearInterval(timer);
                document.getElementById("countdown").innerHTML = "Season has started!";
            }
        }

        const timer = setInterval(updateCountdown, 1000);
    </script>
</head>
<body>
    <h1>POE2 New Season "Dawn of the Hunt" Countdown</h1>

    <div id="countdown"></div>

    </div>
</body>
</html>
