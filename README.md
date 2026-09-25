# EX-NO14-HASH-ALGORITHM

## AIM:
To implement HASH ALGORITHM

## ALGORITHM:

Enter the message from the user.

Initialize the hash value to zero.

Generate the hash by performing XOR and addition on each character.


Display the computed hash in hexadecimal format.


Enter the received hash and compare it with the computed hash.


Display the result as successful if both hashes match; otherwise, display verification failed.


## Program:
```
#include <stdio.h>
#include <string.h>

int main() {
    char msg[100], received[3];
    unsigned char hash = 0;
    int i, r;

    printf("Enter message: ");
    scanf("%s", msg);

    for (i = 0; msg[i] != '\0'; i++)
        hash = (hash ^ msg[i]) + msg[i];

    printf("Computed Hash: %02x\n", hash);

    printf("Enter received hash: ");
    scanf("%s", received);

    sscanf(received, "%x", &r);

    if (hash == r)
        printf("Hash verification successful. Message is unchanged.\n");
    else
        printf("Hash verification failed. Message has been altered.\n");

    return 0;
}
```

## Output:
<img width="659" height="197" alt="Screenshot 2026-03-09 102714" src="https://github.com/user-attachments/assets/2655ce74-bfa3-401d-b321-0409ccb91f81" />

## Result:
The program is executed successfully.
