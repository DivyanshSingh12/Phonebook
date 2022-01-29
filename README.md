# Phonebook
For college mini project 
#include <stdio.h>
#include <string.h>

typedef struct
{
    char* name;
    char* number;
}
person;
const int NUMBER = 5;

int main(void)
{ 
    person people[NUMBER];

    people[0].name = "Divyansh";
    people[0].number = "7800547864";

    people[1].name ="Vansh";
    people[1].number = "9068808984";
    
    people[2].name ="Likith sir";
    people[2].number = "9677259859";
    
    people[3].name ="Cineka ma'am";
    people[3].number = "9159784994";
    
    people[4].name ="Meena ma'am";
    people[4].number = "9444189889";
    
    char str[100];
    scanf("%[^\n]%*c", str);

    for(int i = 0; i < NUMBER; i++)
    {
        if(strcmp(people[i].name, str) == 0)
        {
            printf("Found\nThe mobile number is: %s\n", people[i].number);
            return 0;
        }
    }
    printf("Not Found\n");
    return 1;
}
