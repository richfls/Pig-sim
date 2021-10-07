//2D matrix in SFML
#include<iostream>
using namespace std;
#include "SFML/Graphics.hpp"
class goatty {
private: //private variables can only be seen/used by members of the class
	int xpos;
	int ypos;
	bool isWalking;
	bool isAsleep;
	bool willBaa;
	int number;
public: //can be seen and used by everything in your program
	goatty(); //default constructor: initalizes all the variables in your pig
	goatty(int num); //parameterized constructor
	void walk();
	void sleep();
	void draw();
	void baa();
};//---------------------------------------------------------
//class definition-------------------------------------------
class piggy {
private: //private variables can only be seen/used by members of the class
	int xpos;
	int ypos;
	bool isWalking;
	bool isAsleep;
	bool willOink;
	int number;
public: //can be seen and used by everything in your program
	piggy(); //default constructor: initalizes all the variables in your pig
	piggy(int num); //parameterized constructor
	void walk();
	void sleep();
	void draw();
	void oink();
};//---------------------------------------------------------
int main() {
	piggy p1(1); //instantiate a pig object
	piggy p2(2);
	goatty g3(1);
	sf::RenderWindow renderWindow(sf::VideoMode(800, 800), "loading images"); //set up screen
	sf::Event event; //set up event queue

	//Here's how to load an image: clicke file->save as to see where to store "dog.png"
	sf::Texture img1;
	if (!img1.loadFromFile("Image.png")) return 0; //this line loads the image AND kills your program if it doesn't load
	sf::Sprite pic1;
	pic1.setTexture(img1);
	while (renderWindow.isOpen()) {//keep window open until user shuts it down

		while (renderWindow.pollEvent(event)) { //look for events-----------------------

			//this checks if the user has clicked the little "x" button in the top right corner
			if (event.type == sf::Event::EventType::Closed)
				renderWindow.close();
			cout << "1";
			p1.walk();
			cout << "2";
			p1.draw();
			cout << "3";
			p2.walk();
			p2.draw();
			g3.walk();
			g3.draw();

		}
		}//end event loop----------------------------------



}
piggy::piggy() {
	xpos = rand() % 600 + 100;
	ypos = rand() % 600 + 100;
	isAsleep = false;
	isWalking = true;
}
piggy::piggy(int num) {
	xpos = rand() % 600 + 100;
	ypos = rand() % 600 + 100;
	isAsleep = false;
	isWalking = true;
	number = num;
}
void piggy::walk() {
	//randomly move in one of 8 directions when isWalking is true
	if (isWalking == true) {
		xpos += rand() % 10 - 5;
		ypos += rand() % 10 - 5;
		int off = rand() % 100 + 1;
		oink();

		if (off < 30) { //30% chance walking will turn off each turn
			isWalking = false;
			cout << "stopping!" << endl;
		}

		if (xpos >= 799) {
			xpos = 799;
		}

		if (xpos <= 1) {
			xpos = 1;
		}

		if (ypos >= 799) {
			ypos = 799;
		}

		if (ypos <= 1) {
			ypos = 1;
		}
	}
	else {
		sleep();
	}
	//10% chance any turn that isWalking will turn ON
	int num = rand() % 100 + 1;
	if (num < 30 and isWalking == false and isAsleep == false) {
		isWalking = true;
		cout << "walking!" << endl;
	}
}
void piggy::sleep() {
	//you do this one
	int num = rand() % 100 + 1;
	if (num < 50) {
		isAsleep = true;
	}
	else {
		isAsleep = false;
	}
}
void piggy::oink() {
	int num = rand() % 100 + 1;
	if (num < 10) {
		willOink = true;
	}
	else {
		willOink = false;
	}
}
void piggy::draw() {
	//eventually this will hold drawing functions to make it graphical
	cout << "Hello I am pig # " << number << endl;
	if (willOink == true) cout << "Oink!" << endl;
	cout << "My position is " << xpos << " , " << ypos << endl;
	cout << "I am ";
	if (isAsleep == true) cout << " asleep, and";
	else cout << " not asleep, and";
	if (isWalking == true) cout << " walking." << endl;
	else cout << " not walking." << endl;
	//system("pause");
}
//class function definitions AND standalone function definitions go here
goatty::goatty() {
	xpos = rand() % 600 + 100;
	ypos = rand() % 600 + 100;
	isAsleep = false;
	isWalking = true;
}
goatty::goatty(int num) {
	xpos = rand() % 600 + 100;
	ypos = rand() % 600 + 100;
	isAsleep = false;
	isWalking = true;
	number = num;
}
void goatty::walk() {
	//randomly move in one of 8 directions when isWalking is true
	if (isWalking == true) {
		xpos += rand() % 10 - 5;
		ypos += rand() % 10 - 5;
		int off = rand() % 100 + 1;
		baa();

		if (off < 30) { //30% chance walking will turn off each turn
			isWalking = false;
			cout << "stopping!" << endl;
		}

		if (xpos >= 799) {
			xpos = 799;
		}

		if (xpos <= 1) {
			xpos = 1;
		}

		if (ypos >= 799) {
			ypos = 799;
		}

		if (ypos <= 1) {
			ypos = 1;
		}
	}
	else {
		sleep();
	}
	//10% chance any turn that isWalking will turn ON
	int num = rand() % 100 + 1;
	if (num < 30 and isWalking == false and isAsleep == false) {
		isWalking = true;
		cout << "walking!" << endl;
	}
}
void goatty::sleep() {
	//you do this one
	int num = rand() % 100 + 1;
	if (num < 50) {
		isAsleep = true;
	}
	else {
		isAsleep = false;
	}
}
void goatty::baa() {
	int num = rand() % 100 + 1;
	if (num < 10) {
		willBaa = true;
	}
	else {
		willBaa = false;
	}
}
void goatty::draw() {
	
	//eventually this will hold drawing functions to make it graphical
	cout << "Hello I am goat # " << number << endl;
	if (willBaa == true) cout << "Baa!" << endl;
	cout << "My position is " << xpos << " , " << ypos << endl;
	cout << "I am ";
	if (isAsleep == true) cout << " asleep, and";
	else cout << " not asleep, and";
	if (isWalking == true) cout << " walking." << endl;
	else cout << " not walking." << endl;
	system("pause");
}
