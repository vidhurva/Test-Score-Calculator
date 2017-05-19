// Test-Score-Calculator
// This C++ Program allows the user to enter as many test scores as possible. Once the user exits the program, there will be data that displays the max, min and average test score. 

   #include <iostream>
   using namespace std;
   
   void calculateScores(int array[], int size, int& max, int& min, double& average)
    {
          int num[50];
          int i;
          int sum=0;
  
          max = array[0];
          min = array[0];
  
          sum += array[0];
  
          for (i=1;i < size;i++)
          {
               if(array[i] > max)
                {
                    max = array[i];
                }
  
                if(array[i] < min)
                {
                    min = array[i];
                }
  
                sum += array[i];
            }
  
            average = sum / size;
    }
  int main()
  {
  // initialization
          int num, temp;
          int test_score[50]; // The array is 50, meaning that the user can enter a maximum of 50 test scores. You can change the value of the array to whatever you like.
          int counter=0, max2, min2;
          double average2;
  
          for(num = 0; num < 50; num++)
          {
                  cout << "Enter a test score. Or type -1 to quit." << endl;
                  cout << "Enter a Test Score :";
                  cin  >> temp; 
 
                  if (temp != -1)
                  {
                      test_score[counter] = temp;
                      counter++;
                  }
                  else  // Program ends when user enters -1
                  {
                     break;
                  }
          }
  // Call by reference from the void, calculateScores
         calculateScores(test_score, counter, max2, min2, average2);
  
          cout << " The maximum score is " << max2 << endl;
          cout << " The minimum score is " << min2 << endl;
          cout << " The average score is " << average2 << endl;
          cout << " Have a nice day " << endl;
  
  return 0;
  }
