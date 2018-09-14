# hm1




      var bubbles = [];

      function setup() {
        createCanvas(700, 700);
  
      	for (var i = 0; i <22; i++) {
      		bubbles.push({
      			x: random(width),
      			y: random(height),
      			radius: random(50, 50)
      		});
      	}
        
        if (mouseIsPressed){
          ellipse (mouseX, mouseY, r);
          
      }
      }

      function draw() {
        background(255);
	
        for (var i = 0; i < bubbles.length; i++) {
      		var bubble = bubbles[i];
		
          if (dist(mouseX, mouseY, bubble.x, bubble.y) > bubble.radius) {
         if (mouseIsPressed) {
          bubbles.push({
         x: mouseX,
         y: mouseY,
         radius: random(50, 50)
        }); // remove this bubble!
         }
         fill(100, 100, 200, 200);
        } else {
         fill(100, 100, 200, 200);
          noStroke();
        }
 

      
          ellipse(bubble.x, bubble.y, bubble.radius*2);
        bubble.x += random(-1,2);
        bubble.y += random(-1,2);
     
     
       }
    }
    </script>
  </body>
</html>
