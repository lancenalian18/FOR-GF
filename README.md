<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title></title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      body {
        background-image: url("Background.jpg");
        background-size: cover;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: 0;
        font-family: "Arial", sans-serif;
        color: #fff;
        text-shadow: 0px 0px 10px rgba(0, 0, 0, 0.7);
      }

      .container {
        text-align: center;
        background: rgba(0, 0, 0, 0.7);
        padding: 30px;
        border-radius: 15px;
        box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.5);
        max-width: 500px;
        width: 100%;
        margin: 20px;
        height: 40%;
      }

      .photo {
        width: 250%;
        height: 270%;
        max-width: 500px;
        max-height: 270px;
        border-radius: 15px;
        transition: transform 0.3s ease-in-out;
      }
      .flip-box {
        background-color: transparent;
        width: 500px;
        height: 270px;
        border-radius: 15px;
        perspective: 1000px;
      }

      .flip-box-inner {
        position: relative;
        width: 100%;
        height: 100%;
        border-radius: 15px;
        text-align: center;
        transition: transform 0.8s;
        transform-style: preserve-3d;
      }

      .flip-box:hover .flip-box-inner {
        transform: rotateY(180deg);
      }

      .flip-box-front,
      .flip-box-back {
        position: absolute; 
        width: 100%;
        height: 100%;
        -webkit-backface-visibility: hidden;
        backface-visibility: hidden;
      }

      .flip-box-front {
        background-color: #bbb;
        color: black;
        border-radius: 15px;
      }

      .flip-box-back {
        background-color: #555;
        color: white;
        transform: rotateY(180deg);
        border-radius: 15px;
      }
      .flip-box-back h2{
        margin-top: 50px;
      }
      .next-button {
        display: inline-block;
        padding: 12px 25px;
        font-size: 18px;
        color: #fff;
        background: linear-gradient(45deg, #ff0066, #ff66cc);
        text-decoration: none;
        border-radius: 8px;
        transition: background 0.3s  ease-in-out, transform 0.3s ease-in-out,
          box-shadow 0.3s ease-in-out;
        box-shadow: 0px 5px 15px rgba(255, 0, 102, 0.4);
      }

      .next-button:hover {
        background: linear-gradient(45deg, #ff66cc, #ff0066);
        transform: scale(1.05);
        box-shadow: 0px 10px 20px rgba(255, 0, 102, 0.6);
      }
    
    </style>
  </head>
  <body>
    <audio autoplay>
      <source src="Pamungkas  To The Bone.mp3" type="audio/mpeg">  
    </audio>
    <div class="container">
      <div class="flip-box">
        <div class="flip-box-inner">
          <div class="flip-box-front">
      <img src="Example.jpg" alt="Foto" class="photo" />
    </div>
    <div class="flip-box-back">
      <h2>TO MY LOVE</h2>
      <p>I LOVE YOU SO MUCH</p>
      <a href="next.html" class="next-button">Next</a>
    </div>
    <script src="script.js"></script>
  </body>
</html>
