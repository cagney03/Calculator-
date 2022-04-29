# include <stdio.h>
#include <math.h>

int main()
{
  float value1;
  float value2;
  float answer;
  char operator;
  printf("Enter Calculation:\n"):
  scanf("%f %c %f ,&value1,&operator,&value2);
  
  switch(operator)
   {
     case '*':
       answer=value1*value2;
     case '/':
       answer=value1/value2;
     case '+':
       answer=value1+value2;
     case '-':
       answer=value1-value2;
     case '^':
       answer=pow(value1,value2);
     case '**':
       answer=sqrt(value2);
     default:
         goto fail;
     }
  printf("%0.6f%c%0.6f = %0.6f\n",value1,operator,value2,answer);
  goto exist;
    fail:
      printf("Fail\n")
    exit:
      return 0;
}
     
