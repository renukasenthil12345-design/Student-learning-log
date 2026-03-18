#include <stdio.h>

int main() {
    int days, i;
    char subject[50];
    float hours, total = 0;

    printf("Enter number of days: ");
    scanf("%d", &days);

    for(i = 1; i <= days; i++) {
        printf("\nDay %d\n

    printf("\nTotal Study Hours: %.2f\n", total);
    printf("Average Study Hours: %.2f\n", total / days);

    return 0;
}
