STL 에서 STL container를 위주로 사용하겠지만 이것은 STL에 있는 다양한 기능들을 쓰지 않게 된다. 따라서 algorithm 헤더 파일에 있는 좋은 function들을 소개한다.

먼저 <algorithm> 헤더를 추가한다.
STL에서는 갓벡터를 많이 이용하자.

	1. sort(first_iterator, last_itorator)
	주어진 벡터를 오름 차순 정렬한다. 세번쨰 parameter를 이용해서 다양하게 sort의 기준을 바꿀 수 있다. (또한 배열의 주소값을 넣어서 배열도 정렬가능하다.)
	2. reverse(first_iterator, last_iterator)
	벡터의 순서를 reverse시킨다.
	3. \*max_element(first_iterator, last_iterator)
	벡터의 원소중 최대값을 찾는다.
	4. \*Min_element(first_iterator, last_iterator)
	벡터의 원소중 최소값을 찾는다.
	5. Accumulation(first_iterator, lasr_iterator, initial value of sum)
	벡터 원소들의 합을 구한다.


// A C++ program to demonstrate working of sort(),
// reverse()
#include <algorithm>
#include <iostream>
#include <vector>
#include <numeric> //For accumulate operation
using namespace std;
 
int main()
{
    // Initializing vector with array values
    int arr[] = {10, 20, 5, 23 ,42 , 15};
    int n = sizeof(arr)/sizeof(arr[0]);
    vector<int> vect(arr, arr+n);
 
    cout << "Vector is: ";
    for (int i=0; i<n; i++)
        cout << vect[i] << " ";
 
    // Sorting the Vector in Ascending order
    sort(vect.begin(), vect.end());
 
    cout << "\nVector after sorting is: ";
    for (int i=0; i<n; i++)
       cout << vect[i] << " ";
 
    // Reversing the Vector
    reverse(vect.begin(), vect.end());
 
    cout << "\nVector after reversing is: ";
    for (int i=0; i<6; i++)
        cout << vect[i] << " ";
 
    cout << "\nMaximum element of vector is: ";
    cout << *max_element(vect.begin(), vect.end());
 
    cout << "\nMinimum element of vector is: ";
    cout << *min_element(vect.begin(), vect.end());
 
    // Starting the summation from 0
    cout << "\nThe summation of vector elements is: ";
    cout << accumulate(vect.begin(), vect.end(), 0);
 
    return 0;
}

Output
Vector before sorting is: 10 20 5 23 42 15
Vector after sorting is: 5 10 15 20 23 42
Vector before reversing is: 5 10 15 20 23 42
Vector after reversing is: 42 23 20 15 10 5
Maximum element of vector is: 42
Minimum element of vector is: 5
The summation of vector elements is: 115

	6. Count(first_iterator, last_iterator,x)
	X벡터의 위치를 반환한다. (0번쨰 위치에 있는 애를 1번 eleement로 인식)
	7. Find(first_iterator, last_iterator,x)
	Points to last address of vector ((name_of_vector).end()) if element is not present in vector. (벡터에 element가 존재하는지 확인 해준다)
	존재하지 않는 경우에 대해서는 실험해봐야 될듯.

<code>
// C++ program to demonstrate working of count()
// and find()
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
 
int main()
{
    // Initializing vector with array values
    int arr[] = {10, 20, 5, 23 ,42, 20, 15};
    int n = sizeof(arr)/sizeof(arr[0]);
    vector<int> vect(arr, arr+n);
 
    cout << "Occurrences of 20 in vector : ";
 
    // Counts the occurrences of 20 from 1st to
    // last element
    cout << count(vect.begin(), vect.end(), 20);
 
    // find() returns iterator to last address if
    // element not present
    find(vect.begin(), vect.end(),5) != vect.end()?
                         cout << "\nElement found":
                     cout << "\nElement not found";
 
    return 0;
}

<Output>
Occurrences of 20 in vector: 2
Element found





	8.
