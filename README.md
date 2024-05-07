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

void Menu2()
{
    int num2 = 1;
    int thechoice1, thechoice2;
    for (int j = 0; j < 3; ++j)
    {
        cout << "\n";
        cout << "\t\t\t";
        cout << "Enter " << num2 << "\t for  " << car.model[j + ((thechoice1 - 1) * 3)] << endl;
        num2++;
    }
    cout << "\n\n\n\t\t\tPlease,\n\t\t\tenter your choice: ";
    cin >> thechoice2;
    cout << "\n\t\t\t\tFor how much time do you want to rent " << car.model[((thechoice1 - 1) * 3) + thechoice2 - 1] << " ?\n";
    lease.car = car.model[((thechoice1 - 1) * 3) + thechoice2 - 1];
    int hour, ch;
    cout << "\n\t\t\t\t---> Enter 1 for 12 hours\n";
    cout << "\t\t\t\t---> Enter 2 for 24 hours\n";
    cout << "\t\t\t\t---> Enter 3 for 3 days\n";
    cout << "\t\t\t\t---> Enter 4 for a week\n";
    cout << "\t\t\t\t---> Enter 5 to choose hours yourself.\n\n";
    cout << "Enter your choice : ";
    cin >> ch;
    if (ch == 1)
    {
        cout << "Total payable amount is 4700.";
        lease.rent = 4700;
    }
    else if (ch == 2)
    {
        cout << "Total payable amount is 9000.";
        lease.rent = 9000;
    }
    else if (ch == 3)
    {
        cout << "Total payable amount is 25000.";
        lease.rent = 25000;
    }
    else if (ch == 4)
    {
        cout << "Total payable amount is 63000.";
        lease.rent = 63000;
    }
    else if (ch == 5)
    {
        cout << "Enter hours : ";
        cin >> hour;
        cout << "Total rent is " << hour * 400;
        lease.rent = hour * 400;
    }

    cout << "\n\n\n\t\t\tConfirm checkout for " << car.model[((thechoice1 - 1) * 3) + thechoice2 - 1] << "(yes /no /exit ) : " << endl;
}

void Details(int Choice1)
{
    system("CLS");
    cout << "\n\n\n\t\t\t-----------------------------\n";
    cout << "\t\t\tYou Have Selected - " << car.company[Choice1 - 1] << endl;
    cout << "\t\t\t-----------------------------\n\n\n";
    cout << "\t\t\tModel : " << car.model[Choice1 - 1] << endl;
}


