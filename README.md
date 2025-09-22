//# number-guessing-game-c
//A simple number guessing game in C

#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main()
{
   printf("NUMBER GUESSING GAME\n");    printf("Guess a number between 1 and 100\n");

    srand(time(0));

    int random_number = (rand()%100) + 1;
    int guessed_number;
    int no_of_guesses = 0;
    
    do
    {
    printf("Enter your guess=\n");
    scanf("%d",&guessed_number);
    no_of_guesses++;
    
     if(guessed_number<random_number){
      printf("Too low — guess higher\n");
    }
     else if(guessed_number>random_number){
     printf("Too high — guess lower”\n");
     }
    else{
    printf("congrats🎉🎉\n");
    }
    }
    while(guessed_number != random_number);
    
    printf("Number of guesses =%d\n",no_of_guesses);
    
    
    return 0;
}


