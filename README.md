# C-_ROCK_PAPER_SCISSOR_GAME
#include <stdio.h>
#include <time.h>
  int score_of_comp=0;
  int score_of_user=0;
int comp_win(){
  ++score_of_comp;
  printf("USER-%d||||||COMPUTER-%d\n",score_of_user,score_of_comp);
}
int user_win(){
  ++score_of_user;
printf("USER-%d||||||COMPUTER-%d\n",score_of_user,score_of_comp);
}
int main()
{
  int a = 1;
  int b = 3;
  int choise;

  do
  {
    int random_no;

    srand(time(NULL));
    random_no = (rand() % (b - a + 1)) + a;

    printf("WELCOME TO STONE PAPER SCSSEOR GAME\n");
    printf("=====================================\n");
    printf("1.paper\n");
    printf("2.rock\n");
    printf("3.scissor\n");
    printf("4.exit\n");
    printf("=====================================\n");
    scanf("%d\n", &choise);
    switch (choise)
    {
    case 1:
      // DRAW CONDTION
      if (choise == random_no)
      {
      printf("its a draw computer also chose paper\n");
      //score table
      printf("USER-%d||||||COMPUTER-%d\n",score_of_user,score_of_comp);
      }
      // if computer and user choose are differnt
      if (choise != random_no)
      {
        if(random_no==2){
        printf("======================================\n");
        printf("you win computer  choose rock\n");
        printf("======================================\n");

        //when user win score board updated
        user_win();
        }
        if(random_no==3){
          printf("======================================\n");
        printf("you losse computer choose scissor\n");
        printf("bas hargya computer se bhi\n");
        comp_win();
        printf("======================================\n");
        }
        
        
      }
      
      break;

    case 2:
      if (choise == random_no)
      {//DRAW CONDTION
         printf("its a draw computer also chose rock\n");
         printf("USER-%d||||||COMPUTER-%d\n",score_of_user,score_of_comp);
      }
      if (choise != random_no)
      {
        if(random_no==3){ //USER WIN CONDTION
        printf("======================================\n");
        printf("you win\n");
         printf("you win computer  choose scissor\n");
        user_win();
        printf("======================================\n");
        
        }
        if(random_no==1){//COMPUTER  WIN CONDTION
          printf("======================================\n");
        printf("you losse computer choose paper\n");
        printf("bas hargya computer se bhi\n");
        comp_win();
        printf("======================================\n");
        }
      }

      break;

    case 3:

      if (choise == random_no)
      {//DRAW CONDTION
         printf("its a draw computer also chose scissor\n");
         printf("USER-%d||||||COMPUTER-%d\n",score_of_user,score_of_comp);
      }

      if (choise != random_no)
      {
        if(random_no==1){//USER WIN CONDTION
        printf("======================================\n");
        printf("you win\n");
        printf("you win computer  choose paper\n");
        user_win();
        printf("======================================\n");
        
        }
        if(random_no==2){//COMP WIN CONDTION
           printf("======================================\n");
        printf("you losse computer choose rock\n");
        printf("bas hargya computer se bhi\n");
        comp_win();
        printf("======================================\n");
        }
      }

      break;
    case 4:
      return 0;
      break;

    default:
      printf("Invalid option.\n");
    }
  } while (1);

  return 0;
}
