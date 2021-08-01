#include <iostream>
using namespace std;


int max_sm(int *sm , int no) 
{
	int max = 0 ;   // declearing variable to store maximum value
	for(int i = 0; i < no ; i++)     
	{
        	if(max < *sm)           
		{
		    max = *sm;       
		}             
		*sm++;        	  
	}
	return max ;        
    
}


int min_sm(int *s_m , int num )
{
	int min;  // declaring variable to store minimum value
	for(int i = 0; i < num ; i++) 
	{                                
        	if(min > *s_m)         
		{                      
		    min = *s_m;       
		}                      
		*s_m++;        
	}                                      
	return min ;                   
    
}

int main()
{
	int  m1, m2 ;
	int student_marks[100] , n , ch , i ;
	
	cout<<"Enter the number of students whose marks you wish to enter."<<endl; 
	cin >> n;
	
	cout << "Enter the marks: ";   
	for (i=0; i<n;i++)
	{
		cin >> student_marks[i];
	}
	cout << endl;
	
	do
	{
		cout << "1. Maximum " << endl;
		cout << "2. Minimum " << endl;
		cout << "3. Exit " << endl;
		cout << "Please enter a choice :";
		cin >> ch;
		cout << endl;
		
		switch(ch)
		{
			case 1: m1 = max_sm(student_marks, n);
				cout <<"Maximum value is: "<< m1 <<endl;
			        break;
			case 2: m2 = min_sm(student_marks, n);
			        cout <<"Minimum value is: "<<m2 <<endl;
			        break;
			case 3:
			        break;
			default: cout <<"Invalid choice";                	  
		}
		
	}while(ch != 3);
}
