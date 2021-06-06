# codechef-secondlargest-c++
#include<bits/stdc++.h>
using namespace std;
int main(){
    int t;
    cin>>t;
    int a,b,c,ar[t];
    for(int i=0;i<t;i++){
        cin>>a>>b>>c;
        if(a>b && a>c){
            a=0;
            if(b>c){
                ar[i]=b;
            }
            else
            ar[i]=c;
        }
        else
        if(b>c && b>a){
            b=0;
            if(a>c)
            ar[i]=a;
            else
            ar[i]=c;
        }
        else if(c>a && c>b){
            c=0;
            if(a>b)
            ar[i]=a;
            else
            ar[i]=b;
        }
    }
    for(int i=0;i<t;i++){
        cout<<ar[i]<<"\n";
    }
}
