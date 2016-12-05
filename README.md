# bbbasketgreedy
#include <stdio.h>
#include <math.h>
#include "cs50.h"

 
 int main(void)
 
 {
     float change;
     int coins_quantity = 0, money_amount;
     
    do
    {
        printf ("How much change is owed?\n");
        change= GetFloat();
    }
    while (change < 0);
   money_amount= (int) round(change*100);
    while (money_amount >= 25)
    {
        coins_quantity++;
        money_amount-=25;
    }
    while (money_amount >= 10)
    {
        coins_quantity++;
        money_amount-=10;        
    }
    while (money_amount >= 5)
    {
        coins_quantity++;
        money_amount-=5;   
    }
    while (money_amount >= 1)
    {
        coins_quantity++;
        money_amount-=1;
    }
    printf("%d\n", coins_quantity);
 }
     
