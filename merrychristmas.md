![Cm](pic/download.png)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Snow Effect</title>
    <style>
        body {
            margin: 0;
            background-color: #000;
            overflow: hidden;
        }
        .snowflake {
            position: fixed;
            top: -10px;
            width: 10px;
            height: 10px;
            background: white;
            opacity: 0.8;
            border-radius: 50%;
            animation: fall linear infinite;
        }
        @keyframes fall {
            to {
                transform: translateY(100vh);
            }
        }
    </style>
</head>
<body>
    <script>
        const snowflakeCount = 100;

        for (let i = 0; i < snowflakeCount; i++) {
            const snowflake = document.createElement('div');
            snowflake.classList.add('snowflake');
            snowflake.style.left = Math.random() * 100 + 'vw';
            snowflake.style.animationDuration = Math.random() * 3 + 2 + 's';
            snowflake.style.animationDelay = Math.random() * 5 + 's';
            snowflake.style.width = snowflake.style.height = Math.random() * 5 + 5 + 'px';
            document.body.appendChild(snowflake);
        }
    </script>
</body>
</html>
