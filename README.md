# ARTGALLERY
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Art Gallery</title>
  <style>
    body {
  margin: 0;
  padding: 0;
  font-family: 'Arial', sans-serif;
  background-image: url('img/w4.jpeg'); /* Replace with your image file name */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

    header {
      background-color: #333;
      padding: 10px;
      text-align: center;
      color: white;
    }

    nav {
      display: flex;
      justify-content: space-around;
      background-color: #444;
      padding: 10px;
    }

    section {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      padding: 20px;
    }

    .art-piece {
      position: relative;
      width: 200px; /* Set your default width */
      height: 300px; /* Set your default height */
      margin: 10px;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      display: flex;
      align-items: center;
      justify-content: center;
      transition: transform 0.3s ease-in-out; /* Add a smooth transition effect */
    }

    .art-piece img {
      width: 100%; /* Make sure the image takes up 100% of the container */
      height: auto; /* Maintain the aspect ratio of the image */
    }

    .overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      background: rgba(0, 0, 0, 0.7); /* Semi-transparent black overlay */
      color: white;
      padding: 10px;
      box-sizing: border-box;
      opacity: 0; /* Initially hidden */
      transition: opacity 0.3s ease-in-out;
    }

    .art-piece:hover {
      transform: scale(1.2); /* Increase scale on hover (you can adjust the value) */
    }

    .art-piece:hover .overlay {
      opacity: 1; /* Show overlay on hover */
    }
  </style>
</head>
<body>
  <header>
    <h1>Art Gallery</h1>
  </header>
  
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
    <a href="#support">Support</a>
    <a href="#loginsignup">Log-in/Sign-up</a>
  </nav>

  <section>
    <div class="art-piece">
      <a href="art1.html">
        <img src="img/01nADpg4RnygIYXOGUqLXA.jpg" alt="Art 1">
        <div class="overlay">
          <p>Artist: DRACO</p>
        </div>
      </a>
    </div>
    <div class="art-piece">
        <a href="art1.html">
          <img src="img/3M1GYNlFSBWc2wzdINJ9pA.jpg" alt="Art 1">
          <div class="overlay">
            <p>Artist: JNR</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/8eKta9JqTueAUfRmRtRatQ.jpg" alt="Art 1">
          <div class="overlay">
            <p>Artist: IKEMBA</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/bcBOe1xYRriLRStGaq6tDQ.jpg" alt="Art 1">
          <div class="overlay">
            <p>Artist: EMMANUEL</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="data:image/jpeg;base64,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" alt="Art 1">
          <div class="overlay">
            <p>Artist: IKECHUKWU</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/FLsPG1x7SqWvXBGGV-oR-Q.jpg" alt="Art 1">
          <div class="overlay">
            <p>Artist: PRIME</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (1).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: PRIMAL</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (10).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: STRANGER</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (11).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: PHANTOM</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (12).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: DRAC</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (13).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: X</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (14).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: BOBO</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (15).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: JUNIOR</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (16).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: ME</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (17).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: EMMA</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (18).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: IK</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (19).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: IMPULSE</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (2).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: XS</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (9).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: AGENT E</p>
          </div>
        </a>
      </div>
      <div class="art-piece">
        <a href="art1.html">
          <img src="img/ideogram (8).jpeg" alt="Art 1">
          <div class="overlay">
            <p>Artist: SHADOW</p>
          </div>
        </a>
      </div>
  </section>

  <footer>
    <p>&copy; 2023 Art Gallery</p>
  </footer>
</body>
</html>
