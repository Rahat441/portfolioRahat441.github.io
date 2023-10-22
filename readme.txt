<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" class ="text/css" href="style.css">
   <style>


        body {
            height: 100%; width: 100%;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background-image: url('../asset/BG.jpg');
        }
        
        
        /* Navigation Bar */
        
        /* Responsive styles */
        @media (max-width: 600px) {
            
            .top-bar {
                justify-content: center; /* Center align buttons for smaller screens */
            }
            .button {
                font-size: 18px; /* Adjust font size for smaller screens */
                padding: 8px 10px; /* Adjust padding for smaller buttons */
            }
            .body-text {
                font-size: 16px; /* Adjust font size for smaller screens */
                position: relative; /* Change to relative for better flow */
                left: 0; /* Adjust horizontal position for better centering */
                margin-top: 5%; /* Adjust margin for better spacing */
            }
            .footer-container {
                flex-direction: column;
                align-items: center;
            }

            .footer-icon {
                margin: 10px;
            }
        }

        .footer-container {
            align-self: center;
            display: flex;
            justify-content: center;
            position: relative;
            /* padding: 20px 0; */
            position: fixed;
            left: 100px;
            bottom: 10px;
            width: 80%;
            justify-content: space-between;
            

          
        }

        .footer-icon {
            display: inline-block;
            padding: 0.5%;
            border-radius: 80%;
        }

        .footer-icon img {
            height: 55px;
            width: 60px;
            border-radius: 40px;
        }
    
       /* Optional: Some basic styling */
       #container {
            width: 20%; /* Set the desired maximum width for the container */
            border: 1px solid #ddd; /* Add a border for visibility */
            padding: 10px; /* Add some padding for spacing */
            font-family: monospace; /* Use a monospace font for consistent spacing */
        }
        #hiddenP {
            justify-content: flex-end;
           
            white-space: pre;
        /* display: inline-block;  */
           
            opacity: 0.6; /* Initially set opacity to 0 */
            position: relative;
            right: 400px;
            bottom: 30px;
            font-size: 18px;
            animation: typingEffect 1s steps(249, end);
            transition: opacity 0.3s; 
            
            word-spacing: 5px;
            
        }

        @keyframes typingEffect {
            from {
                transform: translateY(100%);
                opacity: 0.3;
                width: 0;
            }
            to {
                transform: translateY(0);
                opacity: 0.6;
                width: 50%;
            }
        }
        

        

        
        
   </style>
</head>
<body>
    


    
     <!-- NAVIGATION -->
    <div class="nav-bar">
           
        <div class="top-bar">
            <!-- <a href="index.html" style=" position: relative;right:875px;">
                <img src="../asset/homeButton.png" style="height: 40px; width: 40px; border-radius: 50%; " alt="Back" />
                
            </a> -->
            <a href="about.html" class="button"> My Story </a> 
            <a href="Projects.html" class="button">Projects</a>
            <a href="Experience.html" class="button">Experience</a>
            <a href="Education.html" class="button">Education</a>
        </div>
    </div>
    <!-- Navigation bar -->
    
   
    <div class="body-text"> 
        Welcome
        <br/>
        
            <p id='hiddenP'>
                
                Hi, I'm Rahat Bhuiyan, a Computer Science major with a <br/>passion for crafting immersive experiences through code.
                 My journey combines the logic of algorithms, the elegance <br/>of mathematics, and the creativity of game design.
            </p>
         
        
    </div>
    <!-- Footer -->
    <div class="footer-container">
        
        <div class="footer-icon"><a href="https://www.linkedin.com/in/rahat-bhuiyan-30887920b/"> <img src="../asset/ling.png" alt="LinkedIn" class="linkedin-icon"/></a></div>
       
        <div class="footer-icon">
            <a href="https://www.facebook.com/rahat.alam.1614460">
                <img src="../asset/Facebook_Logo.png" alt="Facebook" class="facebook-icon"/>
            </a>
        </div>
        
        <div class="footer-icon">
            <a href="https://www.instagram.com">
                <img src="../asset/insta.jpeg" alt="Instagram" class="instagram-icon"/>
            </a>
        </div>
        <div class="footer-icon">
            <a href="https://github.com/Rahat441">
                <img src="../asset/git.png" alt="GitHub" class="github-icon"/>
            </a>
        </div>
    </div>
    <script>
         // Wait for the page to load
         // Wait for the page to load
        window.onload = function () {
            // Get the target <p> tag
            const targetP = document.getElementById('hiddenP');

            // Get the text content of the <p> tag
            const text = targetP.innerText;

            // Clear the content of the <p> tag
            targetP.innerText = '';

            // Set initial opacity to 0
            targetP.style.opacity = 0.3;

            // Function to reveal each letter with a delay
            function revealLetters(index) {
                if (index < text.length) {
                    targetP.innerText += text.charAt(index);
                    targetP.style.opacity = .6;
                    setTimeout(function () {
                        revealLetters(index + 1);
                    }, 1); // Change the delay time between letters (in milliseconds) as needed
                }
            }

            // Call the revealLetters function
            revealLetters(0);
        };
    </script>
</body>
</html>

THISIS It