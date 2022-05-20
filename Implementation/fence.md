```C++
/**
 *  BIS-MILLAHIR RAHMANIR RAHIM
 *  author: Amin Hossain [tripplet]  
 *  Idea: bruteforce
 *  problem-link: https://codeforces.com/problemset/problem/363/B
**/

#include<bits/stdc++.h>
#include<string>
    
using namespace std;
typedef long long int ll;
typedef long double ld;
typedef unsigned long long int ull;
    
#define sf                scanf
#define pf                printf
#define pb                push_back
#define ppb               pop_back
#define MP                make_pair
#define PF                first
#define PS                second
#define si(n)             scanf("%d",&n)
#define sii(x,y)          scanf("%d %d",&x,&y)
#define siii(x,y,z)       scanf("%d %d %d",&x,&y,&z)
#define sl(n)             scanf("%lld",&n)
#define sll(x,y)          scanf("%lld %lld",&x,&y)
#define slll(x,y,z)       scanf("%lld %lld %lld",&x,&y,&z)
#define outn(x)           cout << x << "\n"
#define outg(x)           cout << x << " "
#define outt(x,y)         cout << x << " " << y <<"\n"
#define FOR(i,x,y)        for(int i=x;i<y;i++)
#define RFOR(i,x,y)       for(int i=x;i>=y;i--)
#define CLR(arr,val)      memset(arr,val,sizeof arr);
#define TC(case,t)        for(case=1;case<=t;case++)
    
#define pi                acos(-1) // 3.1415926535897932
#define mod               1000000007
#define mx                200002
#define base              10000000
#define mxp               100000
 
 
int dx[8] = {1,-1,0,0,-1,-1,1,1};
int dy[8] = {0,0,-1,1,-1,1,-1,1};
 
void inOut();
 
int arr[mx];
 
int main() {
 
    inOut();
    int tc, i, j, k, l, n;
    char ch; string str;
 
    sii(n, k);
    int sum = 0, ans = INT_MAX, idx = INT_MAX;
 
    FOR(i,0,n) si(arr[i]);
 
    FOR(i,0,k) sum += arr[i];
    FOR(i,k,n+1) {
        if(sum < ans) idx = i-k, ans = sum;
        sum -= arr[i-k], sum += arr[i];
    } 
 
    outn(idx+1);
 
    return 0;
}
    
    
void inOut()
{
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    
    #ifndef ONLINE_JUDGE
        //freopen("input.txt", "r", stdin);
        //freopen("output.txt", "w", stdout);
    #endif
}

```