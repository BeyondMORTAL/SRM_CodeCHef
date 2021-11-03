# SRM_CodeCHef

# TASK 1

## Question 1

//compiler showing error
printf(" Enter a number",4589); should be
	-> printf("Enter a number", 4589) or
	-> printf("Enter a number")

//to get the last digit number	
LD = number / 10; should be -> LD = number % 10;


## Questions 3

//result * * * * runs infinitely
for(int i=1;i <= 4;i--) should be 
	->  for(int i=1;i <= 4;i++)

## Question 4

//if void main(), remove - return 0;
	or
//replace void main() to int main();

//a>10?printf("Yes");:printf("No"); should be ->
  a>10?printf("Yes"):printf("No");

## Question 5

int o; i; s; should be -> int o,i,s;
for(s=1 s<=5-o s++) should be -> for(s=1; s<=5-o; s++)
for (i=1 i<=o i++){ should be -> for (i=1; i<=o; i++){
cout>>"*";} should be -> cout<<"*";}
}}} should be -> }} // remove one extra '}'

## Question 7

#include <iostream>
using namespace std;	//added using namespace std
class test{
public:			//added public:
int my_variable;
};			//added ;
int main() {
test code_chef;
cin>>code_chef.my_variable;
if(code_chef.my_variable%2==0){
cout<<"Even";
}
else{
cout<<"odd";		//added "odd"
}
return 0;
}

## Question 8:

// using namespace std 
	should be 
-> using namespace std;

// for (j=start,j<=I,j++)
	should be
-> for (int j=start;j<=i;j++)

// break
	should be
-> break;




# TASK 2

## Question 1 ->

#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;


int main() {

	int i = 0;
	cout << "\n Please enter the number of words: ";
	cin >> i;
	cout << "\n";
	char dic[i];
	vector <string> words;
	vector <string> output;
	for (int j = 0; j < i; j++) {
		string a = "";
		cout << "\nPlease enter a word: ";
		cin >> a;
		words.push_back(a);
	}

	for (int j = 0; j < words.size(); j++) {
		string a = words[j];
		if (a.length() >= 4) {
			dic[j] = a[3];
		} else {
			dic[j] = a[a.length() - 1];
		}
	}

	for (int j = 0; j < i; j++) {
		for (int k = j; k < i; k++) {
			if (dic[j] < dic[k]) {
				string temp = words.at(k);
				words.at(k) = words.at(j);
				words.at(j) = temp;
			}
		}
	}

	reverse(words.begin(), words.end());

	for (int j = 0; j < i; j++) {
		cout << words.at(j) << "\n";
	}

}

## Question 2 ->

#include <iostream>
using namespace std;

int sort(int arr[], int n){
	int i,j,temp;
	for(i=0; i<n; i++){
		temp = arr[i];
		j=i+1;

		while(j>=0 && arr[j]>temp){
			arr[j+1]=arr[j];
			j=j-1;
		}
		arr[j+1]=temp;
	}
}
int main(){
	int n;
	cout<<"Enter size of array: ";
	cin>>n;
	cout<<"Enter the array: ";
	int arr[n];
	for(int i=0; i<n; i++){
		cin>>arr[i];
	}
	sort(arr, n);
	int k;
	cout<<"k = ";
	cin>>k;

	int result = arr[k-1];

	cout<<result<<" is the "<<k;

	switch (k){
    case 1: cout<<"st"; break;
    case 2: cout<<"nd"; break;
    case 3: cout<<"rd"; break;
    default: cout<<"th"; break;
	}

	cout<<" smallest element";

	return 0;
}

## Question 3 ->

#include <bits/stdc++.h>
using namespace std;

int main()
{
    char str[26] = {'a','c','e','g','i','k','m','o','q','s','u','w','y'};
    int i;
    for(i=0; i<26; i++)
    {
        if( (i % 2) == 1)
            str[i] = tolower(str[i]);
        else
            str[i] = toupper(str[i]);
    }
     cout<<str<<endl;
    return 0;
}

## Question 4 ->

