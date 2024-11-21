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
