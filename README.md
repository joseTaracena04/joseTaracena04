int x = 0;
int y = 0;
int speed = 5;

void setup() {
  size(400, 400);
  background(255);
}

void draw() {
  // Dibujar un círculo que sigue el mouse
  fill(0);
  ellipse(mouseX, mouseY, 50, 50);
  
  // Dibujar una línea que sigue el mouse
  stroke(0);
  line(mouseX, mouseY, pmouseX, pmouseY);
  
  // Dibujar un rectángulo que se mueve con las teclas del teclado
  if (keyPressed) {
    if (keyCode == UP) {
      y -= speed;
    } else if (keyCode == DOWN) {
      y += speed;
    } else if (keyCode == LEFT) {
      x -= speed;
    } else if (keyCode == RIGHT) {
      x += speed;
    }
  }
  fill(255, 0, 0);
  rect(x, y, 50, 50);
}

void mousePressed() {
  // Cambiar el color de fondo al hacer clic en el mouse
  background(random(255), random(255), random(255));
}
