# 123
// CPP program to implement run length encoding 
#include <bits/stdc++.h> 
using namespace std; 

void printRLE(string str) 
{ 
	int n = str.length(); 
	for (int i = 0; i < n; i++) { 

		// Count occurrences of current character 
		int count = 1; 
		while (i < n - 1 && str[i] == str[i + 1]) { 
			count++; 
			i++; 
		} 

		// Print character and its count 
		cout << count << str[i]; 
	} 
} 

int main() 
{ 
	string str = "AAABBC"; 
	printRLE(str); 
	return 0; 
} 
