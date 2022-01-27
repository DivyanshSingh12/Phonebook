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
    people[0].number = "780054786866";

    people[1].name ="Vansh";
    people[1].number = "906880898979";
    
    people[2].name ="Likith sir";
    people[2].number = "96772598592";
    
    people[3].name ="Cineka ma'am";
    people[3].number = "91597849999";
    
    people[4].name ="Meena ma'am";
    people[4].number = "9444189889990";
    
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
