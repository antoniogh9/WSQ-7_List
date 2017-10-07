# WSQ-7_List
The function of this program is to read 10 values given by the user and then it returns the sum, average and standard deviation of those numbers.
#include <iostream>
#include <vector> //In order to use vectors
#include <math.h> //In order to use pow
using namespace std ;
int main () {

vector<float> List; //To create a vector of type float named List
float num, sum = 0, average, StandardDeviation, SDResult = 0 ;

cout << "Hi, enter your 10 values: " << endl ;

  //For the user to input his values
    for (int i = 1 ; i <= 10; ++i) {
      cout << "Enter a value: " ;
      cin >> num ;
      List.push_back (num) ;
    }

  //To add up all values given
    for (int i = 0 ; i < List.size () ; ++i) {
      sum = sum + List[i] ;
    }

  //To calculate the average
    average = sum / List.size () ;

    //To calculate standard deviation
    for(int i = 0; i < 10; ++i) {
         StandardDeviation += pow(List[i] - average, 2); //pow elevates a value to the n
    }
    SDResult = sqrt(StandardDeviation / 10); //sqrt is square root

//Output
  cout << endl << "The sum of those numbers is "<< sum << endl ;
  cout << "The average is "<< average << endl ;
  cout << "The standard deviation is " << SDResult << endl ;
  cout << endl << "Have a nice day random user!" << endl ;

return 0;
}
