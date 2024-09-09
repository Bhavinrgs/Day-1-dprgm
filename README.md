# Day-1-dprgm
#include<iostream>
using namespace std;
int function(int siz,int arr[])
{
    int a=0;
    int b=0;
    int c=siz - 1;
    while (b<=c) {
        if (arr[b]==0) {
            swap(arr[a],arr[b]);
            a++;
            b++;
        }
        else if (arr[b]==1) {
            b++;
        }
        else {
            swap(arr[b], arr[c]);
            c--;
         }
    }


}
int main(){
    int i;
    int siz;
    cout<<"enter the size of array: ";
    cin>>siz;
    int arr[siz];
    cout<<"enter elements in the array= ";
    for(i=0;i<siz;i++){
        cin>>arr[i];
    }
    cout<<function(siz,arr);
    cout<<"sorted array is --> ";
    for(i=0;i<siz;i++) {
        cout<<arr[i]<<" ";
    }
    cout<<endl;
   
   }
