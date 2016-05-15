####Sort
1.quick sort

>c++版本

```c++
#include <iostream>
using namespace std;
void Qsort(int a[], int low, int high)
{
    if(low >= high)
    {
        return;
    }
    int first = low;
    int last = high;
    int key = a[first];/*用字表的第一个记录作为枢轴*/
 
    while(first < last)
    {
        while(first < last && a[last] >= key)
        {
            --last;
        }
 
        a[first] = a[last];/*将比第一个小的移到低端*/
 
        while(first < last && a[first] <= key)
        {
            ++first;
        }
         
        a[last] = a[first];    
       /*将比第一个大的移到高端*/
    }
    a[first] = key;/*枢轴记录到位*/
    Qsort(a, low, first-1);
    Qsort(a, first+1, high);
}
```
>javascript版本

```javascript
function quickSort(arr,l=0,h=arr.length-1){
	if(l>=h) return;
	var key=arr[l];
	var first=l,last=h;
	while(first<last){
		while(last>first&&arr[last]>=key) last--;
		arr[first]=arr[last];
		while(first<last&&arr[first]<=key) first++;
		arr[last]=arr[first];
	}
	arr[first]=key;
	quickSort(arr,l,first-1);
	quickSort(arr,first+1,h);
}
var a=[10,2,4,5,6,3,2,6];
quickSort(a);
console.log(a);
```