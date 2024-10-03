# HASH_First_Challenge
## Program:
```c
#include <stdio.h>

int findMajorityElement(int arr[], int size) {
    int count, majorityElement = -1;

    // Iterate through each element in the array
    for (int i = 0; i < size; i++) {
        count = 0;

        // Count how many times arr[i] appears in the array
        for (int j = 0; j < size; j++) {
            if (arr[i] == arr[j]) {
                count++;
            }
        }

        // Check if the current element is the majority element
        if (count > size / 2) {
            majorityElement = arr[i];
            break;
        }
    }

    return majorityElement;
}

int main() {
    int size;

    // Get the size of the array from the user
    printf("Enter the size of the array: ");
    scanf("%d", &size);

    int arr[size];

    // Get the array elements from the user
    printf("Enter the elements of the array:\n");
    for (int i = 0; i < size; i++) {
        printf("Element %d: ", i + 1);
        scanf("%d", &arr[i]);
    }

    // Call the function to find the majority element
    int majorityElement = findMajorityElement(arr, size);

    // Output the result
    if (majorityElement != -1) {
        printf("The majority element is: %d\n", majorityElement);
    } else {
        printf("No majority element found.\n");
    }

    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/783d7297-b1e2-4f52-b520-a36a1a6035b7)
![image](https://github.com/user-attachments/assets/0d4a079f-a8fb-4419-825e-1fb046a12648)
![image](https://github.com/user-attachments/assets/95bf2af2-d66c-4a1a-8256-95542ee225d9)


