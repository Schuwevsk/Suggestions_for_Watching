# 🥤Suggestions_for_Watching🍕
🎃Here, I created a suggestor for movie and series. Don't is very nice, but I tried and strived me for let functional.


let ageInput;    // variáveis para o setup.
let genreInput1; // variáveis para o setup.
let genreInput2; // variáveis para o setup.

function setup() {
  createCanvas(800, 600);
  createElement("h2","Quer uma Recomendação?"); //título.
  createSpan("Minha Idade:");                   //na caixa de texto.
  ageInput = createInput();
  genreInput1 = createCheckbox("Gosto de Fantasia");
  genreInput2 = createCheckbox("Gosto de Romance");
}

function draw() {
  background(0);
  fill("white");
  let age = ageInput.value();              //verificação dos dados.
  let likeFantasy = genreInput1.checked(); //verificação dos dados.
  let likeRomance = genreInput2.checked(); //verificação dos dados.
  let suggestion = runSuggestion(age,likeFantasy,likeRomance);
  text(suggestion, width /2, height / 2);
  textAlign(CENTER,CENTER);
  textSize(50);
}

//gerar recomendações (condicionais).
function runSuggestion (age,likeFantasy,likeRomance) {
  if (age >= 10) {
  if (age >= 12) {
  if (age >= 14) {
  if (age >= 16) {
  if (age >= 18) {
    if (likeFantasy || likeRomance){
    return "The Witcher";
  } else {
    return "Sex/Life";
  }
  } else {
   if(likeFantasy || likeRomance){
    return "Jujutsu Kaisen"; 
  } else {
    return "50 Gray";
  }
  }
  } else {
    if (likeFantasy || likeRomance){
      return "Lords of The Rings";
  } else {
    return "Tonikawa";
  }
  }
  } else {
   if (likeFantasy || likeRomance) {
    return "Spider-Man Into The Spiderverse";
  } else{
    return "Kaguya-Sama";
  }
  }
  } else {
  if (likeFantasy || likeRomance) {
    return "Dragon Ball GT";
  } else {
     return "Your Name";
  }
  }
  }
  else {
  return "Cars";
}
}


html, body {
  margin: 20px;
  padding: 0;
  background-color: rgb(140,140,140)
}
canvas {
  display: block;
}
