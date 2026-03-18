# Student-learning-log
#include <stdio.h>

int main() {
    int n, i;#include <stdio.h>
#include <stdlib.h>

struct Log {
    char date[20];
    char subject[50];
    float hours;
};

int main() {
    int n, i;
    
    printf("Enter number of entries: ");
    scanf("%d", &n);

    struct Log logs[n];

    FILE *file = fopen("learning_log.txt", "a");

    if (file == NULL) {
        printf("Error opening file!\n");
        return 1;
    }

    for (i = 0; i < n; i++) {
        printf("\nEntry %d\n", i + 1);

        printf("Enter Date (DD-MM-YYYY): ");
        scanf("%s", logs[i].date);

        printf("Enter Subject: ");
        scanf("%s", logs[i].subject);

        printf("Enter Hours Studied: ");
        scanf("%f", &logs[i].hours);

        fprintf(file, "Date: %s | Subject: %s | Hours: %.2f\n",
                logs[i].date, logs[i].subject, logs[i].hours);
    }

    fclose(file);

    printf("\nData saved successfully to learning_log.txt\n");

    return 0:
    }
