//Rock, Paper Scissors

#include <iostream>
#include <stdlib.h>

using namespace std;

int main()
{
    string y_n;
    string hand;
    int comp;
    string comphand;
    
    cout<<"You wanna play 'Rock, Paper, Scissors'?\n";
    cin>>y_n;
    
    while (y_n != "yes" && y_n != "no"){
        cout<<"*invalid*\n";
        cout<<"yes or no?\n";
        cin>>y_n;
    }
    if (y_n == "yes"){
        srand(time(NULL));
        int comp = rand()% 3 + 1;
        if(comp == 1){
            comphand = "rock";
        }
        else if(comp == 2){
            comphand = "paper";
        }
        else {
            comphand = "scissors";
        }
        
        cout<<"yeah aight\nRock, paper, or scissors?\n";
        cin>>hand;
        while (hand != "rock" && hand != "paper" && hand != "scissors"){
            cout<<"*invalid*\n";
            cout<<"rock, paper, or scissors\n";
            cin>>hand;
        }
        cout<<"i did "<<comphand<<endl;
        if ((hand == "rock" && comphand == "scissors") || (hand == "scissors" && comphand == "paper") || (hand == "paper" && comphand == "rock")){
            cout<<"What?! I can't lose! I'm a computer\n...\n...\n...\nmaybe I'm malfunctioning";
        }


        else if ((hand == "rock" && comphand == "paper") || (hand == "paper" && comphand == "scissors") || (hand == "scissors" && comphand == "rock" )){
            cout<<"HAH!!!\nYou should have known that robots can't lose!";
        }
        else{
            cout<<"I guess humans can be as good as robots sometimes";
        }
    }
    else{
        cout<<"Okay...";
    }

    return 0;
