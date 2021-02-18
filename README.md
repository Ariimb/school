Intro to algorithms
Exercise 4-1: Write a program to print your name, social security number, and
date of birth.
#include <stdio.h> 
 int main()  
  {
     printf("Name   : Ari Martinez\n"); 
     printf("Date of birth    : October 1st 2001\n"); 
     printf("Security number : 56170148581\n"); 
     return(0); 
  }

Exercise 4-2: Write a program to print a block E using asterisks (*), where the E
has a height of seven characters and a width of five characters.
#include <stdio.h> 
 int main() 
 {
	printf("*****\n");
	printf("*\n");
	printf("*\n");
	printf("*****\n");
	printf("*\n");
	printf("*\n");
	printf("*****\n");

	return(0);
}

Exercise 4-3: Write a program to compute the area and perimeter of a rectangle
with a width of three inches and a height of five inches. What changes must be made
to the program so that it works for a rectangle with a width of 6.8 inches and a
length of 2.3 inches? It has to change the inches in the height and width and the real numbers.

#include <stdio.h> 

/* height and width of a rectangle in inches */
int width;          
int height;         

int area;           
int perimeter;      

int main() {
	height = 5;
	width = 3;

    perimeter = 2*(height + width);
	printf("Perimeter of the rectangle = %d inches\n", perimeter);
	
	area = height * width;
	printf("Area of the rectangle = %d square inches\n", area);

return(0);
}

Exercise 4-4: Write a program to print "HELLO" in big block letters; each letter
should have a height of seven characters and width of five characters.

#include <stdio.h> 
{
    int i;

    for(i=0;i<7;++i)
    {
        if(i==3)
            cout<<"HHHHH\n";
        else
            cout<<"H   H\n";
    }

    for(i=7;i<14;i++)
    {
        if(i==7||i==10||i==13)
            cout<<"EEEEE\n";
        else
            cout<<"E\n";
    }

    return 0;
}


Exercise 4-5: Write a program that deliberately makes the following mistakes:
· Prints a floating-point number using the %d conversion.
· Prints an integer using the %f conversion.
· Prints a character using the %d conversion.

#include <stdio.h>

float floatnum;     /* a floating-point number */
int intnum;         /* an integer */
char character;     /* a character */

int main() {
	floatnum = 1.0;
	intnum = 1;
	character = 'A';

	printf("%f as %%d: %d\n", floatnum, floatnum);
	printf("%d as %%f: %f\n", intnum, intnum);
	printf("%c as %%d: %d\n", character, character);

	return(0);
}

Example 5.6 full2/full2.c
#include <stdio.h>
#include <string.h>

char mystring[30];
char nombre[10];
char last[10];
int mylen; //lenght of the string

int main(void) 
{
  printf("enter first name/ ingrese nombre: ");
  fgets(nombre,sizeof(nombre),stdin);
  mylen = strlen(nombre);
  printf("mylen is %d\n",mylen);
  nombre[mylen-1] = '\0';
  printf("enter last/ ingrese apellido: ");
  fgets(last,sizeof(last),stdin);
  mylen = strlen(last);
  last[mylen-1] = '\0';
  printf("mylen2 is %d\n",mylen);
  strcpy(mystring,nombre);
  strcat(mystring," ");
  strcat(mystring,last);
  printf("the full name is %s \n", mystring);
  return 0;
}

Matrix
#include <stdio.h>

int array[3]={11,12,13};

int matrix[3][2];

int main(void) {

  matrix[0][0]=11;
  matrix[0][1]=12;
  matrix[1][0]=13;
  matrix[1][1]=22;
  matrix[2][0]=23;
  matrix[2][1]=24;

  
  printf("matrix[row %d] ",0);
  printf("%d ",matrix[0][0]);
  printf("%d ",matrix[0][1]);
  printf("\n");

  printf("matrix[row %d] ",1);
  printf("%d ",matrix[1][0]);
  printf("%d ",matrix[1][1]);
  printf("\n");

  printf("matrix[row %d] ",2);
  printf("%d ",matrix[2][0]);
  printf("%d ",matrix[2][1]);
  printf("\n");

  return 0;
}

Example 5.8 double/double.c
#include <stdio.h>
char  line[100];   /* input line from console */
int   value;       /* a value to double */

int main()
{
    printf("Enter a value: ");

    fgets(line, sizeof(line), stdin);
    sscanf(line, "%d", &value);

    printf("Twice %d is %d\n", value, value * 2);
    return (0);
}

