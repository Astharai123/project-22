
const Engine = Matter.Engine;
const World = Matter.World;
const Bodies = Matter.Bodies;
const Body = Matter.Body;

var enging,world;

function setup() {
	createCanvas(800, 700);


	engine = Engine.create();
	world = engine.world;

	//Create the Bodies Here.
 pepar=nawPepar (109,600,10);
 ground=nawGround(400,680,800,20);
 leftside=nawdastbin(550,620,20,100);
 bottom=nawdastbin(610,660.100,20);
 rigthside=nawdastbin(670,620,20,100);
	Engine.run(engine);
  
}


function draw() {
  rectMode(CENTER);
  background(0);
  Engine.update(enging);
  pepar.display();
  ground.display();
  liftside.display();
  dottom.display();
  rigthside.display();
  drawSprites();
 
}

function keypressed(){
if(keypressed===UP_ARROW){
Matter.body.appForcex=15,y=-15;
}
}

