#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *file = fopen("message.txt", "w");

    if (file == NULL) {
        perror("Error opening file");
        return 1;
    }

    fprintf(file, "Hello! This message was written using a C program.\n");

    fclose(file);
    printf("Message successfully written to message.txt\n");

    return 0;
}
----------------------------------------------------------------------------------------
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *file = fopen("message.txt", "r");
    char buffer[256];

    if (file == NULL) {
        perror("Error opening file");
        return 1;
    }

    while (fgets(buffer, sizeof(buffer), file) != NULL) {
        printf("%s", buffer);
    }

    fclose(file);
    return 0;
}
---------------------------------------------------------------------------------------
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *source = fopen("message.txt", "r");
    FILE *destination = fopen("copy.txt", "w");
    char ch;

    if (source == NULL || destination == NULL) {
        perror("Error opening files");
        return 1;
    }

    while ((ch = fgetc(source)) != EOF) {
        fputc(ch, destination);
    }

    fclose(source);
    fclose(destination);

    printf("File successfully copied to copy.txt\n");
    return 0;
}
