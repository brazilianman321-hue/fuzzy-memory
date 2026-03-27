<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>🍕 MATH & GAMES HUB - Pizza Edition</title>  
    <style>  
        @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');  
          
        * {  
            margin: 0;  
            padding: 0;  
            box-sizing: border-box;  
        }  
          
        body {  
            font-family: 'Press Start 2P', system-ui;  
            background: linear-gradient(135deg, #0f0f23, #1a1a2e);  
            color: #00ffcc;  
            min-height: 100vh;  
            overflow: hidden;  
        }  
          
        header {  
            background: #000;  
            border-bottom: 4px solid #00ffcc;  
            padding: 15px;  
            text-align: center;  
            box-shadow: 0 0 20px #00ffcc;  
        }  
          
        h1 {  
            font-size: 2.2rem;  
            text-shadow: 0 0 10px #00ffcc;  
            letter-spacing: 4px;  
        }  
          
        .subtitle {  
            font-size: 0.9rem;  
            color: #ff00aa;  
            margin-top: 5px;  
        }  
          
        .tabs {  
            display: flex;  
            background: #111;  
            border-bottom: 4px solid #ff00aa;  
            flex-wrap: wrap;  
        }  
          
        .tab-button {  
            flex: 1;  
            padding: 20px 15px;  
            background: #1a1a2e;  
            color: #00ffcc;  
            border: none;  
            font-family: 'Press Start 2P';  
            font-size: 1rem;  
            cursor: pointer;  
            transition: all 0.3s;  
            text-transform: uppercase;  
            border-right: 2px solid #222;  
            min-width: 140px;  
        }  
          
        .tab-button:last-child {  
            border-right: none;  
        }  
          
        .tab-button:hover {  
            background: #00ffcc;  
            color: #000;  
            transform: scale(1.05);  
        }  
          
        .tab-button.active {  
            background: #ff00aa;  
            color: #fff;  
            box-shadow: inset 0 0 15px #000;  
        }  
          
        .tab-content {  
            display: none;  
            height: calc(100vh - 140px);  
            padding: 10px;  
            background: #000;  
        }  
          
        .tab-content.active {  
            display: flex;  
            flex-direction: column;  
        }  
          
        iframe {  
            width: 100%;  
            height: 100%;  
            border: 4px solid #00ffcc;  
            border-radius: 8px;  
            box-shadow: 0 0 30px #00ffcc;  
            background: #111;  
        }  
          
        .info {  
            position: fixed;  
            bottom: 15px;  
            left: 15px;  
            background: rgba(0, 0, 0, 0.8);  
            padding: 10px 15px;  
            border: 2px solid #ff00aa;  
            font-size: 0.7rem;  
            max-width: 320px;  
            z-index: 100;  
            border-radius: 4px;  
        }  
          
        .footer {  
            position: fixed;  
            bottom: 15px;  
            right: 15px;  
            font-size: 0.7rem;  
            color: #ff00aa;  
            background: rgba(0, 0, 0, 0.7);  
            padding: 8px 12px;  
            border-radius: 4px;  
        }  
    </style>  
</head>  
<body>  
    <header>  
        <h1>🍕 GN-MATH .PIZZA EDITION 🍕</h1>  
        <p class="subtitle">ALL YOUR FAVORITE MATH & UNBLOCKED GAMES IN ONE TAB • NO NEW TABS EVER</p>  
    </header>  
  
    <div class="tabs">  
        <button class="tab-button active" onclick="openTab(event, 'gnmath')">GN-MATH</button>  
        <button class="tab-button" onclick="openTab(event, 'coolmath')">COOLMATH</button>  
        <button class="tab-button" onclick="openTab(event, 'ubghub')">UBGHUB</button>  
        <button class="tab-button" onclick="openTab(event, 'pizza')">PIZZA EDITION</button>  
    </div>  
  
    <!-- GN-MATH Tab -->  
    <div id="gnmath" class="tab-content active">  
        <iframe src="https://gn-math.dev/" allowfullscreen></iframe>  
    </div>  
  
    <!-- COOLMATH Tab -->  
    <div id="coolmath" class="tab-content">  
        <iframe src="https://www.coolmathgames.com/" allowfullscreen></iframe>  
    </div>  
  
    <!-- UBGHUB Tab -->  
    <div id="ubghub" class="tab-content">  
        <iframe src="http://ubghub.org/" allowfullscreen></iframe>  
    </div>  
  
    <!-- PIZZA EDITION Tab (you can change the URL if you have a specific Pizza Edition link) -->  
    <div id="pizza" class="tab-content">  
        <iframe src="https://gn-math.dev/" allowfullscreen></iframe>  
        <div style="position:absolute; top:20px; left:20px; background:rgba(255,0,170,0.9); color:#fff; padding:15px; border:4px solid #00ffcc; font-size:1.1rem; text-align:center; max-width:400px; z-index:10;">  
            🍕 PIZZA EDITION 🍕<br>  
            (GN-MATH with Pizza Simulator loaded by default)<br>  
            <small>Change the src in the code below if you have a different Pizza Edition URL</small>  
        </div>  
    </div>  
  
    <div class="info">  
        ✅ Everything stays in ONE tab<br>  
        ✅ No new tabs ever<br>  
        ✅ Pure HTML - no server needed<br>  
        ✅ Just save & open!  
    </div>  
  
    <div class="footer">  
        Made for you • Works on any computer • Unblocked style  
    </div>  
  
    <script>  
        function openTab(evt, tabName) {  
            // Hide all tab contents  
            const tabContents = document.getElementsByClassName("tab-content");  
            for (let i = 0; i < tabContents.length; i++) {  
                tabContents[i].classList.remove("active");  
            }  
              
            // Remove active from all buttons  
            const tabButtons = document.getElementsByClassName("tab-button");  
            for (let i = 0; i < tabButtons.length; i++) {  
                tabButtons[i].classList.remove("active");  
            }  
              
            // Show the selected tab and highlight button  
            document.getElementById(tabName).classList.add("active");  
            evt.currentTarget.classList.add("active");  
        }  
          
        // Keyboard shortcuts (1-4)  
        document.addEventListener('keydown', function(e) {  
            if (e.key === "1") openTab({currentTarget: document.querySelectorAll('.tab-button')[0]}, 'gnmath');  
            if (e.key === "2") openTab({currentTarget: document.querySelectorAll('.tab-button')[1]}, 'coolmath');  
            if (e.key === "3") openTab({currentTarget: document.querySelectorAll('.tab-button')[2]}, 'ubghub');  
            if (e.key === "4") openTab({currentTarget: document.querySelectorAll('.tab-button')[3]}, 'pizza');  
        });  
          
        console.log('%c🍕 Pizza Edition Hub ready! Everything stays in one tab.', 'color:#ff00aa; font-family:monospace;');  
    </script>  
</body>  
</html>  
