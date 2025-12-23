#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int gizli_reqem, texmin;
    int cehd_sayi = 3;

    srand(time(0));
    gizli_reqem = rand() % 10 + 1;

    printf("--- Reqem Texmin Etme Oyununa Xos Gelmisiniz! ---\n");
    printf("1 ile 10 arasinda bir reqem tutmusam. 3 cehdiniz var.\n\n");

    for (int i = 1; i <= cehd_sayi; i++) {
        printf("%d. cehdiniz: ", i);
        scanf("%d", &texmin);

        if (texmin == gizli_reqem) {
            printf("Tebrikler! Dogru tapdiniz!\n");
            return 0;
        } else if (texmin < gizli_reqem) {
            printf("Daha boyuk bir reqem yazin.\n");
        } else {
            printf("Daha kicik bir reqem yazin.\n");
        }
    }

    printf("\nCehdleriniz bitdi. Meglub oldunuz!\n");
    printf("Dogru reqem bu idi: %d\n", gizli_reqem);

    return 0;
}
