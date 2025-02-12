# bishnulimbu.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Current Date & Time</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            text-align: center;
            background-color: #282c34;
            color: white;
        }
        h1 {
            font-size: 2rem;
        }
        #datetime {
            font-size: 1.5rem;
            margin-top: 10px;
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <h1>Current Date & Time</h1>
    <div id="datetime"></div>

    <script>
        function updateDateTime() {
            const now = new Date();
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric', hour: '2-digit', minute: '2-digit', second: '2-digit' };
            document.getElementById("datetime").innerText = now.toLocaleString('en-US', options);
        }
        setInterval(updateDateTime, 1000);
        updateDateTime(); // Run immediately
    </script>
</body>
</html>
