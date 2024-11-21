#include <iostream>
using namespace std;

int  linear(int a[],int n,int s){
    for(int i=0;i<=s;i++){
        if(n==a[i]){
           return i;
        }
       
    }
    return -1;
}

int main() {
 int n=10;
 int a[]={4,0,1,7,3,20};
 int s= sizeof(a)/sizeof(a[0]);
 int location= linear(a,n,s);
cout<< location;
}

--------------------------------
binary search
#include <iostream>
using namespace std;

int  binary(int a[],int key,int size){
    int left=0;
    int right=size;
    int mid;
    while(left<=right){
        mid=(left+right)/2;
        
        if(key==a[mid]){
            return mid;
        }
        else if(a[mid]>key){
            right=mid-1;
        }
      else{
            left=mid+1;
        }
    }
    return -1;
}

int main() {
 int key=6;
 int a[]={1,2,3,4,5,6,7,8,9};
 int size= sizeof(a)/sizeof(a[0]);
 int location= binary(a,key,size);
cout<< location;
}
