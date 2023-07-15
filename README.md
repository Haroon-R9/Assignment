/*    # Assignment
  "Haroon Khan"
F.Name: Sahib Khan
Roll No 35  */
#include <stdio.h>

int isprime(int num);

int main() {
    int num, retry;
    
    do {
        printf("Enter a number between 2 and 100: ");
        scanf("%d", &num);
        
        if (num < 2 || num > 100) {
            printf("Number out of range, press 1 to try again.\n");
            scanf("%d", &retry);
        } else {
            if (isprime(num)) {
                printf("%d is a prime number.\n", num);
            } else {
                printf("%d is not a prime number.\n", num);
            }
            
            retry = 0;
        }
    } while (retry == 1);
    
    return 0;
}

int isprime(int num) {
    if (num < 2) {
        return 0;
    }
    
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0) {
            return 0;
        }
    }
    
    return 1;
}
