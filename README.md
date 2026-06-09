#include <iostream>
using namespace std;

int main() {
    const int MAX_SIZE = 100;

    int size;
    int digits[MAX_SIZE];
    int result[MAX_SIZE + 1] ={0};

    // TODO: Read the size of the array
    cin >> size;
    cin.ignore();


    // TODO: Read the digits into the digits array
    for (int i = 0; i < size; i++){
        cin >> digits[i];
    }
    

    // TODO: Add one to the number stored in the array
    // Hint: Start from the last digit and move backward
    int carry = 1; 
    

    for (int i = size - 1 ; i >=0; --i){
     int sum = digits[i] + carry;
     result[i] = sum % 10;
     carry = sum /10;
    }
// handle carry output without segmentation fault or whitespace
// TODO: Print the result array
    if(carry > 0){
        cout << carry << " ";
        for (int i = 0; i < size; i++){
            cout << result[i];
            if (i < size-1){
                cout << " ";
            }
        }
    }else{
        for(int i = 0; i < size; i++){
            cout << result[i];
            if (i< size-1){
            cout << " ";
            } 
        }
    }


    // TODO: Print the result array
 


    return 0;
}
