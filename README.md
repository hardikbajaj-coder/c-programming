# c-programming

#include <stdio.h>
#include <time.h>
int main() {
    int birth_year, current_year, age;
    int birth_month, birth_day;
    int current_month, current_day;
    int years , months , days;
    time_t now;
    struct tm *today;
    time(&now);
    today = localtime(&now);

    current_year = today->tm_year + 1900;
    current_month = today->tm_mon +1;
    current_day = today->tm_mday;
    // 1. Input birth year
    printf("Enter your birth year:\n ");
    scanf("%d", &birth_year);
    printf("enter your birth month:\n");
    scanf("%d" , &birth_month);
    printf("enter your birth day:\n" );
    scanf("%d" ,&birth_day);
    age = current_year - birth_year;
    years = current_year - birth_year;
    if (current_month>= birth_month) {
    months = current_month - birth_month;}
    else {
    months = birth_month - current_month;}
    
    // 3. Calculate age
    if  (birth_month> current_month ||(birth_month == current_month && birth_day>current_day)) {
       age--;
        printf("your current age is: %d\n " , age);

    }

    else{
    printf("You are %d years old.\n", age);
    }
    return 0;
}




    
    
