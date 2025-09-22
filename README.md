//# number-guessing-game-c
//A simple number guessing game in C

#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main()
{
    printf("NUMBER GUESSING GAME\n");
    srand(time(0));
    int random_number = (rand()%100) + 1;
    int guessed_number;
    int no_of_guesses = 0;
    
    do
    {
    printf("Guessed Number=\n");
    scanf("%d",&guessed_number);
    no_of_guesses++;
    
     if(guessed_number<random_number){
      printf("Higher!!!!!\n");
    }
     else if(guessed_number>random_number){
     printf("Lower!!!!!\n");
     }
    else{
    printf("congrats🎉🎉\n");
    }
    }
    while(guessed_number != random_number);
    
    printf("Number of guesses =%d\n",no_of_guesses);
    
    
    return 0;
}


