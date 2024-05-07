#include <iostream>
#include <conio.h>
#include <stdlib.h>
using namespace std;

struct Cars
{

    string company[200] = {"BMW", "AUDI", "MERCEDES", "ROLLS ROYCE", "RANGE ROVER"};

    string model[100] = {"BMW M5CS", "BMW GT", "BMW 7SERIES",
                         "AUDI R8", "AUDI A4", "AUDI Q5",
                         "MERCEDES E 63 AMG", "MERCEDES BENZ G CLASS", "MERCEDES MAYBACH S680",
                         "ROLLS ROYCE CULLINAN", "ROLLS ROYCE DAWN", "ROLLS ROYCE GHOST",
                         "RANGE ROVER VELAR", "RANGE ROVER SPORT", "RANGE ROVER EVOQUE"};

} car;

struct Lease_info
{
    string Name[100];
    int age[10];
    string city[10];
    long contact[100];
    int payment_acc[100];
    int rent;
    string car;
} lease;

void Menu1()
{
    int num1 = 1;
    int thechoice1;
    for (int i = 0; i < 5; ++i)
    {
        cout << "\n";
        cout << "\t\t\t";
        cout << "Enter " << num1 << "\t for  " << car.company[i] << endl;
        num1++;
    }
    cout << "\n\n\n\t\t\tPlease,\n\t\t\tEnter your Choice: ";
    cin >> thechoice1;
}
