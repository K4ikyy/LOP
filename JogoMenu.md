// DECLARANDO AS VARIAVÉIS

var tela = 0;

let imgFundoI;
let imgKaiky;
let imgOrivaldo;
let fonte;
let fonte2;

//CARREGANDO IMAGENS E FONTES USADAS NO JOGO

function preload() {
  imgFundoI = loadImage ('blackboard-g8e259cb45_1920 (1).jpg');
  imgKaiky = loadImage('KaikyHanry.jpg');
  imgOrivaldo = loadImage('orivaldo.png');
  fonte = loadFont ('Bungee-Regular.ttf');
  fonte2 = loadFont ('editundo.ttf');
}

function setup() {
  createCanvas(500, 400);                                 //DIMENSÕES DA TELA
} 

function draw() {
  
// CÓDIGO DA TELA INICIAL
  
  if (tela === 0) {
    background(imgFundoI);                                //IMAGEM DE FUNDO

    fill(255,255,0);
    textAlign(CENTER);
    textSize(60);
    textFont(fonte);                                      //MONTANDO O TÍTULO
    text("PENSA ", 250, 100);
    text("RÁPIDO ", 250, 165);
    
    strokeWeight(3);                                      //COLOCANDO BORDAS NOS BOTÕES
    
    fill(255);
    if (mouseX >= 150 && mouseX <= 350 && mouseY >= 190 && mouseY <= 240) {
      fill(255, 255, 75);                                 //MUDAR A COR CASO O MOUSE PASSE EM CIMA
    }
    rect(150, 190, 200, 50, 15);                          // BOTÃO DE JOGAR
    
    fill(20);
    textAlign(CENTER);
    textSize(35);
    textFont(fonte2)
    text("JOGAR", 250, 226);

    fill(255);
    if (mouseX >= 150 && mouseX <= 350 && mouseY >= 250 && mouseY <= 300) {
      fill(255, 255, 75);                                 //MUDAR A COR CASO O MOUSE PASSE EM CIMA
    }
    rect(150, 250, 200, 50, 15);                          //BOTÃO DE CRÉDITOS

    fill(20);
    textAlign(CENTER);
    textSize(32);
    text("CRÉDITOS", 251, 285);
  }
  
// CÓDIGO DA TELA DE INTRUÇÕES
  
  else if (tela == 1) {
    background(imgFundoI);
    
    textAlign(CENTER);
    textSize(23);
    text("Para jogar, basta você utilizar o", 250,120);
    text("mouse e escolher a resposta correta", 250,150);
    text("para a expressão que vai aparecer na",250,180);
    text("sua tela. Só cuidado para não errar...", 250,210);
    
    fill(255,255,0);
    textAlign(CENTER);
    textSize(28);
    text("PENSE RÁPIDO E VAMOS LÁ!!!", 250, 250);
    
    strokeWeight(3);
    fill(255);
    rect(115,29,270,50,10);
    
    fill(10);
    textAlign(CENTER);
    textSize(40);
    text("COMO JOGAR?", 250, 70);
    
    strokeWeight(3);
    
    fill(255);
    if (mouseX >= 170 && mouseX <= 330 && mouseY >= 278 && mouseY <= 323) {
      fill(255, 255, 75);
    }
    rect(170, 278, 160, 45, 15);                               //BOTÃO DE JOGAR
    
    fill(10);
    textAlign(CENTER);
    textSize(35);
    text("JOGAR", 250, 311);
    
    fill(255);
    if (tela == 1 && mouseX >= 25 && mouseX <= 105 && mouseY >= 35 && mouseY <= 75) {
    fill(255,255,72);
    }
    rect(25, 35, 80, 40, 10);                                  //BOTÃO DE VOLTAR
    
    strokeWeight(1);
    
    fill(10);
    textAlign(CENTER);
    textSize(21);
    text("VOLTAR", 64, 63);
  }
  
  //CÓDIGO DA TELA DE CRÉDITOS
  
  else if (tela == 2) {
    background(imgFundoI);
    image(imgKaiky, 35, 100);                                   //DESCARREGANDO IMAGENS
    image(imgOrivaldo,35,220);
    
    strokeWeight(3);
    fill(255);
    rect(150,29,200,50,10);
    
    strokeWeight(1);
    
    fill(20);
    textAlign(CENTER);
    textSize(40);
    text("CRÉDITOS",250,70);
    
    fill(20);
    textAlign(CENTER);
    textSize(20);
    text("Desenvolvedor: Kaiky Fernandes", 291, 118);
    text("Curso: Bacharelado em", 250, 140);
    text("Ciências e Tecnologia.", 245, 160);
    
    fill(20);
    textAlign(CENTER);
    textSize(20);
    text("Orientador: Orivaldo Vieira", 270, 240);
    text("Docente da Universidade Federal", 299, 260);
    text("do Rio Grande do Norte.", 258, 278);
    
    strokeWeight(3);
    
    fill(255);
    if (mouseX >= 30 && mouseX <= 110 && mouseY >= 35 && mouseY <= 75) {
      fill(255, 255, 75);
    }
    rect(30, 35, 80, 40, 10);                                       //BOTÃO DE VOLTAR

    fill(10);
    textAlign(CENTER);
    textSize(21);
    text("VOLTAR", 69, 63);
  }
  
  //CÓDIGO DA TELA DE EXEMPLO DO JOGO
  
  else if (tela == 3) {
    background(imgFundoI);
    
    textAlign(CENTER);
    textSize(45);                                            //EXPRESSÃO PROBLEMA
    text("2 + 2 x 4 - 1", 250,100);
    
    strokeWeight(3);
                                                            //DECLARANDO AS ALTERNATIVAS DE RESPOSTA
    fill(255);
    if (tela == 3 && mouseX >= 70 && mouseX <= 220 && mouseY >= 180 && mouseY <= 230) {
      fill(255, 255, 75);
    }
    rect(70, 180, 150, 50, 15);
    
    fill(10);
    textAlign(CENTER);
    textSize(35);
    text("9", 145, 216);
    
    fill(255);
    if (tela == 3 && mouseX >= 230 && mouseX <= 380 && mouseY >= 180 && mouseY <= 230) {
      fill(255, 255, 75);
    }
    rect(230, 180, 150, 50, 15);
    
    fill(10);
    textAlign(CENTER);
    textSize(35);
    text("8", 302, 215);
    
    fill(255);
    if (tela == 3 && mouseX >= 70 && mouseX <= 220 && mouseY >= 250 && mouseY <= 300) {
      fill(255, 255, 75);
    }
    rect(70, 250, 150, 50, 15);
    
    fill(10);
    textAlign(CENTER);
    textSize(35);
    text("15", 145, 285);
    
    fill(255);
    if (tela == 3 && mouseX >= 230 && mouseX <= 380 && mouseY >= 250 && mouseY <= 300) {
      fill(255, 255, 75);
    }
    rect(230, 250, 150, 50, 15);
    
    fill(10);
    textAlign(CENTER);
    textSize(35);
    text("12", 304, 285);
    }
  
  // TELA DE CONTINUAÇÃO DO JOGO
  
  else if (tela == 4) {
    background(imgFundoI);
    
    fill(255);
    textAlign(CENTER);
    textSize(70);
    text("NEXT LEVEL", 250, 200);
  }
  
  // TELA EM CASO DE ERRO
  
  else if (tela == 99) {
    background(255,0,20);
    
    fill(10);
    textAlign(CENTER);
    textSize(65);
    text("VOCÊ PERDEU!",250,165);
    
    fill(255);
    if (tela == 99 && mouseX >= 100 && mouseX <= 400 && mouseY >= 200 && mouseY <= 250) {
      fill(0, 255, 20);
    }
    rect(100, 200, 300, 50, 15);                                    //BOTÃO PARA JOGAR NOVAMENTE
    
    fill(10);
    textAlign(CENTER);
    textSize(35);
    text("JOGAR NOVAMENTE", 250,235);
  }
}

//FUNÇÕES DO CLIQUE DO MOUSE NO JOGO

function mouseClicked() {
  if (tela == 0 && mouseX >= 150 && mouseX <= 350 && mouseY >= 190 && mouseY <= 240) {
    tela = 1;
  }
  if (tela == 0 && mouseX >= 150 && mouseX <= 350 && mouseY >= 250 && mouseY <= 300) {
    tela = 2;
  }
  if (tela == 1 && mouseX >= 25 && mouseX <= 105 && mouseY >= 35 && mouseY <= 75) {
    tela = 0;
  }
  if (tela == 1 && mouseX >= 170 && mouseX <= 330 && mouseY >= 278 && mouseY <= 323) {
    tela = 3;
  }
  if (tela == 2 && mouseX >= 30 && mouseX <= 110 && mouseY >= 35 && mouseY <= 75) {
    tela = 0;
  }
  if (tela == 3 && mouseX >= 70 && mouseX <= 220 && mouseY >= 180 && mouseY <= 230) {
    tela = 4;
  }
  if (tela == 3 && mouseX >= 230 && mouseX <= 380 && mouseY >= 180 && mouseY <= 230) {
    tela = 99;
  }
  if (tela == 3 && mouseX >= 70 && mouseX <= 220 && mouseY >= 250 && mouseY <= 300) {
    tela = 99;
  }
  if (tela == 3 && mouseX >= 230 && mouseX <= 380 && mouseY >= 250 && mouseY <= 300) {
    tela = 99;
  }
  if (tela == 99 && mouseX >= 100 && mouseX <= 400 && mouseY >= 200 && mouseY <= 250) {
    tela = 0;
  }
}
