//Guess the number

#include <iostream>
#include <stdlib.h>

using namespace std;

int main()
{
    srand (time(NULL));
    int randnum = rand() % 10 + 1;
    int yoguess;
    string play;
    
    cout << "do you want to play the number guessing game";
    cin >> play;
    while (play != "yes" && play != "no"){
        cout << "*invalid input*\nYes or No?";
    }
    if (play == "yes"){
        cout << "guess a number 1 - 10 fool\n";
        cin >> yoguess;
        if (yoguess == randnum){
            cout << "ok, lucky guess it was " << randnum << endl;
        }
        else{
            cout << "WRONG FOOL, THE NUMBER WAS " << randnum << endl;
        }
    }
    else {
        cout << "ok maybe next time";
    }
    return 0;
} 

