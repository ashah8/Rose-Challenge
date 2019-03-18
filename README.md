# Rose-Challenge


I made the change which was colour.I will do more in the weekend but the period ended.

My Code

var d = 8;
var n = 5;
var sliderD;
var sliderN;

function setup() {
  createCanvas(400, 400);
	sliderD = createSlider(1, 10, 5, 0.1);
	sliderN = createSlider(1, 10, 5, 0.1);
}


function draw() {
	d = sliderD.value();
	n = sliderN.value();
	var k = n / d;
  background(51);
	translate(width / 2, height / 2);
	
	beginShape();
	stroke(255);
	noFill();
	fill(20, 20, 30);
	strokeWeight(1);
	for (var a = 0; a < TWO_PI * 8; a += 0.01) {
		var r = 200 * cos(k*a);
		var x = r * cos(a);
		var y = r * sin(a);
		stroke(255);
		strokeWeight(4);
		vertex(x, y);
	}
	endShape(CLOSE);
}
