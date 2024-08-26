<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meaowsi Website</title>
    <style>
        /* Base Styles */
        body {
            background-image: url('dog.jpg');
            background-size: cover;
            background-position: center;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            color: #fff;
        }
        header {
            background: rgba(0, 0, 0, 0.5);
            padding: 10px;
            text-align: center;
        }
        .logo {
            font-family: 'Lato', sans-serif;
            font-size: 36px;
            color: #fff;
            margin: 0;
        }
        nav {
            display: flex;
            justify-content: center;
            padding: 10px 0;
            flex-wrap: wrap; /* Allow items to wrap on smaller screens */
        }
        .nav-links a {
            margin: 5px;
            text-decoration: none;
            color: #017bf5;
            font-family: 'Cinzel', serif;
            font-size: 16px;
        }
        .nav-links a:hover {
            color: #0056b3;
        }
        .search-form {
            margin-top: 10px;
        }
        .search-form input[type="text"] {
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 4px;
            width: 300px;
            box-sizing: border-box;
        }
        .search-form button {
            padding: 8px 16px;
            border: none;
            border-radius: 4px;
            background-color: #017bf5;
            color: white;
            cursor: pointer;
            margin-left: 5px;
        }
        .search-form button:hover {
            background-color: #0056b3;
        }
        main {
            text-align: center;
            padding: 20px;
        }
        .main-title {
            font-family: 'Lato', sans-serif;
            font-size: 36px;
            color: #017bf5;
            margin: 20px 0;
        }
        .sub-title {
            font-family: 'Lato', sans-serif;
            font-size: 20px;
            color: #fff;
            margin-bottom: 30px;
        }
        footer {
            background: rgba(0, 0, 0, 0.7);
            color: #fff;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
            margin: 0;
        }
        
        /* Responsive Styles */
        @media (min-width: 768px) {
            .nav-links a {
                font-size: 18px;
            }
            .main-title {
                font-size: 48px;
            }
            .sub-title {
                font-size: 24px;
            }
            .search-form input[type="text"] {
                width: 400px; /* Wider search bar on larger screens */
            }
        }
        @media (min-width: 1024px) {
            .nav-links a {
                font-size: 20px;
            }
            .main-title {
                font-size: 60px;
            }
            .sub-title {
                font-size: 28px;
            }
            .search-form input[type="text"] {
                width: 500px; /* Even wider search bar on extra large screens */
            }
        }

        /* Chatbot Styles */
        .chatbot {
            position: fixed;
            bottom: 10px;
            right: 10px;
            width: 350px; /* Increased width */
            height: 450px; /* Increased height */
            background: rgba(0, 0, 0, 0.8);
            color: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            display: none;
            flex-direction: column;
        }

        .chatbot-header {
            background: #017bf5;
            color: #fff;
            padding: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-top-left-radius: 8px;
            border-top-right-radius: 8px;
        }

        .chatbot-body {
            flex: 1;
            padding: 10px;
            overflow-y: auto;
            background: #333;
            display: flex;
            flex-direction: column;
        }

        .chatbot-footer {
            background: #222;
            padding: 10px;
            display: flex;
            align-items: center;
        }

        .chatbot-toggle {
            position: fixed;
            bottom: 10px;
            right: 10px;
            background: #017bf5;
            color: #fff;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }

        .chatbot-toggle:hover {
            background: #0056b3;
        }

        #chatbot-messages {
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 5px;
        }

        #chatbot-input {
            flex: 0;
            width: calc(100% - 80px); /* Adjust input width */
            height: 50px; /* Increased height for better typing space */
            padding: 10px;
            border: none;
            border-radius: 5px;
            font-size: 16px; /* Larger font size for better readability */
        }

        #chatbot-send {
            width: 70px;
            padding: 10px;
            border: none;
            background: #017bf5;
            color: #fff;
            border-radius: 5px;
            cursor: pointer;
            margin-left: 10px; /* Add space between input and button */
        }

        #chatbot-send:hover {
            background: #0056b3;
        }
    </style>
</head>
<body>
    <header>
        <h3 class="logo">LOGO</h3>
        <nav class="nav-links">
            <a href="1.html">HOME</a>
            <a href="2.html">VIDEOS</a>
            <a href="3.html">PORTFOLIO</a>
            <a href="4.html">BLOG</a>
            <a href="5.html">CONTACT US</a>
        </nav>
        <div class="search-form">
            <input type="text" placeholder="Search...">
            <button>Search</button>
        </div>
    </header>
    
    <main>
        <h1 class="main-title">Meaowsi Kingdom</h1>
        <h3 class="sub-title">The Meaowsi Land</h3>
        <h3>
            <a href="rules.html" style="color: #017bf5; text-decoration: none;">The Rules</a>
        </h3>
    </main>

    <footer>
        <p>&copy; 2024 Meaowsi Kingdom. All rights reserved.</p>
    </footer>

    <!-- Chatbot HTML -->
    <div id="chatbot" class="chatbot">
        <div class="chatbot-header">
            <h4>Chat with us!</h4>
            <button id="chatbot-close">×</button>
        </div>
        <div class="chatbot-body">
            <div id="chatbot-messages"></div>
            <div class="chatbot-footer">
                <input type="text" id="chatbot-input" placeholder="Type your message...">
                <button id="chatbot-send">Send</button>
            </div>
        </div>
    </div>
    <button id="chatbot-toggle" class="chatbot-toggle">Chat</button>

    <script>
        // JavaScript for chatbot functionality
        document.getElementById('chatbot-toggle').onclick = function() {
            var chatbot = document.getElementById('chatbot');
            chatbot.style.display = chatbot.style.display === 'none' || chatbot.style.display === '' ? 'flex' : 'none';
        };

        document.getElementById('chatbot-close').onclick = function() {
            document.getElementById('chatbot').style.display = 'none';
        };

        document.getElementById('chatbot-send').onclick = function() {
            var input = document.getElementById('chatbot-input');
            var messages = document.getElementById('chatbot-messages');
            var message = input.value.trim();
            
            if (message) {
                console.log('User input:', message); // Debugging statement
                var userMessage = document.createElement('div');
                userMessage.textContent = 'You: ' + message;
                messages.appendChild(userMessage);
                
                // Simulate a bot response based on the message content
                var botResponse = '';
                if (/who created this website/i.test(message)) {
                    botResponse = 'Bot: Meaowsi created this website and also me!';
                } else if (/hi|hello/i.test(message)) {
                    botResponse = 'Bot: Hello! How can I help you today?';
                } else if (/meaowsi act 4/i.test(message)) {
                    botResponse = 'Bot: omnipotent';
                } else if (/is this website good?|is this good/i.test(message)) {
                    botResponse = 'Bot: Yes! but still in development!';
                } else if (/thanks|thank you/i.test(message)) {
                    botResponse = 'Bot: You\'re welcome! If you need more help, just let me know.';
                } else if (/joke/i.test(message)) {
                    botResponse = 'Bot: Why did the scarecrow win an award? Because he was outstanding in his field!';
                } else if (/time/i.test(message)) {
                    botResponse = 'Bot: The current time is... (Simulated response)';
                } else if (/how are you/i.test(message)) {
                    botResponse = 'Bot: I\'m just a bot, but I\'m doing great! How can I assist you?';
                } else if (/help/i.test(message)) {
                    botResponse = 'Bot: I\'m here to help! Please ask me anything.';
                } else if (/where are you/i.test(message)) {
                    botResponse = 'Bot: I exist in the digital realm, always here to assist you!';
                } else if (/weather/i.test(message)) {
                    botResponse = 'Bot: I can\'t check the weather, but you can use a weather app for that.';
                } else if (/your favorite color/i.test(message)) {
                    botResponse = 'Bot: I don\'t have personal preferences, but I like all colors equally but I like the shade black!';
                } else if (/goodbye|bye/i.test(message)) {
                    botResponse = 'Bot: Goodbye! Have a great day!';
                } else if (/news/i.test(message)) {
                    botResponse = 'Bot: I can\'t fetch the latest news, but you can check news websites for updates.';
                } else if (/dialogue|leon/i.test(message)) {
                    botResponse = 'Bot: "30 September 1998 it\'s a day I will never forget, the cop inside me died that day." - Leon S. Kennedy';
                } else if (/game/i.test(message)) {
                    botResponse = 'Bot: Let\'s play a game! English or Spanish?';
                } else if (/food/i.test(message)) {
                    botResponse = 'Bot: I don\'t eat, but I hear Kurkure is delicious!';
                } else if (/book/i.test(message)) {
                    botResponse = 'Bot: I don\'t read books, but I can recommend some popular ones like Diary of a Wimpy Kid series or the Harry Potter series!';
                } else if (/holiday/i.test(message)) {
                    botResponse = 'Bot: Holidays are a great time to relax! What\'s your favorite holiday?';
                } else if (/music/i.test(message)) {
                    botResponse = 'Bot: I don\'t listen to music, but I can suggest some popular genres!';
                } else if (/sports/i.test(message)) {
                    botResponse = 'Bot: Sports are exciting! Do you have a favorite sport or team?';
                } else {
                    botResponse = 'Bot: I\'m not sure how to respond to that. Can you please clarify or ask something else? I am still in development, sorry for the inconvenience.';
                }
                
                var botMessage = document.createElement('div');
                botMessage.textContent = botResponse;
                messages.appendChild(botMessage);
                
                // Scroll to the bottom
                messages.scrollTop = messages.scrollHeight;
                
                // Clear input
                input.value = '';
            }
        };
    </script>
</body>
</html>

