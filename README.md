# demo
this is my first git repo
#include <iostream>
using namespace std;
int main()
{
    int t,s,a,b,srow,erow,scol,ecol;
    cout << "Enter the value of t: ";
    cin >> t;
 
    for(int i=0;i<t;i++)
    {
    cout << "Enter the value of s: ";
    cin >> s;
    srow=0;
    erow=s-2;
    scol=1;
    ecol=s-2;
    char arr[s][s];
    while(srow<=erow && scol<=ecol)
    {
        for(int l=srow;l<erow;l++)
        arr[l][scol]='+';
        for(int l=scol;l<ecol;l++)
        arr[erow][l]='+';  
        for(int l=erow;l>srow;l--) 
        arr[l][ecol]='+'; 
        for(int l=ecol;l>scol+1;l--) 
        arr[srow+1][l]='+'; 
        srow+=2;   
        scol+=2;
        erow-=2;
        ecol-=2;    
    }
    
    for(int l=0;l<s;l++)
    {
        for(int m=0;m<s;m++)
        {
            if(arr[l][m]=='+')
            continue;
            else
            arr[l][m]='*';
        }
    }
       cout << "Enter the value of a and b: ";
       cin >> a >> b;
       cout << arr[a-1][b-1] << endl;
    }
    return 0;
}                        
