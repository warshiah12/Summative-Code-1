# Summative-Code-1
#include<iostream>
using namespace std;
int main()
{
	string firstname, secondname;    /*declaring variables 'firstname' and 'secondname' with datatype string and 
	                           variable 'age','sum','s1marks','s2marks','avg' with datatype int*/
	int age;
	int sum, s1marks,s2marks;
	int avg;
	cout << "Enter your first and second name: " << endl;     
	cin >> firstname>>secondname;           
	cout << "Enter your age: " << endl;
	cin >> age;
	cout << "Marks of first subject : " << endl;
	cin >> s1marks;
	cout << "Marks of second subject : " << endl;
	cin >> s2marks;
	if ((s1marks > 0 && s1marks <= 100) && (s2marks > 0 && s2marks <= 100))   /*if the marks are within the range of 0 to 100 then control will move to the calculation
		                                                                       of marks */
	{
		sum = s1marks + s2marks;    
		avg = sum / 2;
		cout << "The average marks are: " << avg << endl;
		switch (avg/10)     //divides the average marks by 10 and displays the appropriate result
		{
		case 10:
		case 9:
		case 8:
		case 7:            //if marks are within the range of 70-100 then the following statement will be displayed
			cout << "\n"<<firstname << " " << secondname << "\nAge: " << age << "\n" << "Marks Obtained: " << avg << "\nYou got Grade A " << endl;
			break;
		case 6:            //if marks are within the range of 60-69 then the following statement will be displayed
			cout << "\n"<<firstname << " " << secondname << "\nAge: " << age << "\n" << "Marks Obtained: " << avg << "\nYou got Grade B " << endl;
			break;
		case 5:           //if marks are within the range of 50-59 then the following statement will be displayed
			cout << "\n"<<firstname << " " << secondname << "\nAge: " << age << "\n" << "Marks Obtained: " << avg << "\nYou got Grade C " << endl;
			break;
		case 4:           //if marks are within the range of 40-49 then the following statement will be displayed
			cout << "\n"<<firstname << " " << secondname << "\nAge: " << age << "\n" << "Marks Obtained: " << avg << "\nYou got Grade D " << endl;
			break;
		default:          //if marks are below than 40 then the following statement will be displayed
			cout << "\n"<<firstname << " " << secondname << "\nAge: " << age << "\n" << "Marks Obtained: " << avg << "\nYou got Grade F " << endl;
			break;
		}
	}
	else
	{
		cout << "Invalid marks. Please enter the marks within the range of 0-100" << endl;
	}
	return 0;
}
