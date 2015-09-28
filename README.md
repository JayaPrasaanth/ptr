#include <stdio.h>

void update(int *a,int *b) {
    int c = *a;
    if(*b>c)
        {
          *a=*b+c;
          *b=*b-c;
    }
    else
        {
          *a=c+*b;
          *b=c-*b;
    }
}
int main() {
    int a, b;
    int *pa = &a, *pb = &b;
    
    scanf("%d %d", &a, &b);
    update(pa, pb);
    printf("%d\n%d", a, b);

    return 0;
}
