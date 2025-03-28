<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Watchers</title>
    <style>
        body {
            font-family: 'Courier New', monospace;
            background-color: #000;
            color: #0f0;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }
        
        .container {
            text-align: center;
            padding: 30px;
            border: 1px solid #0f0;
            border-radius: 5px;
            max-width: 600px;
            width: 90%;
            box-shadow: 0 0 15px rgba(0, 255, 0, 0.3);
        }
        
        h1 {
            margin-bottom: 30px;
            letter-spacing: 3px;
            text-transform: uppercase;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-size: 18px;
        }
        
        input {
            background-color: #111;
            border: 1px solid #0f0;
            color: #0f0;
            padding: 10px;
            width: 80%;
            font-size: 16px;
            font-family: 'Courier New', monospace;
        }
        
        button {
            background-color: #0f0;
            color: #000;
            border: none;
            padding: 12px 25px;
            font-size: 16px;
            cursor: pointer;
            font-family: 'Courier New', monospace;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s;
        }
        
        button:hover {
            background-color: #0c0;
            box-shadow: 0 0 10px rgba(0, 255, 0, 0.7);
        }
        
        .message {
            display: none;
            margin-top: 20px;
            font-size: 18px;
            animation: blink 1.5s infinite;
        }
        
        @keyframes blink {
            0% { opacity: 1; }
            50% { opacity: 0.3; }
            100% { opacity: 1; }
        }
        
        .eyes {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #000;
            color: #f00;
            display: none;
            justify-content: center;
            align-items: center;
            font-size: 36px;
            font-weight: bold;
            letter-spacing: 5px;
            z-index: 1000;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>The Watchers</h1>
        <form id="targetForm">
            <div class="form-group">
                <label for="target">Enter Target Information:</label>
                <input type="text" id="target" name="target" required>
            </div>
            <button type="submit">Submit</button>
        </form>
        <div class="message" id="message">Processing target... We are watching...</div>
    </div>
    
    <div class="eyes" id="eyes">YOUR EYES WILL BE OURS</div>

    <script>
        // Prevent closing the tab
        window.onbeforeunload = function() {
            return "The Watchers are observing. Are you sure you want to leave?";
        };
        
        document.getElementById('targetForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Show the processing message
            document.getElementById('message').style.display = 'block';
            document.getElementById('targetForm').style.display = 'none';
            
            // After 6-10 seconds, show the eyes message
            const delay = Math.floor(Math.random() * 4000) + 6000; // 6-10 seconds
            
            setTimeout(function() {
                document.querySelector('.container').style.display = 'none';
                document.getElementById('eyes').style.display = 'flex';
                
                // Make the eyes message blink
                const eyes = document.getElementById('eyes');
                setInterval(function() {
                    eyes.style.color = eyes.style.color === 'rgb(255, 0, 0)' ? '#0f0' : '#f00';
                }, 500);
                
            }, delay);
        });
    </script>
</body>
</html>
