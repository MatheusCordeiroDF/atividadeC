#include <iostream>
#include <algorithm>

using namespace std;

void selection_sort(int A[], int n) {
    for(int i=0; i<n-1; i++) {
        int min_idx = i;
        for(int j=i+1; j<n; j++) {
            if(A[j] < A[min_idx]) {
                min_idx = j;
            }
        }
        swap(A[i], A[min_idx]);
    }
}

int main() {
    int A[] = {5, 2, 4, 6, 1, 3};
    int n = sizeof(A)/sizeof(A[0]);
    
    selection_sort(A, n);
    
    for(int i=0; i<n; i++) {
        cout << A[i] << " ";
    }
    cout << endl;
    
    return 0;
}
