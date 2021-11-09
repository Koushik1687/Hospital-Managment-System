# Hospital-Managment-System
#include <iostream>
#include <conio.h>
#include <string>
#include <stdlib.h>
#include <fstream>

using namespace std;

void intro();
void enter();
void login();
void menu();
void Register();
void loginD();
void loginP();

void patient_entry();
void doctor();
void patient_information();
void doctor_information();
void hospital_information();
void schedule();

void appointment();
void doctorLogin();
void patientLogin();
void hospital();
void doctor();

void vishal();
void koushik();
void soumyadip();
void akash();
void preetam();
void saptak();

void vishal1();
void koushik1();
void soumyadip1();
void akash1();
void preetam1();
void saptak1();

class entry
{
protected:
    string name;
    int age;
    string bloodGroup;
    string address;

public:
};
void patient_entry()
{
    string name, bath, blood, gen, date, pas;
    int age, phone;
    system("cls");

    ofstream file;
    file.open("patient_information.txt", ios::out | ios::app);

    cout << "\n\n\n\n\t\t\t\t\t       Patient entry ";
    cout << "\n\t\t\t\t\t   ===================== ";
    cout << "\n\n\n\n\t\t\t\t Patient name : ";
    cin >> name;
    cout << "\n\t\t\t\t Set a password : ";
    cin >> pas;
    cout << "\n\t\t\t\t Patient gender : ";
    cin >> gen;
    cout << "\n\t\t\t\t Patient age : ";
    cin >> age;
    cout << "\n\t\t\t\t Date of bath : ";
    cin >> bath;
    cout << "\n\t\t\t\t Blood group : ";
    cin >> blood;
    cout << "\n\t\t\t\t Phone number : ";
    cin >> phone;
    cout << "\n\t\t\t\t Entry date : ";
    cin >> date;
    cout << "\n\n\n\t\t\t\t\t  All data is store ";
    //file<<"\n\n       name        password        gender       age         birth date         blood group          phone number            entry date"<<endl;
    //file<<"\n --------        -------------        --------            ------           ----------             ----------          ----------            -----------   "<<endl;
    file << "\t" << name << "\t\t" << pas << "\t\t" << gen << "\t\t" << age << "\t\t" << bath << "\t\t" << blood << "\t\t"
         << "0" << phone << "\t\t" << date << endl;

    file.close();

    char ch;
    cout << "\n\n\n\n\n\t\t\t\t\t\t\t\t\t\t Press 'g' to go back : ";
    cin >> ch;

    switch (ch)
    {
    case 'g':
    {
        system("cls");
        menu();
    }
    }
}

void patient_information()
{
    string line;
    system("cls");
    ifstream file1("patient_information.txt");

    while (getline(file1, line))
    {
        cout << line << endl;
    }
    char ch;
    cout << "\n\n\n\n\n\t\t\t\t\t\t ";
    cout << "Press 'g' to go back : ";
    cin >> ch;

    switch (ch)
    {
    case 'g':
    	{
        	system("cls");
        	menu();
    	}
    }
}

void doctor_information()
{

    system("cls");
    cout << "\n\n\n\n\n\t\t\t\t\t             Doctor information  ";
    cout << "\n\t\t\t\t\t\t  ========================";
    cout << "\n\n";
    cout << "\n                                  id                name                       sector ";
    cout << "\n                                ------           -----------               ---------------              ";
    cout << "\n\n\t\t\t\t 3476.        Dr. Vishal Parui       Cardiologist specialist          " << endl
         << endl;
    cout << "\t\t\t\t 8436.        Dr. Koushik Paul           Bone Specialist                    " << endl
         << endl;
    cout << "\t\t\t\t 8956.        Dr. Soumyadip Mukherjee   Anesthesiologists Specialist   " << endl
         << endl;
    cout << "\t\t\t\t 3487 .       Dr. Akash Roy            Darmatologist Specialist                 " << endl
         << endl; // Colon and Rectal
    cout << "\t\t\t\t 2398.         Dr. Saptak Mondal       Critical Medicine specialist       " << endl
         << endl; //Care
    cout << "\t\t\t\t 1875.        Dr. Preetam Das           Child Specialist        " << endl
         << endl;
    //char ch;
    int in;
    cout << "\n\n\n\t\t\t\t Enter id :";
    cin >> in;

    switch (in)
    {
    case 3476:
    {
        int count = 1;
        system("cls");
        vishal();
        break;
    }
    case 8436:
    {
        system("cls");
        koushik();
        break;
    }
    case 8956:
    {
        system("cls");
        soumyadip();
        break;
    }

    case 3487:
    {
        system("cls");
        akash();
        break;
    }

    case 2398:
    {
        system("cls");
        preetam();
        break;
    }

    case 1875:
    {
        system("cls");
        saptak();
        break;
    }
    default:
        cout << "Wrong choice";
    }
    getch();
}

void hospital_information()
{
    system("cls");
    cout << "\n\n\n\t\t\t\t\t                   COVID RELIEF MEDICAL HOSPITAL  ";
    cout << "\n\t\t\t                       _______________________________________________ ";

    cout << "\n\n\n\n\n\t\t\t Type          : Public medical hospital ";
    cout << "\n\n\t\t\t Established   	: 1946 ";
    cout << "\n\n\t\t\t Principal     	: Sri Animesh Sengupta ";
    cout << "\n\n\t\t\t Director      	: Ridhima Chokroborty ";
    cout << "\n\n\t\t\t Location      	: Newtown, Kolkata ";
    cout << "\n\n\t\t\t Campus	      	: 35 acres (20 ha) ";
    cout << "\n\n\t\t\t Language      	: English ";
    cout << "\n\n\t\t\t Website       	: www.crmh.gov.bd ";
    cout << "\n\n\n\t\t\t phone number  : (033)22417059 ";
    cout << "\n\n\t\t\t               	: 9831556847 ";
    cout << "\n\n\t\t\t               	: 9756882157 ";

    char ch;
    cout << "\n\n\n\n\n\t\t\t\t\t\t ";
    cout << "Press 'g' to go back : ";
    cin >> ch;

    switch (ch)
    {
    case 'g':
    {
        system("cls");
        patientLogin();
    }
    }
}

void intro() //page 1
{

    char ch;
    cout << endl
         << endl
         << endl;
    cout << "                                         ===================================== ";
    cout << "\n                                         |                                   | ";
    cout << "\n                                         |  # HOSPITAL MANAGEMENT SYSTEM #   |";
    cout << "\n                                         |                                   |";
    cout << "\n                                         ===================================== ";

    cout << endl
         << endl
         << endl
         << endl
         << endl;
    cout << "                      In this present world,any infectious disease can spread very quickly. If we want    ";
    cout << "\n                            to prevent an infectious disease, then a temporary hospital has to    ";
    cout << " \n                              be built quickly. If we built a temporary hospital then first         ";
    cout << " \n                           thing we need a hospital management software. So that we can manage  \n\t\t\t\t";
    cout << " \n                                     the whole hospital activities. besides, a hospital ";
    cout << "\n                                     can be managed by a developed management software.";

    cout << "\n\n\n\n\n\n\n\n                                    # The people who worked to create this software  " << endl;
    cout << "\n                                      _____________________________________________";
    cout << "\n                                     |           Name                    Roll. No  |";
    cout << "\n                                     |      --------------              ---------- |";
    cout << "\n                                     |  1.   Vishal Parui                    16    |";
    cout << "\n                                     |  2.   Koushik Paul                    18    |";
    cout << "\n                                     |  3.   Soumodeep Mukherjee             29    |";
    cout << "\n                                     |  4.   Akash Roy                       36    |";
    cout << "\n                                     |  5.   Preetam Das                     39    |";
    cout << "\n                                     |  6.   Saptak Mondal                   41    |";
    cout << "\n                                     |_____________________________________________|";

    cout << "\n\n\n\n\t\t\t\t\t     Press 'e'  to enter : ";
    cin >> ch;

    switch (ch)
    {
    case 'e':
    {
        enter();
    }
    break;

    default:
        cout << "\n\n\t\t\t\t\t\t Invalid choice \n";
    }
}

void enter() // page 2
{
    int i;
    system("cls");
    cout << "\n\n\n\n\n\t\t\t\t  *******   WELCOME TO Covid Relief Medical HOSPITAL  *******  ";
    cout << "\n\t\t\t    _________________________________________________________________________ ";

    cout << "\n\n\n\t\t\t\t\t\t          1. Login ";
    cout << "\n\n\n\n\n\n\n\t\t\t        Press 1 key to go login page ";
    cout << "\n\n\n\n\n\t                         Enter : ";
    cin >> i;

    switch (i)
    {
    case 1:
    {
        login();
        break;
    }

    default:
        login();
        break;
    }
}

void login() // page 3
{
    int a;
    system("cls");
    cout << "\n\n\n\n\n\t\t\t\t\t\t  Login page ";
    cout << "\n\t\t\t\t\t        ==============";

    cout << "\n\n\n\n\t\t\t\t\t  1. Patient ";
    cout << "\n\n\t\t\t\t\t  2. Doctor ";
    cout << "\n\n\t\t\t\t\t  3. Register ";
    cout << "\n\n\n\n\n\n\n\n\n\t\t\t                  Press any option and enter to go login ";
    cout << "\n\n\n\t\t\t\t\t  Enter : ";
    cin >> a;
    switch (a)
    {
    case 1:
    {
        loginP();
        break;
    }
    case 2:
    {
        loginD();
        break;
    }
    case 3:
    {
        Register();
        break;
    }
    default:
        cout << "\n\n\n\t\t\t\t\t  Probably you press wrong " << endl;
        char ch;
        cout << "\n\t\t\t\t\t  Press 'r' to refresh : ";
        cin >> ch;

        switch (ch)
        {
        case 'r':
            system("cls");
            login();
        }
    }
}
void loginP() // page 4
{
    int count = 0;
    string user, pass, u, p;
    system("cls");
    cout << "\n\n\n\t\t\t\t Please enter the username and password" << endl;
    cout << "\t\t\t     ______________________________________________ ";
    cout << "\n\n\n\n\t\t\t\t USERNAME : ";
    cin >> user;
    cout << "\n\n\t\t\t\t PASSWORD : ";
    cin >> pass;

    ifstream input("patient_information.txt");
    while (input >> u >> p)
    {
        if (user == u && pass == p)

        {
            count = 1;
            system("cls");
        }
    }
    input.close();
    if (count == 1)
    {
        system("cls");
        patientLogin();
    }
    else
    {
        cout << "\n\n\n\n\n\n\t\t\t\t Your username or password is wrong ";
        cout << "\n\n\n\n\n\n\t\t\t\t\t\t\t\t       Press 'r' to refresh : ";
        char gh;
        cin >> gh;

        switch (gh)
        {
        case 'r':

        {
            system("cls");
            loginP();
        }
        }
    }
}

void loginD() //page 4
{
    int count = 0;
    string user, pas, u, p;
    system("cls");
    cout << "\n\n\n\t\t\t\t\t  Please enter the username and password  ";
    cout << "\n\t\t\t              ______________________________________________ ";
    cout << " \n\n\n\t\t\t USERNAME : ";
    cin >> user;
    cout << " \n\n\t\t\t PASSWORD : ";
    cin >> pas;

    ifstream input("doctor.txt");
    while (input >> u >> p)
    {
        if (user == u && pas == p)

        {
            count = 1;
            system("cls");
        }
    }
    input.close();
    if (count == 1)
    {
        system("cls");
        doctorLogin();
    }

    else
    cout << "\n\n\n\n\n\n\t\t\t Your username or password is wrong ";
    cout << "\n\n\n\n\n\n\t\t\t\t\t\t\t\t       Press 'r' to refresh : ";
    char gh;
    cin >> gh;
    switch (gh)
    {
    case 'r':
    {
        system("cls");
        loginD();
    }
    }
}
void Register() // page 4
{
    int count = 0;
    string user, pas, u, p;
    system("cls");
    cout << "\n\n\n\t\t\t\t\t  Register  ";
    cout << "\n\t\t\t          ===================== ";
    cout << " \n\n\n\t\t\t Enter USERNAME : ";
    cin >> user;
    cout << " \n\n\t\t\t Enter PASSWORD : ";
    cin >> pas;

    ifstream input("admin.txt");
    while (input >> u >> p)
    {
        if (user == u && pas == p)

        {
            count = 1;
            system("cls");
        }
    }
    input.close();
    if (count == 1)
    {
        system("cls");
        menu();
    }

    else
        cout << "\n\n\n\n\n\n\t\t\t Your username or password is wrong ";
    cout << "\n\n\n\n\n\n\t\t\t\t\t\t\t\t       Press 'r' to refresh : ";
    char gh;
    cin >> gh;

    switch (gh)
    {
    case 'r':

    {
        system("cls");
        Register();
    }
    }
}
void menu() //   register page
{

    int n;
    system("cls");
    cout << "\n\n\n\n";
    cout << "\t\t\t\t\t ==========================================";
    cout << "\t\t\t\t\t\t\t\t\t||                                        ||";
    cout << "\n\t\t\t\t        ||         COVID RELIEF MEDICAL HOSPITAL                          ||";
    cout << "\n                                        ||                                        ||";
    cout << "\t\t\t\t\t                                 ==========================================";
    cout << "\n\n\n\n\t\t\t\t\t\t01. Patient entry " << endl;

    cout << "\n\t\t\t\t\t\t02. Patient information " << endl;
    cout << "\n\t\t\t\t\t\t03. Doctor information " << endl;

    cout << "\n\t\t\t\t\t\t04. Hospital information " << endl;

    cout << "\n\t\t\t\t\t\t05. Back to login page " << endl;
    cout << "\n\n\t\t\t\t\t\tChoose any option ...";
    cin >> n;

    switch (n)
    {
    case 1:
    {
        patient_entry();
        break;
    }

    case 2:
    {
        patient_information();
        break;
    }
    case 3:
    {
        doctor();
        break;
    }

    case 4:
    {
        hospital_information();
        break;
    }

    case 5:
    {
        login();
        break;
    }
    default:
    {
        cout << "\n\n\t\t\t\t      Wrong choce ";
        char ch;

        cout << "\n\n\n\n\t\t\t\t\t  Press 'r' to refresh : ";
        cin >> ch;

        switch (ch)
        {
        case 'r':
        {
            system("cls");
            menu();
        }
        }
    }
    }

    getch();
}

void schedule()
{

    cout<<"\n  _______________________________________________________________________________________________________________________________________________________________________  ";
    cout<<"\n |  TIME    |           sunday     |         monday    |         tuesday      |        wednesday      |       thursday       |       friday      |      saturday         | ";
    cout<<"\n |__________|______________________|___________________|______________________|_______________________|______________________|___________________|_______________________| ";
    cout<<"\n |          |  Dr Saptak Mondal    |  Dr Vishal Parui  |  Dr Saptak Mondal    |  Dr Koushik Paul      |Dr Soumyodip Mukherjee|  Dr Preetam Das   |  Dr Koushik Paul      | ";
    cout<<"\n |9 AM-11 Am|Dr Soumyodip Mukherjee|  Dr Preetam Das   |  Dr Koushik Paul     |  Dr Preetam Das       |  Dr Akash Roy        |                   |                       | ";
    cout<<"\n |__________|______________________|___________________|______________________|_______________________|______________________|___________________|_______________________| ";
    cout<<"\n |          |  Dr Vishal Parui     |  Dr Akash Roy     |Dr Soumyodip Mukherjee|  Dr Akash Roy         |  Dr Vishal Parui     |  Dr Akash Roy     |  Dr Preetam Das       | ";
    cout<<"\n |11AM-1 pm |  Dr Koushik Paul     |  Dr Saptak Mondal |  Dr Preetam Das      |  Dr Vishal Parui      |  Dr Preetam Das      |                   |                       | ";
    cout<<"\n |__________|______________________|___________________|______________________|_______________________|______________________|___________________|_______________________| ";
    cout<<"\n |          |  Dr Akash Roy        |  Dr Koushik Paul  |  Dr Vishal Parui     |Dr Soumyodip Mukherjee |  Dr Saptak Mondal    |  Dr Vishal Parui  |  Dr Saptak Mondal     | ";
    cout<<"\n |1 PM-3 PM |  Dr Preetam Das      |  Dr Preetam Das   |  Dr Akash Roy        |  Dr Preetam Das       |  Dr Akash Roy        |                   |                       | ";
    cout<<"\n |__________|______________________|___________________|______________________|_______________________|______________________|___________________|_______________________| ";
    cout<<"\n |          |  Dr Saptak Mondal    |  Dr Saptak Mondal |  Dr Preetam Das      |  Dr Saptak Mondal     |Dr Soumyodip Mukherjee|  Dr Saptak Mondal |Dr Soumyodip Mukherjee | ";
    cout<<"\n |3 PM-5 PM |  Dr Koushik Paul     |  Dr Vishal Parui  |  Dr Koushik Paul     |  Dr Koushik Paul      |  Dr Vishal Parui     |                   |                       | ";
    cout<<"\n |__________|______________________|___________________|______________________|_______________________|______________________|___________________|_______________________| ";
    

    char ch;
    cout << "\n\n\n\n\n\t\t\t\t\t\t\t\t\t\t Press 'g' to go back : ";
    cin >> ch;

    switch (ch)
    {
    case 'g':
    {
        system("cls");
        patientLogin();
    }
    }
}
void doctorLogin() // doctor page
{

    int n;
    system("cls");
    cout << "\n\n\n\n";
    cout << "\t\t\t\t\t============================================\n";
    cout << "\t\t\t\t\t||                                        ||\n";                                      
    cout << "\t\t\t\t        ||              Doctor Portal             ||";
    cout << "\n                                        ||                                        ||\n";
    cout << "\t\t\t\t\t============================================";
    cout<<"\n\n\n\n\t\t\t\t\t\t01. hospital information "<<endl;
    cout << "\n\t\t\t\t\t\t02. Patient information " << endl;
    cout << "\n\t\t\t\t\t\t03. Doctor information " << endl;
    cout << "\n\t\t\t\t\t\t04. Back to login page " << endl;

    cout << "\n\n\t\t\t\t\t\tChoose any option ...";
    cin >> n;

    switch (n)
    {
	case 1:
    {
        hospital_information();
        break;
    }
    case 2:
    {
        string line;
        system("cls");
        ifstream file1("patient_information.txt");

        while (getline(file1, line))
        {
            cout << line << endl;
        }
        char ch;
        cout << "\n\n\n\n\n\t\t\t\t\t\t ";
        cout << "Press 'g' to go back : ";
        cin >> ch;

        switch (ch)
        {
        case 'g':
        {
            system("cls");
            doctorLogin();
        }
        }
    }
    case 3:
    {
        doctor();
        break;
    }

    case 4:
    {
        login();
        break;
    }

    default:
    {
        cout << "\n\n\t\t\t\t      Wrong choce ";
        char ch;

        cout << "\n\n\n\n\t\t\t\t\t  Press 'r' to refresh : ";
        cin >> ch;

        switch (ch)
        {
        case 'r':
        {
            system("cls");
            doctorLogin();
        }
        }
    }
    }

    getch();
}

void patientLogin() // patient page
{

    int n;
    system("cls");
    cout << "\n\n\n\n";
    cout << "\t\t\t\t\t============================================\n";
    cout << "\t\t\t\t\t||                                        ||\n";
    cout << "\t\t\t\t        ||              Patient Portal            ||";
    cout << "\n                                        ||                                        ||\n";
    cout << "\t\t\t\t\t============================================";
    cout << "\n\n\n\n ";

    cout << "\n\t\t\t\t\t\t01. Doctor schedule " << endl;
    cout << "\n\t\t\t\t\t\t02. Doctor information " << endl;

    cout << "\n\t\t\t\t\t\t03. Hospital information " << endl;

    cout << "\n\t\t\t\t\t\t04. Back to login page " << endl;
    cout << "\n\n\t\t\t\t\t\tChoose any option ...";
    cin >> n;

    switch (n)
    {
    case 1:
    {
        system("cls");

        schedule();

        break;
    }

    case 2:
    {
        doctor_information();
        break;
    }

    case 3:
    {
        hospital_information();
        break;
    }

    case 4:
    {
        login();
        break;
    }

    default:
    {
        cout << "\n\n\t\t\t\t      Wrong choce ";
        char ch;

        cout << "\n\n\n\n\t\t\t\t\t  Press 'r' to refresh : ";
        cin >> ch;

        switch (ch)
        {
        case 'r':
        {
            system("cls");
            patientLogin();
        }
        }
    }
    }

    getch();
}

void vishal()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr Vishal Parui ";
    cout<<"\n\t\t\t Cardiologist Specialist  ";
    cout<<"\n\t\t\t 3rd floor ";
    cout<<"\n\t\t\t Room-306 ";
    cout<<"\n\t\t\t Email: vishalparui1508@gmail.com";
    cout<<"\n\t\t\t Contact no:	8481088442";


    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

             patientLogin() ;

        }
    }
}

void koushik()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr. Koushik Paul ";
    cout<<"\n\t\t\t Bone Specialist ";
    cout<<"\n\t\t\t 4th floor ";
    cout<<"\n\t\t\t Room-406 ";
    cout<<"\n\t\t\t Email: koushikp72@gmail.com";
    cout<<"\n\t\t\t Contact no: 9831332681";

    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

             patientLogin() ;

        }
    }

}

void soumyadip()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr. Soumyadip Mukherjee ";
    cout<<"\n\t\t\t Anesthesiologists Specialist ";
    cout<<"\n\t\t\t 5th floor ";
    cout<<"\n\t\t\t Room-504 ";
    cout<<"\n\t\t\t Email: soumyadip450@gmail.com";
    cout<<"\n\t\t\t Contact no: 7044564290";

    char ch;
    cout<<"\n\n\n\t\t\t enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

             patientLogin() ;

        }
    }
}

void akash()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";;
    cout<<"\n\n\n\n\t\t\t Dr. Akash Roy";
    cout<<"\n\t\t\t Darmatologist Specialist ";
    cout<<"\n\t\t\t 6th floor ";
    cout<<"\n\t\t\t Room-606 ";
     cout<<"\n\t\t\t Email: aroy933050@gmail.com";
    cout<<"\n\t\t\t Contact no: 0196545514";

    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

             patientLogin() ;

        }
    }

}

void saptak()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr. Saptak Mondal ";
    cout<<"\n\t\t\t Critical Medicine Specialist ";
    cout<<"\n\t\t\t 5th floor ";
    cout<<"\n\t\t\t room-502 ";
     cout<<"\n\t\t\t email: saptak.mondal.on@gmail.com";
    cout<<"\n\t\t\t contact no: 9007920187";

    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

             patientLogin() ;

        }
    }
 }

void preetam()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr. Preetam Das ";
    cout<<"\n\t\t\t Child Specialist  ";
    cout<<"\n\t\t\t 6th floor ";
    cout<<"\n\t\t\t room-306 ";
    cout<<"\n\t\t\t email: daspreetam50@gmail.com";
    cout<<"\n\t\t\t contact no:01796875752";

    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

             patientLogin() ;

        }
    }
}





void vishal1()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr Vishal Parui ";
    cout<<"\n\t\t\t Cardiologist Specialist  ";
    cout<<"\n\t\t\t 3rd floor ";
    cout<<"\n\t\t\t Room-306 ";
    cout<<"\n\t\t\t Email: vishalparui1508@gmail.com";
    cout<<"\n\t\t\t Contact no:	8481088442";


    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

            doctorLogin() ;

        }
    }
}

void koushik1()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr. Koushik Paul ";
    cout<<"\n\t\t\t Bone Specialist ";
    cout<<"\n\t\t\t 4th floor ";
    cout<<"\n\t\t\t Room-406 ";
    cout<<"\n\t\t\t Email: koushikp72@gmail.com";
    cout<<"\n\t\t\t Contact no: 9831332681";

    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

            doctorLogin();

        }
    }

}

void soumyadip1()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr. Soumyadip Mukherjee ";
    cout<<"\n\t\t\t Anesthesiologists Specialist ";
    cout<<"\n\t\t\t 5th floor ";
    cout<<"\n\t\t\t Room-504 ";
    cout<<"\n\t\t\t Email: soumyadip450@gmail.com";
    cout<<"\n\t\t\t Contact no: 7044564290";

    char ch;
    cout<<"\n\n\n\t\t\t enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

            doctorLogin();

        }
    }
}

void akash1()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";;
    cout<<"\n\n\n\n\t\t\t Dr. Akash Roy";
    cout<<"\n\t\t\t Darmatologist Specialist ";
    cout<<"\n\t\t\t 6th floor ";
    cout<<"\n\t\t\t Room-606 ";
     cout<<"\n\t\t\t Email: aroy933050@gmail.com";
    cout<<"\n\t\t\t Contact no: 0196545514";

    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

            doctorLogin();

        }
    }

}

void saptak1()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr. Saptak Mondal ";
    cout<<"\n\t\t\t Critical Medicine Specialist ";
    cout<<"\n\t\t\t 5th floor ";
    cout<<"\n\t\t\t room-502 ";
     cout<<"\n\t\t\t email: saptak.mondal.on@gmail.com";
    cout<<"\n\t\t\t contact no: 9007920187";

    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

            doctorLogin();

        }
    }
 }

void preetam1()
{
    cout<<"\n\n\n\t\t\t\t\t Doctor Information   ";
    cout<<"\n\t\t\t\t\t____________________ ";
    cout<<"\n\n\n\n\t\t\t Dr. Preetam Das ";
    cout<<"\n\t\t\t Child Specialist  ";
    cout<<"\n\t\t\t 6th floor ";
    cout<<"\n\t\t\t room-306 ";
    cout<<"\n\t\t\t email: daspreetam50@gmail.com";
    cout<<"\n\t\t\t contact no:01796875752";

    char ch;
    cout<<"\n\n\n\t\t\t Enter 'b' to go back : ";
    cin>>ch;

    switch(ch)
    {
    case 'b':
        {
            system("cls");

            doctorLogin();

        }
    }
}

void doctor()
{

    system("cls");
    cout << "\n\n\n\n\n\t\t\t\t\t             Doctor Information  ";
    cout << "\n\t\t\t\t\t\t  ======================  ";
    cout << "\n\n";
    cout << "\n                                  id                name                       sector ";
    cout << "\n                                ------           -----------               ---------------              ";
    cout << "\n\n\t\t\t\t 01.        Dr. Vishal Parui       Cardiologist specialist          " << endl
         << endl;
    cout << "\t\t\t\t 02.        Dr. Koushik Paul           Bone Specialist                    " << endl
         << endl;
    cout << "\t\t\t\t 03.        Dr. Soumyadip Mukherjee   Anesthesiologists Specialist   " << endl
         << endl;
    cout << "\t\t\t\t 04.        Dr. Akash Roy            Darmatologist Specialist                 " << endl
         << endl; 
    cout << "\t\t\t\t 05.        Dr. Saptak Mondal       Critical Medicine specialist       " << endl
         << endl; 
    cout << "\t\t\t\t 06.        Dr. Preetam Das           Child Specialist        " << endl
         << endl;
    char ch;

    cout << "\n\n\n\n\t\t\t\t\t Doctor details press 'd'\n \t\t\t\t\t\t   Or\n\t\t\t\t\t Press 'g' to back : ";
    cin >> ch;

switch (ch)
    {
    case 'g':
        system("cls");
        doctorLogin();
    case 'd':
        system("cls");
        int a;
    cout << "\n\n\n\n\n\t\t\t\t\t             Doctor Information  ";
    cout << "\n\t\t\t\t\t\t  ======================  ";
    cout << "\n\n";
    cout << "\n                                  id                name                       sector ";
    cout << "\n                                ------           -----------               ---------------              ";
    cout << "\n\n\t\t\t\t 01.        Dr. Vishal Parui       Cardiologist specialist          " << endl
         << endl;
    cout << "\t\t\t\t 02.        Dr. Koushik Paul           Bone Specialist                    " << endl
         << endl;
    cout << "\t\t\t\t 03.        Dr. Soumyadip Mukherjee   Anesthesiologists Specialist   " << endl
         << endl;
    cout << "\t\t\t\t 04.        Dr. Akash Roy            Darmatologist Specialist                 " << endl
         << endl; 
    cout << "\t\t\t\t 05.        Dr. Saptak Mondal       Critical Medicine specialist       " << endl
         << endl; 
    cout << "\t\t\t\t 06.        Dr. Preetam Das           Child Specialist        " << endl
         << endl;
        cout << " Enter id : " ;
		cin >> a;
        switch (a)
        {
        case 1:
        {
            int count = 1;
            system("cls");
            vishal1();
            break;
        }
        case 2:
        {
            system("cls");
            koushik1();
            break;
        }
        case 3:
        {
            system("cls");
            soumyadip1();
            break;
        }

        case 4:
        {
            system("cls");
            akash1();
            break;
        }

        case 5:
        {
            system("cls");
            preetam1();
            break;
        }

        case 6:
        {
            system("cls");
            saptak1();
            break;
        }
        default:
            cout << "Wrong choice";
        }
        getch();
    }
}
int main()
{
    intro();

    getch();
}
