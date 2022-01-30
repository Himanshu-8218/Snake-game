# Snake-game
#include <stdio.h>
#include <stdlib.h>
#include<windows.h>
#include<conio.h>
void Plot()
{
    int x;
    int y;
COORD a;
    x = (rand() % (118)) + 2;
    y = (rand() % (26)) + 1;
    a.X=x;
    a.Y=y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("0");

}
int main()
{
    int score=0;
    int Max_step=0;
    COORD a;
    a.X = 53;
    a.Y = 1;
    system("COLOR 9E");
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("WELCOME\n");
    getch();
    a.X = 40;
    a.Y = 10;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("press 1 to Play game\n");
    a.X = 40;
    a.Y = 11;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("press 2 exit\n");
    a.X = 40;
    a.Y = 13;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Enter your choice: ");
    a.X = 58;
    a.Y = 13;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    int s;
    scanf("%d",&s);
    system("cls");

    switch(s)
    {
        case 1:
        for (int i = 0; i < 28; i++)
        {
            a.X = 0;
            a.Y = i;
            SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
            if (i == 0 || i==27)
            {
            SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
                for(int j=0;j<120;j++)
                printf("|");
            }
            else
            {
            printf("||");
            for(int j=0;j<116;j++)
            {
                printf(" ");
            }
            printf("||");
        //     int x;
        //     int y;
        //     y = (rand() % (26)) + 1;
        //     x = (rand() % (118)) + 2;
        //     a.X=x;
        //     a.Y=y;
        //    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
        //     printf("0");
                // Plot();
            }
        }
        // a.X = 50;
        // a.Y = 15;
        // SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
        a.X = 90;
        a.Y = 28;
        SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
        printf(" d for left f for right");
        a.X = 90;
        a.Y = 29;
        SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
        printf("c for down and r for up");
        int X;
        int Y;
        Y = (rand() % (26)) + 1;
        X = (rand() % (118)) + 2;
        a.X=X;
        a.Y=Y;
        int p,q;
        p=X;
        q=Y;
        SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
        printf("0");
    int x;
    int y;
    x = (rand() % (118)) + 2;
    y = (rand() % (26)) + 1;
    a.X=x;
    a.Y=y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("#");
    while(1)
    {
    char l=getch();
    
    if(l=='d')
    {
    a.X = --x;
    a.Y = y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("#");
    a.X = x+1;
    a.Y = y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf(" ");
    a.X = x-1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    if(x==0||x==1||x==118||x==119||y==0||y==27)
    {
    system("cls");
    system("COLOR 07");
    a.X = 55;
    a.Y = 15;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("GAME OVER");
    a.X = 50;
    a.Y = 17;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Your score is : %d", score);
    getch();
        system("cls");
        system("game.exe");
    }
    Max_step +=1;
    a.X = 100;
    a.Y = 1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Number of step :%d",Max_step);
    a.X = 3;
    a.Y = 1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Score :%d",score);
    }
    else if(l=='f')
    {
    while(1)
    {
    a.X = ++x;
    a.Y = y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("#");
    a.X = x-1;
    a.Y = y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf(" ");
    a.X = x+1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    }

    // printf("\b\b ");
    // a.X = x;
    // SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    if(x==0||x==1||x==118||x==119||y==0||y==27)
    {
    system("cls");
    system("COLOR 07");
    a.X = 55;
    a.Y = 15;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("GAME OVER");
    a.X = 50;
    a.Y = 17;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Your score is : %d", score);
    getch();
        system("cls");
        system("game.exe");
    }
    Max_step +=1;
    a.X = 100;
    a.Y = 1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Number of step :%d",Max_step);
    a.X = 3;
    a.Y = 1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Score :%d",score);
    }
    else if(l=='c')
    {
    a.X = x;
    a.Y = ++y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("#");
    a.X = x;
    a.Y = y-1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf(" ");
    a.X = x;
    a.Y = y+1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    if(x==0||x==1||x==118||x==119||y==0||y==27)
    {
    system("cls");
    system("COLOR 07");
    a.X = 55;
    a.Y = 15;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("GAME OVER");
    a.X = 50;
    a.Y = 17;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Your score is : %d", score);
    getch();
        system("cls");
        system("game.exe");
    }
    Max_step +=1;
    a.X = 100;
    a.Y = 1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Number of step :%d",Max_step);
    a.X = 3;
    a.Y = 1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Score :%d",score);
    }
    else if(l=='r')
    {
    a.X = x;
    a.Y = --y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("#");
    a.X = x;
    a.Y = y+1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf(" ");
    a.X = x;
    a.Y = y-1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    if(x==0 || x==1 || x==118 || x==119 || y==0 || y==27)
    {
    system("cls");
    system("COLOR 07");
    a.X = 55;
    a.Y = 15;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("GAME OVER");
    a.X = 50;
    a.Y = 17;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Your score is : %d", score);
    getch();
        system("cls");
        system("game.exe");
    }
    Max_step +=1;
    a.X = 100;
    a.Y = 1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Number of step :%d",Max_step);
    a.X = 3;
    a.Y = 1;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Score :%d",score);
    }
    else
    {
    a.X = 40;
    a.Y = 128;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("Invalid key");
    system("cls");
    system("game.exe");
    }
        a.X = 90;
        a.Y = 28;
        SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
        printf(" d for left f for right");
        a.X = 90;
        a.Y = 29;
        SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
        printf("c for down and r for up");
    if(x== p && y == q)
    {
    score+=1;
    a.X=p;
    a.Y=q;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("#");
    p = (rand() % (118)) + 2;
    q = (rand() % (26)) + 1;
    a.X=p;
    a.Y=q;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    printf("0");
    a.X=x;
    a.Y=y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), a);
    // p=x;
    // q=y;
    }
}
    case 2:
    system("exit");

    getch();
    return 0;
}
}

