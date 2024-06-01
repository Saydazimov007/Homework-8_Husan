# Homework-8_Husan

#include <iostream>
#include <iomanip>
#include <vector>
using namespace std;

void fahrenheitToCelcius(double& fahrenheit) {
    double celsius = (fahrenheit - 32) * 5.0/9.0;
    fahrenheit = celsius;
}

void func(int *x, int *y) {
    *y = 7 * (*x) - 5;
}

int maxElement(int* arr, int size) {
    int max = arr[0];
    for (int i = 1; i < size; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}
 
//Problem 1

int main() {
    double temperature;
    
    cout << "Enter temperature in Fahrenheit: ";
    cin >> temperature;
    
    fahrenheitToCelcius(temperature);
    
    cout << "Temperature in Celsius: " << fixed << setprecision(4) << temperature << endl;
    
    return 0;
}

//problem2


    vector<int> numbers;
    
    int input;
    do {
        cin >> input;
        
        if (input != 0) {
            numbers.push_back(input % 2== 0 ? 2 : 1);
        }
    } while (input != 0);
    
    for (int num : numbers) {
        cout << num << " ";
    
    
    return 0;
}

//problem3


    int x, y;
    
    cout << "Enter a value for x: ";
    cin >> x;
    
    int *ptr_x = &x;
    int *ptr_y = &y;
    
    func(ptr_x, ptr_y);
    
    cout << "x: " << x << endl;
    cout << "y: " << y << endl;
    
    return 0;
}

//problem4

int n;
    cout << "Enter the size of the array: ";
    cin >> n;
    
    int arr[n];
    
    cout << "Enter the elements of the array: ";
    for(int i = 0; i < n; i++) {
        cin >> *(arr + i);
    }
    
    int count = 0;
    
    for(int i = 0; i < n; i++) {
        for(int j = i + 1; j < n; j++) {
            if(*(arr + i) == *(arr + j)) {
                count++;
                break;
            }
        }
    }
    
    cout << "Number of duplicates in the array: " << count << endl;

    return 0;
}

//problem5

int size1, size2;
    cin >> size1;
    
    int arr1[size1];
    for (int i = 0; i < size1; i++) {
        cin >> arr1[i];
    }
    
    cin >> size2;
    
    int arr2[size2];
    for (int i = 0; i < size2; i++) {
        cin >> arr2[i];
    }
    
    int max1 = maxElement(arr1, size1);
    int max2 = maxElement(arr2, size2);
    
    cout << "Output: " << max1 * max2 <<endl;

    return 0;
}
