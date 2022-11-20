# 20.11.2022
/******************************************************************************

Welcome to GDB Online.
GDB online is an online compiler and debugger tool for C, C++, Python, Java, PHP, Ruby, Perl,
C#, OCaml, VB, Swift, Pascal, Fortran, Haskell, Objective-C, Assembly, HTML, CSS, JS, SQLite, Prolog.
Code, Compile, Run and Debug online from anywhere in world.

*******************************************************************************/
#include <iostream>
#include <math.h>
using namespace std;

int main()
{
    cout << "\t\t\tПрограмма 'Geometry'"<< endl;
    cout << "В этой программе мы предлагаем вам выбрать букву и узнать, какая фигура за ней скрывается" << endl;
    int ch;
    int s1 = 10;
    int s2 = 12;
    cout << "Выберите номер буквы из списка: а, б, в, г, д, е, ж, з, и, к" << endl;
    cin >> ch;
    //
    switch (ch)
    {
    case 1:
    {
        cout << "Картинка а:" << endl;
        for (int i = 0; i < s1; i++)
        {
            for (int j = 0; j < s1; j++)
            {
                if (j >= i)
                    cout << "*";
                else
                    cout << " ";
            }
            cout << "\n";
        }
        break;
    }
    case 2:
    {
        cout << "Картинка б:" << endl;
        for (int i = 0; i < s1; i++)
        {
            for (int j = 0; j <= i; j++)
            {
                cout << "*";
            }
            cout << "\n";
        }
    }
    case 3:
    {
        cout << "Картинка в:" << endl;
        for (int i = 0; i < s2/2; i++)
        {
            for (int j = 0; j <= s2 - i; j++)
            {
                if (j >= i)
                    cout << "*";
                else
                    cout << " ";
            }
            cout << "\n";
        }
        break;
    }
    case 4:
    {
        cout << "Картинка г:" << endl;
        int st = 1;
        for (int i = 0; i < s2; i++)
        {
            if (i <= s2/2-1)
                cout << "\n" << endl;
            else
                for (int j = 0; j < i; j++)
                {
                    if (j >= i - st)
                        cout << "*";
                    else
                        cout << " ";
                }
                st += 2;
                cout << "\n";
        }
        break;
    } 
    case 5:
    {
    int st = 1;
    for (int i = 0; i < s2; i++)
    {
        if (i <= s2/2-1)
        {
            for (int j = 0; j <= s2 - i; j++)
            {
                if (j >= i)
                    cout << "*";
                else
                    cout << " ";
            }
            cout << "\n";
        }
        else
            for (int j = 0; j < i; j++)
                {
                    if (j >= i - st)
                        cout << "*";
                    else
                        cout << " ";
                }
                st += 2;
                cout << "\n";
    }
    break;
    }
    case 6:
    {
        cout << "See you!";
        break;
    }
    }
}
