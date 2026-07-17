<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Control Panel</title>
    <style>
        :root { --bg: #ffffff; --text: #000000; }
        body.dark-mode { --bg: #121212; --text: #ffffff; background-color: var(--bg); color: var(--text); }
        body { background-color: var(--bg); color: var(--text); font-family: sans-serif; padding: 20px; }
        .section { display: none; }
        .active { display: block; }
    </style>
</head>
<body>

    <button onclick="toggleTheme()">Toggle Dark/Light Mode</button>
    <nav>
        <button onclick="showSection('settings')">Settings</button>
        <button onclick="showSection('chat')">Chat</button>
    </nav>

    <!-- Settings Section -->
    <div id="settings" class="section active">
        <h2>Advanced Settings</h2>
        <label>Upload AI Model (.gguf):</label>
        <input type="file" id="modelUpload">
        <!-- Add your sliders/inputs here based on your screenshots -->
    </div>

    <!-- Chat Section -->
    <div id="chat" class="section">
        <h2>Chat Interface</h2>
        <div id="chatBox" style="height: 300px; border: 1px solid #ccc;"></div>
        <input type="text" id="userInput" placeholder="Type a message...">
    </div>

    <script>
        function showSection(id) {
            document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
            document.getElementById(id).classList.add('active');
        }
        function toggleTheme() { document.body.classList.toggle('dark-mode'); }
    </script>
</body>
</html>

