#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;
int *sort_arr(int N[],int size)
{
    int hold;
    for(int i = 0;i<size;i++)
    {
        for(int j = 0;j<size;j++)
        {
            if(N[i]<N[j])
            {
               hold = N[i];
               N[i] = N[j];
               N[j] = hold;
            }
        }
    }
    return N;
}
int numnum(int N[], int size)
{
    int hold = 0;
    int num;
    for(int i = 0;i<size-1;i++)
    {
        if(N[i]!=N[i+1])
        {
            hold++;
        }
    }
    num = hold+1;
    return num;
}
int FA(int N[], int size)
{
    int HA[size];
    int hold = 1;
    int j = 0;
    int total = 0;

    for(int i = 0;i < size;i++)
    {
        if(N[i]!=N[i+1])
        {
            HA[j] = hold;
            j++;
            hold = 1;
        }
        if(N[i]==N[i+1])
        {
            hold++;

        }
    }
    sort_arr(HA,j);
    for(int i = 0;i<j-1;i++)
    {
        total= total+ HA[i];

    }

    return total;

}

int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */
    int n,size;
    int H;
    int count = 0;
    cin >> n;
    int ln[n+1];
    for(int i = 0;i<n;i++)
    {
        cin >> ln[i];
    }

    sort_arr(ln,n);
    size = numnum(ln,n);
    H = FA(ln,n);
    cout << H;


    return 0;
}
