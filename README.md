int main()
{
    int num;
    cout<<"Press 1 to check current year is leap year or not"<<endl<<"Press 2 to check particular year is leap year or not\n";
    cin>>num;
    if(num==1)
    {
        lyear();
    }
    else if(num==2)
    {
        int year;
        cout<<"Enter the year to check the entered year is leap year or not\n";
        cin>>year;
          if(year%4==0)
   {
       if(year%100==0)
       {
           if(year%400==0)
           {
               cout<<"Entered year is a leap year";
           }
           else
           {
               cout<<"Entered year is Not a leap year";
           }
       }
       else
       {
           cout<<"Entered year is a leap year";
       }
   }
   else
   {
       cout<<"Entered year is not a leap year";
   }
    }
    else{cout<<"Enter between 1 and 2 only";}
    return 0;
}
 -------------------------------------------------------------------------------------------------------------
//Q.4)**Triangle Type:**Develop a program that takes three angles as input and determines whether the triangle is acute, obtuse, or right-angled using `if-else` statements.
#include<bits/stdc++.h>
using namespace std;
int main()
{
    int angle;
    cout<<"Enter an angle: ";
    cin>>angle;
    if(angle<90)
    {
        cout<<"Acute angle";
    }
    else if(angle==90)
    {
        cout<<"Right angle triangle";
    }
    else{cout<<"Obtuse";}
    return 0;
}
 -------------------------------------------------------------------------------------------------------------
//Q.5)**Positive, Negative, or Zero:**Create a C++ program that takes an integer as input and prints whether it is positive, negative, or zero using `if-else` statements.
#include<bits/stdc++.h>
using namespace std;
int main()
{
    int num;
    cout<<"Enter a number: ";
    cin>>num;
    if(num<0)
    {
        cout<<"Negative integer";
    }
    else if(num==0)
    {
        cout<<"Zero";
    }
    else{cout<<"Positive integer";}
    return 0;
}
 -------------------------------------------------------------------------------------------------------------
/*Q.6) **Login System:**
Implement a basic login system where the user enters a username and password. Use `if-else`statements to validate the login credentials.*/
#include<bits/stdc++.h>
using namespace std;
int main()
{
    string user_name="satish@123",password="satish123";
    string uname,passwd;
    cout<<"Enter user name\n";
    cin>>uname;
    cout<<"Enter password\n";
    cin>>passwd;
    if(user_name==uname && password==passwd)
    {
     cout<<"Login successfully";   
    }
    else if(user_name!=uname||password!=passwd)
    {
        for(int i=3; i>=1; i--)
        {
            cout<<"Invalid user name or password Please try again"<<endl;
            cout<<"You have only "<<i<<" attempts"<<endl;
            cout<<"Enter user name\n";
            cin>>uname;
            cout<<"Enter password\n";
            cin>>passwd;
            if(user_name==uname && password==passwd)
            {
                cout<<"Login successfully"<<endl;   
            }
        }
        cout<<"Try again after some time";
    }
    return 0;
}
 -------------------------------------------------------------------------------------------------------------
/*Q.7)**Traffic Light Simulation:**
Write a program that simulates a traffic light. The program should take user input for the current
signal and output the next signal using `if-else` statements.*/
#include<bits/stdc++.h>
using namespace std;
int main()
{
   string sig_nal; 
   cout<<"Enter the signal light color(Green,Yellow,Red)"<<endl;
   cin>>sig_nal;
   transform(sig_nal.begin(),sig_nal.end(),sig_nal.begin(),::tolower);
   if(sig_nal=="red")
   {
       cout<<"Next signal is Green";
   }
   else if(sig_nal=="yellow")
   {
       cout<<"Next signal is RED";
   }
   else if(sig_nal=="green")
   {
       cout<<"Next signal is Yellow";
   }
   else
   {
       cout<<"Not a signal light color";
   }
    return 0;
}
 -------------------------------------------------------------------------------------------------------------
/*Q.8)**Divisibility Checker:**
Create a program that checks if a given number is divisible by both 5 and 7. Use logical operators
within an `if` statement for the check.*/
#include<bits/stdc++.h>
using namespace std;
int main()
{
    int num;
    cout<<"Enter a number: ";
    cin>>num;
    if(num%5==0 && num%7==0)
    {
        cout<<"The number is divisible by both 5 and 7";
    }
    else
    {
        cout<<"The number is not divisible by both 5 and 7";
    }
    return 0;
}
 -----------------------------------------------------------------------------------------------------------------
/*Q.9)**Temperature Converter:**
Develop a program that converts temperatures between Celsius and Fahrenheit. Use `if-else`
statements to handle the conversion based on user input.*/
#include<bits/stdc++.h>
using namespace std;
int main()
{
    char choice;
    double temperature;
    double convertedTemperature;
    
    cout << "Choose the conversion type: " <<endl;
    cout << "a. Celsius to Fahrenheit" <<endl;
    cout << "b. Fahrenheit to Celsius" <<endl;
    cin >> choice;

    if (choice == 'a' || choice == 'A') {
        cout << "Enter temperature in Celsius: ";
        cin >> temperature;
        convertedTemperature = (temperature * 9.0 / 5.0) + 32.0;
        cout << "Temperature in Fahrenheit: " << convertedTemperature <<endl;
    } else if (choice == 'b' || choice == 'B') {
        cout << "Enter temperature in Fahrenheit: ";
        cin >> temperature;
        convertedTemperature = (temperature - 32.0) * 5.0 / 9.0;
        cout << "Temperature in Celsius: " << convertedTemperature <<endl;
    } else {
        cout << "Invalid choice" <<endl;
    }

    return 0;
}
 ------------------------------------------------------------------------------------------------------------------------
/*Q.10)**Largest of Three Numbers:**
Write a C++ program that takes three numbers as input and outputs the largest one using `if-else`
statements and relational operators.*/
#include<bits/stdc++.h>
using namespace std;
int main()
{
     int num1, num2, num3;

    cout << "Enter three numbers: ";
    cin >> num1 >> num2 >> num3;
    if (num1 > num2 && num1 > num3) {
        cout << "The largest number is: " << num1 << endl;
    } else if (num2 > num1 && num2 > num3) {
        cout << "The largest number is: " << num2 << endl;
    } else {
        cout << "The largest number is: " << num3 << endl;
    }
    return 0;
}
 -------------------------------------------------------------------------------------------------------------------------
/*Q.11) **Vowel or Consonant:**
Create a program that takes a character as input and determines whether it is a vowel or
consonant using `if-else` statements..*/
#include<bits/stdc++.h>
using namespace std;
int main()
{
     char ch;
    cout << "Enter a character: ";
    cin >> ch;
    ch = tolower(ch);
    if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
        cout << ch << " is a vowel." << endl;
    } else if (ch >= 'a' && ch <= 'z') {
        cout << ch << " is a consonant." << endl;
    } else {
        cout << "Invalid input. Please enter a valid character." << endl;
    }
    return 0;
}
 -----------------------------------------------------------------------------------------------------------------------------
/*Q.12)**Age Classifier:**
Write a program that classifies a person into different age groups (child, teenager, adult, senior)
based on their age using `if-else` statements.*/
#include<bits/stdc++.h>
using namespace std;
int main()
{
    int age;
    cout << "Enter your age: ";
    cin >> age;

    if (age >= 0 && age <= 12) {
        cout << "You are a child." << endl;
    } else if (age >= 13 && age <= 19) {
        cout << "You are a teenager." << endl;
    } else if (age >= 20 && age <= 64) {
        cout << "You are an adult." << endl;
    } else if (age >= 65) {
        cout << "You are a senior." << endl;
    } else {
        cout << "Invalid age input." << endl;
    }
    return 0;
}
 ---------------------------------------------------------------------------------------------------------------------------------

/*Q.14)**Palindrome Checker:**
Develop a program that checks if a given string is a palindrome (reads the same backward as
forward). Use `if-else` statements for the check.*/
#include<bits/stdc++.h>
using namespace std;
int main()
{
    string str;
    cout<<"Enter a string: ";
    cin>>str;
    string rev=str;
    reverse(rev.begin(),rev.end());
    if(rev==str)
    {
        cout<<"Palindrome";
    }
    else
    {
        cout<<"Not a Palindrome";   
    }
    return 0;
}
 ------------------------------------------------------------------------------------------------------------------------------------
/*Q.15)**BMI Calculator:**
Create a program that calculates the Body Mass Index (BMI) based on user input for height and
weight. Classify the BMI into different categories (underweight, normal, overweight) using `if-else`statements.*/
#include <iostream>
using namespace std;
    int main() {
    float weight, height, bmi;

    cout << "Enter your weight (in kilograms): ";
    cin >> weight;

    cout << "Enter your height (in meters): "; 
    cin >> height;

    bmi = weight / (height * height);

    if (bmi < 18.5) {
        cout << "Your BMI is: " << bmi << " - Underweight" << endl;
    } else if (bmi >= 18.5 && bmi < 25.0) {
        cout << "Your BMI is: " << bmi << " - Normal weight" << endl;
    } else {
        cout << "Your BMI is: " << bmi << " - Overweight" << endl;
    }
    return 0;
    }
-----------------------------------------------------------------------------------------------------------------------------------

/*Q.16)**Currency Converter:**
Write a program that converts currency from one unit to another. Use `if-else` statements to
determine the conversion based on the selected currency pair.*/
#include <iostream>
using namespace std;
int main(){
    const float INR_TO_USD = 0.012;
    const float USD_TO_INR = 80.04 ;  
    const float USD_TO_EUR = 0.85;
    const float USD_TO_GBP = 0.73;
    const float EUR_TO_USD = 1.18;
    const float GBP_TO_USD = 1.37;

    float amount;
    char fromCurrency, toCurrency;
    float convertedAmount;

    cout << "Enter the amount: ";
    cin >> amount;

    cout << "Enter the currency first letter (e.g., USD=U to EUR=E =U E ):\n";
    cin >> fromCurrency >> toCurrency;
    fromCurrency=toupper(fromCurrency),toCurrency=toupper(toCurrency);
    if(fromCurrency == 'I' && toCurrency == 'U'){
        convertedAmount = amount * INR_TO_USD;
        cout<< amount << " INR is equivalent to "<< convertedAmount << " USD."<<endl;
    }
    else if(fromCurrency == 'U' && toCurrency == 'I'){
        convertedAmount = amount * USD_TO_INR;
        cout<< amount << " USD is equivalent to "<< convertedAmount << " INR."<<endl;
    }
    else if(fromCurrency == 'U' && toCurrency == 'E') {
        convertedAmount = amount * USD_TO_EUR;
        cout << amount << " USD is equivalent to " << convertedAmount << " EUR." << endl;
    } else if (fromCurrency == 'U' && toCurrency == 'G') {
        convertedAmount = amount * USD_TO_GBP;
        cout << amount << " USD is equivalent to " << convertedAmount << " GBP." << endl;
    } else if (fromCurrency == 'E' && toCurrency == 'U') {
        convertedAmount = amount * EUR_TO_USD;
        cout << amount << " EUR is equivalent to " << convertedAmount << " USD." << endl;
    } else if (fromCurrency == 'G' && toCurrency == 'U') {
        convertedAmount = amount * GBP_TO_USD;
        cout << amount << " GBP is equivalent to " << convertedAmount << " USD." << endl;
    } else {
        cout << "Invalid currency pair." << endl;
    }
    return 0;
    }
---------------------------------------------------------------------------------------------------------------------------------

#include <bits/stdc++.h>
using namespace std;
int main() {
    string password;
    cout << "Enter your password: ";
    cin >> password;

    bool hasUpperCase = false;
    bool hasDigit = false;

    if (password.length() < 7) 
    {
        cout << "Password is too short. Minimum length is 8 characters." <<endl;
    } 
    else
    {
        for (char ch : password) 
        {
            if (isupper(ch)) 
            {
                hasUpperCase = true;
            } 
            else if (isdigit(ch)) 
            {
                hasDigit = true;
            }
        }

        if (hasUpperCase && hasDigit) {
            cout << "Password is strong." << std::endl;
        } else if (hasUpperCase) {
            cout << "Password is moderately strong (missing digits)." << endl;
        } else if (hasDigit) {
            cout << "Password is moderately strong (missing uppercase letters)." << endl;
        } else {
            cout << "Password is weak (missing uppercase letters and digits)." << endl;
        }
    }
    return 0;
}
-------------------------------------------------------------------------------------------------------------------------------------
/*Q.18)**Day of the Week:**
Create a program that takes a number representing a day of the week (1 for Sunday, 2 for Monday,
etc.) and prints the corresponding day using `if-else` statements..*/
#include <bits/stdc++.h>
using namespace std;
int main(){
    int dayNumber;

    cout << "Enter the day number (1 for Sunday, 2 for Monday, etc.): ";
    cin >> dayNumber;

    if (dayNumber == 1)
    {
        cout << "Sunday" << endl;
    } 
    else if (dayNumber == 2)
    {
        cout << "Monday" << endl;
    } 
    else if (dayNumber == 3) 
    {
        cout << "Tuesday" <<endl;
    } 
    else if (dayNumber == 4)
    {
        cout << "Wednesday" <<endl;
    } 
    else if (dayNumber == 5) 
    {
        cout << "Thursday" <<endl;
    } 
    else if (dayNumber == 6)
    {
        cout << "Friday" << endl;
    } 
    else if (dayNumber == 7) 
    {
        cout << "Saturday" << endl;
    } 
    else {
        cout << "Invalid day number. Please enter a number between 1 and 7." << endl;
    }

    return 0;
}

    ---------------------------------------------------------------------------------------------------------------------
/*Q.19)**Ticket Price Calculator:**
Write a program that calculates the ticket price for a movie based on age and time of day. Apply
discounts for children and seniors using `if-else` statements.*/
#include <bits/stdc++.h>
using namespace std;
int main(){
    const double CHILD_PRICE = 5.0;
    const double ADULT_PRICE = 10.0;
    const double SENIOR_PRICE = 8.0;
    const double CHILD_DISCOUNT = 0.5; 
    const double SENIOR_DISCOUNT = 0.8; 

    int age;
    char timeOfDay;
    float ticketPrice;
    
    cout << "Enter your age: ";
    cin >> age;

    cout << "Enter the time of day (M for morning, A for afternoon, E for evening): ";
    cin >> timeOfDay;

    if (age <= 12) { // Child
        ticketPrice = CHILD_PRICE;
        if (timeOfDay == 'M' || timeOfDay == 'A') {
            ticketPrice *= CHILD_DISCOUNT;
        }
    } else if (age >= 65) { // Senior
        ticketPrice = SENIOR_PRICE;
        if (timeOfDay == 'M' || timeOfDay == 'A') {
            ticketPrice *= SENIOR_DISCOUNT;
        }
    } else { // Adult
        ticketPrice = ADULT_PRICE;
    }

    cout << "The ticket price is: " << ticketPrice <<" rupee"<< endl;

    return 0;
}

    ------------------------------------------------------------------------------------------------------------------------
/*Q.20)**Character Classification:**
Develop a program that classifies a given character into categories such as uppercase letter,
lowercase letter, digit, or special character using `if-else` statements.*/
#include <bits/stdc++.h>
using namespace std;
int main(){
  char ch;

    cout << "Enter a character: ";
    cin >> ch;

    if (isupper(ch)) {
        cout << ch << " is an uppercase letter." <<endl;
    } else if (std::islower(ch)) {
        cout << ch << " is a lowercase letter." << endl;
    } else if (isdigit(ch)) {
        cout << ch << " is a digit." << endl;
    } else {
        cout << ch << " is a special character." << endl;
    }

    return 0;
}

 -----------------------------------------------------------------------------------------------------------------------------
/*Q.21)**Electricity Bill Calculator:**
Create a program that calculates the electricity bill based on the units consumed. Apply different
rates for different consumption ranges using `if-else` statements.*/
#include <bits/stdc++.h>
using namespace std;
int main(){
    float units, billAmount;
    cout << "Enter the number of units consumed: ";
    cin >> units;
    if (units <= 100) {
        billAmount = units * 1.5;
    } else if (units>100 && units <= 200) {
        billAmount = 100 * 2 + (units - 100) * 2;
    } else {
        billAmount = 100 * 1.5 + 100 * 2 + (units - 200) * 2.5;
    }

    cout << "Electricity bill amount: $" << billAmount << endl;

    return 0;
}

 ------------------------------------------------------------------------------------------------------------------------------
/*Q.22)**Game of Rock, Paper, Scissors:**
Write a simple rock-paper-scissors game where the user plays against the computer. Use `if-else`
statements to determine the winner.*/
#include <bits/stdc++.h>
using namespace std;
int main(){
    srand(time(nullptr));
    int userChoice, computerChoice;
    cout << "Enter your choice (1 for Rock, 2 for Paper, 3 for Scissors): ";
    cin >> userChoice;
    computerChoice = rand() % 3 + 1;
     
    if (userChoice == computerChoice) {
        cout << "It's a tie!" << endl;
    } else if ((userChoice == 1 && computerChoice == 3) || (userChoice==2 && computerChoice == 1)||(userChoice == 3 && computerChoice == 2)) {
        cout << "Congratulations! You win!" <<endl;
    } else {
        cout << "Sorry, the computer wins!" << endl;
    }
    return 0;
}

-----------------------------------------------------------------------------------------------------------------------------------
/*Q.23)**Bookstore Discount Calculator:**
Implement a program that calculates the total cost of books after applying discounts based on the
quantity purchased. Use `if-else` statements to determine the discount rate.
Purchased above Rs 10000 then discount 5%
Purchased above Rs 20000 then discount 10%
Purchased above Rs 30000 then discount 15%*/
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    float totalCost, discountedCost;
    cout << "Enter the total cost of books: Rs ";
    cin >> totalCost;

    if (totalCost > 30000) {
        discountedCost = totalCost * (1 - 0.15);
    } else if (totalCost > 20000) {
        discountedCost = totalCost * (1 - 0.10);
    } else if (totalCost > 10000) {
        discountedCost = totalCost * (1 - 0.05);
    } else {
        discountedCost = totalCost; 
    }

    cout << "Total cost after applying discounts: Rs " << discountedCost <<endl;

    return 0;
}

    ----------------------------------------------------------------------------------------------------------------------------------------
/*Q.24)**Sorting Three Numbers:**
Write a program that takes three numbers as input and prints them in ascending order using `if-
else` statements and relational operators.*/
#include <bits/stdc++.h>
using namespace std;
int main(){
  int num1, num2, num3;
    cout << "Enter three numbers: ";
    cin >> num1 >> num2 >> num3;
    if (num1 > num2) {
        int temp = num1;
        num1 = num2;
        num2 = temp;
    }
    if (num2 > num3) {
        int temp = num2;
        num2 = num3;
        num3 = temp;
    }
    if (num1 > num2) {
        int temp = num1;
        num1 = num2;
        num2 = temp;
    }
    cout << "Numbers in ascending order: " << num1 << " " << num2 << " " << num3 <<endl;

    return 0;
}

    -----------------------------------------------------------------------------------------------------------------------------------------
Q26.Write a program that takes the current time as input and prints a message based on whether it's
morning, afternoon, evening, or night.

#include <bits/stdc++.h>
using namespace std;

int main() {
    // Get the current time point in UTC
    auto currentTimePoint = chrono::system_clock::now();

    // Get the time zone offset for IST (Indian Standard Time)
    constexpr int istOffsetHours = 5;
    constexpr int istOffsetMinutes = 30;

    // Adjust the current time point for IST
    currentTimePoint += chrono::hours(istOffsetHours) + chrono::minutes(istOffsetMinutes);

    // Convert the time point to a time_t object
    time_t currentTime = chrono::system_clock::to_time_t(currentTimePoint);

    // Convert the time_t object to a tm structure
    tm* localTime = std::localtime(&currentTime);

    // Extract the hour part
    int hour = localTime->tm_hour;

    //yaha se dsa lagega
   
    if(hour>=6 && hour<12)
    {
        cout<<"Morning";
    }
    else if(hour>=12 && hour<18)
    {
        cout<<"After Noon";
    }
    else if(hour>=18 && hour<21)
    {
        cout<<"Evening";
    }
    else if( (hour>=21 && hour<24) || (hour>=0  && hour<6) )
    {
        cout<<"Night";
    }

    return 0;
}

---------------------------------------------------------------------------------------------------------------------------------------
Q27.Write a program that takes an integer as input and prints whether it is a positive or negative number.

#include <iostream>

using namespace std;

int main() {
    int number;

    cout << "Enter an integer: ";
    cin >> number;

    if (number > 0) {
        cout << number << " is a positive number." << endl;
    } else if (number < 0) {
        cout << number << " is a negative number." << endl;
    } else {
        cout << "The number entered is zero." << endl;
    }

    return 0;
}

---------------------------------------------------------------------------------------------------------------------------------------
