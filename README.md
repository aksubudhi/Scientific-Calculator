// Scientific-Calculator <-This project is fully based on C language and using function.

#include <stdio.h>
#include <math.h>

void add()
{
    int a, b, sum;
    printf("Enter two number:\n");
    scanf("%d \n %d", &a, &b);
    sum = a + b;
    printf("The sum of two number is %d", sum);
}
void sub()
{
    int a, b, sub;
    printf("Enter two Number:\n");
    scanf("%d \n %d", &a, &b);
    sub = a - b;
    printf("The substraction of two number is %d", sub);
}
void mul()
{
    int a, b, mul;
    printf("Enter two Number:\n");
    scanf("%d \n %d", &a, &b);
    mul = a * b;
    printf("The substraction of two number is %d", mul);
}
void div()
{
    int a, b, div;
    printf("Enter two Number:\n");
    scanf("%d \n %d", &a, &b);
    div = a / b;
    printf("The division of two number is %d", div);
}
void power()
{
    int a, b, pow = 1;
    printf("enter two number:\n");
    scanf("%d \n %d", &a, &b);
    while (b != 0)
    {
        pow *= a;
        --b;
    }
    printf("power is : %d", pow);
}
void modulo()
{
    int a, b;
    printf("Enter two number: \n");
    scanf("%d \n %d", &a, &b);
    scanf("The mod is:%d", a % b);
}
void facto()
{
    int i, num, facto = 1;
    printf("enter the number: \n");
    scanf("%d", &num);
    for (i = 1; i <= num; i++)
    {
        facto = facto * i;
    }
    printf("The factorial of the number is:%d", facto);
}
void sqrroot()
{
    double num, sqrroot;
    printf("Enter the number:\n");
    scanf("%lf", &num);
    sqrroot = sqrt(num);
    printf("The square root of the number is:%lf", sqrroot);
}
void cuberoot()
{
    double num, cuberoot;
    printf("Enter the number:\n");
    scanf("%lf", &num);
    cuberoot = cbrt(num);
    printf("The cuberoot of the number is:%lf", cuberoot);
}
void trigonometric()
{
    float degree, radian;
    const float pi = 3.14159;
    printf("Enter the Degree:");
    scanf("%f", &degree);
    radian = degree * (pi / 180.0);
    printf("sine(%f)= %f", degree, sin(radian));
}
void arraymul()
{
    int x, y, z;
    printf("Enter the value of X :");
    scanf("%d", &x);
    printf("Enter the value of Y :");
    scanf("%d", &y);
    int a[x][y], b[y][z];
    int r1, c1, r2, c2;
    int i, j, k;
    for (r1 = 0; r1 < x; r1++)
    {
        for (c1 = 0; c1 < y; c1++)
        {
            printf("a[%d][%d]=", r1, c1);
            scanf("%d", &a[r1][c1]);
        }
    }
    printf("Enter the value of Z :");
    scanf("%d", &z);

    for (r2 = 0; r2 < y; r2++)
    {
        for (c2 = 0; c2 < z; c2++)
        {
            printf("b[%d][%d]=", r2, c2);
            scanf("%d", &b[r2][c2]);
        }
    }
    int mul[x][z];
    for (r1 = 0; r1 < x; r1++)
    {
        for (c1 = 0; c1 < y; c1++)
        {
            printf("%d\t", a[r1][c1]);
        }
        printf("\n");
    }

    for (r2 = 0; r2 < x; r2++)
    {
        for (c2 = 0; c2 < y; c2++)
        {
            printf("%d\t", a[r2][c2]);
        }
        printf("\n");
    }

    printf("Multiplication of matrix a and b is :\n");
    for (i = 0; i < x; i++)
    {
        for (j = 0; j < y; j++)
        {
            for (k = 0; k < z; k++)
            {
                mul[i][j] += a[i][k] * b[k][j];
            }
        }
    }
    for (i = 0; i < x; i++)
    {
        for (j = 0; j < y; j++)
        {
            for (k = 0; k < z; k++)
            {
                printf("%d\t", mul[i][j]);
            }
            printf("\n");
        }
    }
}

// main
int main()
{

    char choice;

    printf("The avialable option: \n 1: addition \n 2: substraction \n 3: multiplication \n 4: division \n 5: power function \n 6: modulo \n 7: factorial \n 8: square root \n 9: cube root \n 10:array multiplication \n 11:trigonomrtric\n");
    printf("\nEnter your choice from the above option:\n");
    scanf("%d", &choice);
    switch (choice)
    {
    case 1:
        add();
        break;
    case 2:
        sub();
        break;
    case 3:
        mul();
        break;
    case 4:
        div();
        break;
    case 5:
        power();
        break;
    case 6:
        modulo();
        break;
    case 7:
        facto();
        break;
    case 8:
        sqrroot();
        break;
    case 9:
        cuberoot();
        break;
    case 10:
        arraymul();
        break;
    case 11:
        trigonometric();
        break;
    }

    return 0;
}
