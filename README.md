# E4
float x = 0;//movimiento
float y= 5;//velocidad
float o=0;
int k=30;
//float c=random(0, 250);
float p;
float col;
color colorsh;
//PImage webimg;
//PImage webimg2;
PImage img;
PImage img2;


void setup() {
  size (510, 600);
  background (190, 204, 211);
  noCursor();
  //String url= "https://s-media-cache-ak0.pinimg.com/736x/24/eb/41/24eb41c313ea216a6bf02cdc81016235.jpg";
  //String url2 = "https://68.media.tumblr.com/4923aa534ec2772448a8bcdfb15ed308/tumblr_oo5xc8OP3V1sqv7x1o1_250.png";
  //webimg= loadImage(url);
  //webimg2=loadImage(url2);

  img= loadImage("lemonet.jpg"); 
  img2= loadImage("claude-monet.png");
}

////////////////////////////////////////////

void draw() {

  if (mousePressed == true) {
    background(255);
    tint(255, 30);// r, g,b 

    for ( int i=0; i<5; i ++) {
      image(img, i*10, 0, 520, 610); //poner imagen en la posoción x,y
    }

    textSize(20);
    smooth();
    fill(255);
    text("Mantén presionado el mouse", 110, 560);
  } else { 
    background(255);
    tint(255, 150);// r, g,b 
    image(img, 0, 0, 520, 610);
    textSize(20);
    smooth();
    fill(255);
    text("Mantén presionado el mouse", 110, 560);
  }

  ///// pelotitas fondo

  if (mousePressed ==true) {
    p=random(0, 20);
    //col=random(0, 255);
    // fill(mouseX, col, mouseY);
    fill(255, 255, 255, 180);
  } else {
    p= 0;
    fill(255, 255, 255, 180);
  }

  noStroke();
  // bolitas fondo

  for ( int al = 10; al< 510; al+=80) {
    for (int an = 10; an<550; an+=80) {
      ellipse(an+p, al+p, 10, 10);
    }
  }

  for ( int al = 40; al< 510; al+=80) {
    for (int an = 40; an<550; an+=80) {
      ellipse(an+p, al+p, 10, 10);
    }
  }


  /////////////////

  // cuerpo
  noStroke();
  fill(247, 244, 240);
  quad(250, 146, 377, 238, 250, 412, 127, 257);
  quad(127, 257, 250, 412, 194, 412, 86, 299);
  quad(86, 299, 194, 412, 142, 423, 50, 351);
  quad(50, 351, 142, 423, 56, 418, 39, 392);
  quad(377, 238, 387, 288, 378, 411, 250, 412);

  //sombra cuello
  fill(237, 232, 226);
  quad(154, 232, 140, 245, 166, 266, 188, 232);
  quad(166, 266, 188, 232, 244, 232, 240, 281);
  quad(244, 232, 240, 281, 299, 274, 299, 232);
  quad(299, 274, 299, 232, 325, 232, 346, 263);
  quad(325, 232, 346, 263, 377, 238, 368, 228);

  //sombra pata izq
  //fill(235,236,237);
  fill(237, 232, 226);
  quad(56, 418, 101, 386, 68, 382, 53, 414);
  triangle(101, 386, 56, 418, 142, 423);
  quad(101, 386, 142, 423, 148, 421, 142, 389);
  triangle(142, 389, 68, 382, 100, 361);

  //pata izq
  fill(247, 244, 240);
  triangle(100, 366, 139, 392, 70, 387);
  quad(139, 392, 146, 431, 50, 423, 70, 387);
  quad(146, 431, 53, 468, 45, 444, 50, 423);
  quad(146, 431, 139, 472, 100, 487, 53, 468);

  //sombra pataderecha
  fill(237, 232, 226);
  quad(263, 411, 378, 411, 362, 351, 292, 381);
  triangle(378, 411, 362, 351, 382, 357);

  //pata derecha
  fill(247, 244, 240);
  quad(274, 411, 296, 385, 365, 357, 327, 444);
  quad(365, 357, 380, 361, 395, 397, 327, 444);
  triangle(395, 397, 428, 431, 327, 444);
  triangle(428, 431, 395, 397, 327, 444);
  triangle(428, 431, 460, 444, 475, 488);
  triangle(327, 444, 393, 491, 428, 431);
  quad(428, 431, 475, 488, 421, 500, 393, 491);

  //detalles patas 
  fill(237, 232, 226); //derecha
  triangle(56, 470, 60, 471, 60, 450);
  triangle(86, 481, 92, 484, 89, 458);
  triangle(107, 485, 110, 483, 107, 467);
  triangle(131, 475, 134, 474, 130, 467);

  quad(66, 347, 101, 340, 132, 347, 102, 334);
  triangle(142, 370, 154, 397, 166, 392);
  quad(154, 397, 166, 392, 169, 417, 154, 420);

  triangle(348, 458, 351, 443, 351, 461);//izq
  quad(401, 493, 406, 496, 415, 470, 413, 485);
  triangle(436, 496, 441, 495, 443, 477);
  triangle(453, 492, 457, 492, 457, 483);

  //cabeza atras 
  fill(247, 244, 240);

  quad(250, 45, 180, 60, 131, 155, 250, 155);
  quad(250, 45, 315, 45, 376, 114, 250, 155);
  quad(376, 114, 398, 171, 395, 209, 250, 155);
  quad(131, 155, 131, 197, 144, 227, 250, 155);
  quad(144, 227, 186, 247, 250, 250, 250, 155);
  quad(250, 250, 351, 239, 395, 209, 250, 155);

  //orejas 
  //izq

  if (mousePressed ==true) {

    //oreja izq
    fill(247, 244, 240);
    triangle(189, 23, 158, 38, 174, 15);
    quad(151, 118, 199, 66, 189, 23, 158, 38);
    fill(239, 218, 229);
    triangle(188, 28, 161, 39, 174, 21);
    quad(156, 121, 197, 67, 188, 28, 161, 39);
    //dercha
    fill(247, 244, 240);
    triangle(360, 21, 324, 15, 342, 4);
    quad(315, 45, 376, 114, 360, 21, 324, 15);
    fill(239, 218, 229);
    triangle(356, 22, 326, 18, 342, 10);
    quad(315, 58, 368, 117, 356, 22, 326, 18);
  } else {

    //oreja izq
    fill(247, 244, 240);
    triangle(140, 24, 133, 42, 158, 24);
    quad(133, 42, 160, 126, 199, 60, 158, 24);
    fill(239, 218, 229);
    triangle(136, 44, 142, 28, 159, 28);
    quad(136, 44, 159, 28, 197, 61, 161, 122);

    //dercha
    fill(247, 244, 240);
    triangle(369, 4, 351, 8, 380, 19);
    quad(351, 8, 380, 19, 369, 121, 295, 65);
    fill(239, 218, 229);
    triangle(367, 8, 377, 23, 350, 13);
    quad(377, 23, 350, 13, 296, 67, 367, 119);
  }


  //cara detras ojos
  fill(237, 232, 226);

  triangle(199, 56, 250, 110, 150, 130);
  quad(150, 130, 250, 110, 250, 200, 196, 200);
  triangle(150, 130, 196, 200, 144, 149);
  quad(250, 200, 327, 201, 375, 145, 250, 145);
  quad(250, 145, 375, 145, 374, 123, 250, 110);
  triangle(250, 110, 374, 123, 303, 45);

  //detras puente nariz
  fill(242, 237, 231);
  quad(250, 181, 250, 131, 279, 102, 301, 184);
  quad(279, 102, 301, 184, 324, 174, 304, 98);
  quad(324, 174, 304, 98, 332, 113, 344, 156);
  triangle(332, 113, 344, 156, 345, 131);

  quad(250, 181, 250, 131, 230, 106, 193, 179);
  quad(230, 106, 193, 179, 176, 168, 205, 102);
  quad(176, 168, 205, 102, 184, 110, 171, 151);
  triangle(184, 110, 171, 151, 169, 132);

  // entre ojos 
  fill(247, 244, 240);
  triangle(250, 147, 222, 117, 277, 118);
  quad(222, 117, 277, 118, 274, 98, 225, 98);
  quad(225, 98, 250, 98, 250, 45, 195, 56);
  quad(250, 98, 274, 98, 315, 45, 250, 45);

  //parte atras boca
  fill(224, 214, 198);
  triangle(250, 235, 276, 224, 250, 194);
  triangle(250, 194, 223, 224, 250, 235);

  //boca
  fill(170, 166, 162);
  triangle(250, 205, 265, 214, 250, 197);
  triangle(250, 197, 234, 214, 250, 205);

  //partes redonditas
  fill(235, 236, 237);
  quad(190, 191, 189, 209, 222, 227, 214, 175);
  quad(214, 175, 222, 227, 250, 200, 250, 180);
  quad(250, 180, 250, 200, 277, 227, 285, 175);
  quad(285, 175, 309, 190, 310, 209, 277, 227);

  //nariz
  fill(116, 89, 87);
  stroke(116, 89, 87);
  strokeWeight(1);
  triangle(230, 178, 269, 179, 250, 200);
  quad(230, 178, 269, 179, 263, 171, 236, 171);

  noStroke();
  fill(237, 232, 226);
  triangle(250, 174, 247, 171, 252, 171);

  //orificios
  fill(10);
  noStroke();
  triangle(233, 181, 239, 181, 241, 190);
  triangle(267, 181, 260, 181, 258, 190);

  //puente nariz
  fill(247, 244, 240);
  quad(236, 171, 263, 171, 269, 159, 230, 159); 
  quad(269, 159, 230, 159, 234, 148, 266, 148);
  triangle(234, 148, 266, 148, 250, 137);

  //ojo derecho
  fill(82, 154, 204);
  stroke(82, 154, 204);
  strokeWeight(1);
  triangle(183, 131, 198, 123, 186, 145);
  quad(198, 123, 186, 145, 197, 154, 212, 125);
  quad(197, 154, 212, 125, 222, 135, 209, 157);
  triangle(222, 135, 209, 157, 228, 151);

  fill(50);
  noStroke();
  ellipse(205, 140, 30, 30);

  //ojo izq
  fill(82, 154, 204);
  stroke(82, 154, 204);
  strokeWeight(1);
  triangle(278, 150, 298, 153, 280, 134);
  quad(298, 153, 280, 134, 291, 121, 312, 151);
  quad(291, 121, 312, 151, 321, 142, 308, 118);
  triangle(321, 142, 308, 118, 324, 125);

  fill(50);
  noStroke();
  ellipse(301, 136, 32, 32);

  //m de buda
  fill(235, 236, 237);
  triangle(225, 50, 236, 48, 242, 88);
  triangle(269, 45, 281, 45, 263, 86);


  if (mousePressed==false) {

    //bigotes
    stroke(180);
    line(109, 197, 208, 184);
    line(114, 223, 203, 191);
    line(132, 229, 208, 191);
    line(166, 260, 216, 200);
    line(168, 281, 211, 211);
    line(192, 266, 216, 211);
    line(281, 204, 307, 259);
    line(287, 204, 324, 274);
    line(293, 197, 393, 245);
    line(293, 189, 400, 197);
    line(281, 184, 391, 187);
  } else if (mousePressed== true) {

    x=x+y;
    stroke(150);
    line(109, 197+x, 208, 184);
    line(114, 223+x, 203, 191);
    line(132, 229+x, 208, 191);
    line(166, 260+x, 216, 200);
    line(168, 281+x, 211, 211);
    line(192, 266+x, 216, 211);

    line(281, 204, 307, 259+x);
    line(287, 204, 324, 274+x);
    line(293, 197, 393, 245+x);
    line(293, 189, 400, 197+x);
    line(281, 184, 391, 187+x);

    if ( (x > 40) || (x<-60))
    {
      y=y*-1;
    }
  }

  if (mouseX<100) {
    colorsh = color(19, 24, 98);
  } else if ((mouseX<200) && (mouseX>100)) {
    colorsh = color(46, 68, 130);
  } else if ((mouseX<300) && (mouseX>200)) {
    colorsh = color(84, 107, 171);
  } else if ((mouseX<400) && (mouseX>300)) {
    colorsh = color(135, 136, 156);
  } else if ((mouseX<550) && (mouseX>400)) {
    colorsh = color(190, 169, 222);
  }




  if (mousePressed==true) {
    o=o+1;//var ojos
    if ( o > 20 )
    {
      o=o*-1;
    }

    //ojo derecho
    fill(colorsh);
    stroke(colorsh);
    strokeWeight(1);
    strokeCap(ROUND);
    triangle(183, 131, 198, 123, 186, 145);
    quad(198, 123, 186, 145, 197, 154, 212, 125);
    quad(197, 154, 212, 125, 222, 135, 209, 157);
    triangle(222, 135, 209, 157, 228, 151);

    fill(50);
    noStroke();
    ellipse(205, 140, 10+o, 30);

    //ojo izq
    fill(colorsh);
    stroke(colorsh);
    strokeWeight(1);
    triangle(278, 150, 298, 153, 280, 134);
    quad(298, 153, 280, 134, 291, 121, 312, 151);
    quad(291, 121, 312, 151, 321, 142, 308, 118);
    triangle(321, 142, 308, 118, 324, 125);

    fill(50);
    noStroke();
    ellipse(301, 136, 10+o, 32);
  }

  ////////////////////// cursor


  if (mousePressed== true) {
    /*stroke(0, 0, 0, 100);
     strokeWeight(5);
     fill(250, 0, 0, 230);
     ellipse(mouseX, mouseY, k, k);
     println("dibujando"); //se ve en la pantallita de abajo saber donde hay un error 
     println(frameCount); //contador de cuadros
     fill(mouseX,p,mouseY);*/
    tint(255, 240);
    image(img2, mouseX, mouseY, 50, 50);
    fill(255);
    text("Mantén presionado el mouse", 110, 560);
  } else {
    stroke(0, 0, 0, 100);
    strokeWeight(5);
    fill(0, 0, 0, 150);
    ellipse(mouseX, mouseY, k, k);
    println("dibujando"); //se ve en la pantallita de abajo saber donde hay un error 
    println(frameCount); //contador de cuadros
  }

  frameRate(50);
}
