#include<iostream>
#include<unistd.h>
#include<stdlib.h>
#include<string>
#include<vector>
using namespace std;

void moveText();
void tailName();
void tailArrow();
void showTimes();
void userString();
void setSpeed();
void display();
void dispMenu();

int index1 , index2, index3, counter1, counter2, counter3, textT, size, speed;
string Name[78], tempString[78], Right[78], Left[78];
vector<string> temp_userString;


int main()
{
    int userChoice;

    do{
    dispMenu();
    cin >> userChoice;
        switch(userChoice){
            case 1:
                system("cls");
                moveText();
                tailName();
                tailArrow();

                showTimes();
                userString();

                display();
                break;
            case 2:
                system("cls");
                setSpeed();
                break;
            case 3:
                system("cls");
                break;
            case 0:
                system("cls");
                cout << "You exited the program." << endl;
                break;
            default:
                system("cls");
                cout << "Error: Undefind choice." << endl;
                break;
        }
    }while(userChoice != 0);

    return 0;
}

void dispMenu(){
    cout << "=======================" << endl;
    cout << "Enter 0 to exit." << endl;
    cout << "Enter 1 to start." << endl;
    cout << "Enter 2 set speed." << endl;
    cout << "Enter 3 to clear screen." << endl;
    cout << "Your choice: ";
}

void moveText()
{
    size = 78;
    counter1 = 0;
    counter2 = 0;
    counter3 = 0;
    speed = 130000;
}

void setSpeed(){
    int tempSpeed;
    cout << "Enter 0 for default." << endl;
    cout << "Enter 1 for fast." << endl;
    cout << "Enter 2 for middle." << endl;
    cout << "Enter 3 for slow." << endl;
    cin >> tempSpeed;

    system("cls");

    switch(tempSpeed){
        case 1:
            speed = 70000;
            break;
        case 2:
            speed = 300000;
            break;
        case 3:
            speed = 500000;
            break;
        default:
            speed = 130000;
            break;
    }
}

void tailName(){
    Name[28] = "A";
    Name[29] = "n";
    Name[30] = "d";
    Name[31] = "a";
    Name[32] = "m";
    Name[33] = "_";
    Name[34] = "J";
    Name[35] = "_";
    Name[36] = "A";
    Name[37] = "z";
    Name[38] = "i";
    Name[39] = "z";
    Name[40] = "_";
    Name[41] = ":";
    Name[42] = "_";
    Name[43] = "U";
    Name[44] = "S";
    Name[45] = "H";
    Name[46] = "_";
    Name[47] = "C";
    Name[48] = "S";
    Name[49] = "D";

    for(index1 = 0 ; index1 < size ; index1++){
        if(index1 < 28 || index1 > 49){
            Name[index1] = "_";
        }
    }
}

void tailArrow(){
    for(index1 = 0 ; index1 < size ; index1++){
        if(index1 % 2 == 0){
            Right[index1] = "-";
            Left[index1] = "<";
        }else{
            Right[index1] = ">";
            Left[index1] = "-";
        }
        tempString[index1] = " ";
    }
}

void showTimes(){
    cout << "How many times you want to show the text: ";
    cin >> textT;
    system("cls");
}

void userString(){
string tempUser_input = "", stringHolder ="";
    temp_userString.resize(0);
    int i, j;

    counter3 = 0;
    i = 0;

    cout << "Enter your string." << endl;
    cout << "Enter null to stop inputing." << endl;
    do{
        cin >> tempUser_input;
        if(tempUser_input != "null" && tempUser_input != "Null" && tempUser_input != "NULL"){
            temp_userString.push_back(tempUser_input);
            tempUser_input = " ";
            temp_userString.push_back(tempUser_input);

            for(string::iterator it=temp_userString[i].begin(); it!=temp_userString[i].end(); ++it){
                counter3++;
            }

            i++;

            for(string::iterator it=temp_userString[i].begin(); it!=temp_userString[i].end(); ++it){
                counter3++;
            }
        }else{
            break;
        }

        i++;
    }while(counter3 <= size);

    j = ((size/2) - (counter3/2));
    for(i = 0; i < temp_userString.size() ; i++){
        stringHolder ="";

        for(string::iterator it=temp_userString[i].begin(); it!=temp_userString[i].end(); ++it){
            if(j >= size){
                cout << "Error: You inputed alot." << endl;
                goto end;
            }

            j++;
            stringHolder = *it;
            tempString[j] = stringHolder;
        }
    }
    end: cout << endl << endl;
}


void display(){
    counter1 = size;
    counter2 = size;
    for(index1 = 1; index1 <= textT; index1++){
        for(index2 = 0; index2 <= size ; index2++){
            for(index3 = counter2; index3 < size ; index3++){
                cout << Name[index3];
            }

            cout << endl;

            for(index3 = counter2; index3 < size ; index3++){
                cout << Right[index3];
            }

            cout << endl;

            for(index3 = counter2; index3 < size ; index3++){
                cout << tempString[index3];
            }

            counter2--;
            usleep(speed);
            system("cls");
        }

        counter2 = 0;
        for(index2 = 0; index2 <= size ; index2++){
            for(index3 = counter2; index3 < size ; index3++){
                cout << Name[index3];
            }

            cout << endl;

            for(index3 = counter2; index3 < size ; index3++){
                cout << Left[index3];
            }

            cout << endl;

            for(index3 = counter2; index3 < size ; index3++){
                cout << tempString[index3];
            }

            counter2++;
            usleep(speed);
            system("cls");
        }
        counter2 = counter1;
    }
}
