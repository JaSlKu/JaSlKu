- 👋 Hi, I’m @JaSlKu
- 👀 I’m interested in Linux, c++ and breaking OSs, codes and similar
- 🌱 I’m currently learning c++, Linux
- 💞️ I’m looking to collaborate on idk
- 📫 How to reach me: do not
- 😄 Pronouns: he/class
- ⚡ Fun fact: ...

// chess.cpp : Tento soubor obsahuje funkci main. Provádění programu se tam zahajuje a ukončuje.
//

#include <iostream>


std::string pieces = "VJSDKSJV";
std::string bpieces = "VJSKDSJV";

struct p {
    int x;
    int y;
};



enum color {
    white=1,
    black=0
};
char Board[8][8];
void Player(color clr);
void genBoard();
void printBoard();
void move();

int main()
{
    genBoard();
    Player(black);
    while (true) {
        printBoard();
    }
    
    
}

void genBoard() {
    for (int x = 0; x < 8; x++) {
        for (int y = 0; y < 8; y++) {
            Board[x][y] = '0';
        }
    }
}

void printBoard() {
    std::cout << "\033[H\033[?25l";
    for (int x = 0; x < 8; x++) {
        for (int y = 0; y < 8; y++) {
            std::cout << Board[x][y] << " ";
        }
        std::cout << "\n";
    }
}

void Player(color clr) {
    if (clr == white) {
        for (int i = 0; i < 8; i++) {
            Board[7][i] = pieces[i];
            Board[6][i] = 'p';
            Board[0][i] = pieces[i];
            Board[1][i] = 'p';
        }
    }
    else if (clr == black) {
        for (int i = 0; i < 8; i++) {
            Board[7][i] = bpieces[i];
            Board[6][i] = 'p';
            Board[0][i] = bpieces[i];
            Board[1][i] = 'p';
        }
    }
}


void move(){
    /// TOP SECRET
    extern p a1; extern p  a2; extern p a3; extern p a4, extern p a5, extern p a6, extern p a7, extern p a8,
          extern p b1, extern p  b2, extern p  b3, extern p  b4, extern p b5, extern p  b6, extern p  b7, extern p  b8,
          extern p c1, extern p  c2, extern p  c3, extern p  c4, extern p  c5, extern p  c6, extern p  c7, extern p  c8,
          extern p d1, extern p  d2, extern p  d3, extern p  d4, extern p  d5, extern p  d6, extern p  d7, extern p  d8,
          extern p e1, extern p  e2, extern p  e3, extern p  e4, extern p  e5, extern p  e6, extern p  e7, extern p  e8,
          extern p f1, extern p  f2, extern p  f3, extern p  f4, extern p  f5, extern p  f6, extern p  f7, extern p  f8,
          extern p g1, extern p  g2, extern p  g3, extern p  g4, extern p  g5, extern p  g6, extern p  g7, extern p  g8,
          extern p h1, extern p h2, extern p  h3, extern p  h4, extern p  h5, extern p  h6, extern p  h7, extern p  h8;

      a1.x = 0; a1.y = 0;a2.x = 1; a2.y = 0;a3.x = 2; a3.y = 0;a4.x = 3; a4.y = 0;a5.x = 4; a5.y = 0;a6.x = 5; a6.y = 0;a7.x = 6; a7.y = 0;a8.x = 7; a8.y = 0;
    b1.x = 0; b1.y = 1;b2.x = 1; b2.y = 1;b3.x = 2; b3.y = 1;b4.x = 3; b4.y = 1;b5.x = 4; b5.y = 1;b6.x = 5; b6.y = 1;b7.x = 6; b7.y = 1;b8.x = 7; b8.y = 1;
    c1.x = 0; c1.y = 2;c2.x = 1; c2.y = 2;c3.x = 2; c3.y = 2;c4.x = 3; c4.y = 2;c5.x = 4; c5.y = 2;c6.x = 5; c6.y = 2;c7.x = 6; c7.y = 2;c8.x = 7; c8.y = 2;
    d1.x = 0; d1.y = 3;d2.x = 1; d2.y = 3;d3.x = 2; d3.y = 3;d4.x = 3; d4.y = 3;d5.x = 4; d5.y = 3;d6.x = 5; d6.y = 3;d7.x = 6; d7.y = 3;d8.x = 7; d8.y = 3;
    e1.x = 0; e1.y = 4;e2.x = 1; e2.y = 4;e3.x = 2; e3.y = 4;e4.x = 3; e4.y = 4;e5.x = 4; e5.y = 4;e6.x = 5; e6.y = 4;e7.x = 6; e7.y = 4;e8.x = 7; e8.y = 4;
    f1.x = 0; f1.y = 5;f2.x = 1; f2.y = 5;f3.x = 2; f3.y = 5;f4.x = 3; f4.y = 5;f5.x = 4; f5.y = 5;f6.x = 5; f6.y = 5;f7.x = 6; f7.y = 5;f8.x = 7; f8.y = 5;
    g1.x = 0; g1.y = 6;g2.x = 1; g2.y = 6;g3.x = 2; g3.y = 6;g4.x = 3; g4.y = 6;g5.x = 4; g5.y = 6;g6.x = 5; g6.y = 6;g7.x = 6; g7.y = 6;g8.x = 7; g8.y = 6;
    h1.x = 0; h1.y = 7;h2.x = 1; h2.y = 7;h3.x = 2; h3.y = 7;h4.x = 3; h4.y = 7;h5.x = 4; h5.y = 7;h6.x = 5; h6.y = 7;h7.x = 6; h7.y = 7;h8.x = 7; h8.y = 7;

    /// DONT LOOK THERE
    std::string input;
    std::string inputf;
    char temp;
    std::cout << "\n" << "Enter piece position (a1-h8): ";
    std::cin >> input;
    std::cout << "\n" << "Enter piece position (a1-h8): ";
    std::cin >> inputf;
    if (input != "") {
        if (input == "a1") {
            temp = Board[a1.x][a1.y];

        }
    }

    
    

}

void getXY(std::string input){
    if (input == "a1") {
        
    }
}
