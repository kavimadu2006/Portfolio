<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Portfoilo Web Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="header">
        <div class="container">
            <nav>
                <img src="my p.jpg" class="jpg">
                <ul id="sidemenu">
                    <li><a href="#header">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <i class="fas fa-times" onclick="closemenu()"></i>
                </ul>
                <i class="fas fa-bars" onclick="openmenu()"></i>
            </nav>
            <div class="header-text">
                <h1>Hi, I'm <span>Kavindiya</span><br> Madubashani From Sri Lanka</h1>
            </div>
        </div>
    </div>
    <!-- -------about----- -->
    <div id="about">
        <div class="container">
            <div class="row">
                <div class="about-col-1">
                    <img src="phone-and-laptop.jpg">
                </div>
                <div class="about-col-2">
                    <h1 class="sub-title">About me</h1>
                    <p>I am Kavindiya Madubashani Rathnayaka. I am a student of LNBTI Japanese <br>IT University in Maharagama. <br>
                        I am studying BSc(Hons) Computing Degree(Information Systems).
                    </p>
                </div>
            </div>
        </div>  
        <!-- -------projects------- --->
    <div id="projects">
        <div class="container">
            <h1 class="sub-title">Projects</h1>
            <div class="project-list">
                <div class="list">
                    <img src="project.jpg" class="jpg">
                    <div class="layer">
                        <h3>Arduino Based Digital Ruler</h3>
                        <p>Manually measuring distances, especially in hard-to-reach places, presents challenges and often requires 
                            multiple people to obtain accurate results. Traditional tools such as rulers and tape measures can be 
                            inconvenient, time-consuming, and prone to human error. <br>In this project, we use an Arduino-based system with 
                            an ultrasonic sensor to measure distances. The sensor emits ultrasonic waves, which reflect back to the sensor, 
                            and by calculating the time it takes for the reflection, the system determines the distance between objects. This 
                            solution automates the measurement process, reduces human involvement, and ensures more accurate and 
                            reliable results. <br>The aim of the Digital Measurement System is to provide an accurate and convenient method for measuring 
                            length, width, area, and perimeter in a user-friendly manner, minimizing the potential for human error and 
                            improving efficiency.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Contact Section -->
    <div id="contact">
        <div class="container">
            <div class="row">
                <div class="contact-left">
                    <h1 class="sub-title">Contact Me</h1>
                    <p>madukavindi05.com@gmail.com</p>
                    <p>0766073961</p>
                    <div class="social-icons">
                        <a href="http://wa.me/+94766073961" target="_blank">
                            <img src="what.jpeg" alt="WhatsApp">
                        </a>
                        <a href="https://www.instagram.com/kavindiyamadubashani?igsh=dG84dWxqcWJnMjNu"
                            target="_blank">
                            <img src="inst.jpeg" alt="Instagram">
                        </a>
                        <a href="https://www.tiktok.com/@kavi_girl_1982?_t=8q6MfTOPB6G&_r=1" target="_blank">
                            <img src="tiktok1.png" alt="TikTok">
                        <a href="https://www.facebook.com/share/xVu8dFwXgAx2QFzW/?mibextid=qi2Omg" target="_blank">
                            <img src="face.png" alt="facebook">
                        </a>
                    </div>
                </div>
                <div class="contact-right">
                    <form name="submit-to-google-shee">
                        <input type="text" name="Name" placeholder="Your Name" required>
                        <input type="email" name="Email" placeholder="Your Email" required>
                        <textarea name="Message" rows="6"placeholder="Your Message"></textarea>
                        <button type="submit" class="btn2">Submit</button>
                    </form>
                </div>
            </div>
        </div>
    </div>
<script>
    var tablinks = document.getElementsByClassName("tab-links");
    var tabcontents = document.getElementsByClassName("tab-links");

    function opentab(tabname){
        for(tablink of tablinks){
            tablink.classList.remove("active-link");
        }
        for(tablink of tabcontents){
            tablink.classList.remove("active-tab");
        }
        event.currentTarget.classList.add("active-link");
        document.getElementsById(tabname).classList.add("active-tab");
    }
</script>

<script>
    var sidemenu = document.getElementById("sidemenu");

    function openmenu(){
        sidemenu.style.right ="0";
    }
    function closemenu(){
        sidemenu.style.right ="200px";
    }
</script>
<script>
    const scriptURL = 'https://script.google.com/macros/s/AKfycbyt_7m7zcIAwtCs3BLIevsVau80jO6jdnvH-V2ouL09-AQ0hOKnQ6wd0cUjWuabxgT7/exec'
    const form = document.forms['submit-to-google-sheet']
  
    form.addEventListener('submit', e => {
      e.preventDefault()
      fetch(scriptURL, { method: 'POST', body: new FormData(form)})
        .then(response => console.log('Success!', response))
        .catch(error => console.error('Error!', error.message))
    })
  </script>
        
</body>
</html>
