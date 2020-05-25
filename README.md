//Coin Flipping

#include <iostream>
#include <stdlib.h>
using namespace std;
int main()
{
    int toth = 0;
    int tott = 0;
    srand(time(NULL));    
    for(int i = 0;i < 3; i++){        
        
        int coin = rand()% 2 + 1;
        if(coin == 2)
        {
         //cout<<"It's Tails.\n";
         tott++;
        }
        else
        {
        //cout<<"It's Heads.\n";
        toth++;
        }
    }
    cout<<"Heads: "<< toth<<endl;
    cout<<"Tails: "<<tott;
}
