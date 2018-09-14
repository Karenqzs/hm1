<!DOCTYPE html>
<html>
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.1/p5.min.js"></script>
    <style>
      html, body {
        margin: 0;
        padding: 0;
      }
    </style>
    <meta charset="utf-8" />

  </head>
  <body>
    <script>
      var bubbles = [];

      function setup() {
        createCanvas(700, 700);
  
       for (var i = 0; i < 22; i++) {
        bubbles.push({
         x: random(width),
         y: random(height),
         radius: random(50, 50)
        });
       }
      }

      function draw() {
        background(255);
 
        for (var i = 0; i < bubbles.length; i++) {
        var bubble = bubbles[i];
  
        if (dist(mouseX, mouseY, bubble.x, bubble.y) < bubble.radius) {
         
          fill(100, 100, 200, 200);
        } else
        {
         fill(100, 100, 200, 200);
          noStroke();
        }
 

      
        ellipse(bubble.x, bubble.y, bubble.radius*2);
        bubble.x += random(-1,2);
        bubble.y += random(-1,2);
     
     
       }
        
        if (dist(mouseX, mouseY, bubble.x, bubble.y) > bubble.radius) {
         if (mouseIsPressed) {
           bubbles.push({
           x: mouseX,
           y: mouseY,
           radius: random(50, 50)
          }); 
          }
        } 
    }
    </script>
  </body>
</html>
