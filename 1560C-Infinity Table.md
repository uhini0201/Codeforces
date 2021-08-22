# Infinity Table

<span>Polycarp has found a table having an infinite number of rows and columns. The rows are numbered from 1, starting from the topmost one. The columns are numbered from 1, starting from the leftmost one.
Initially, the table hasn't been filled and Polycarp wants to fix it. He writes integers from 1 and so on to the table as follows.
  
<br><br>
 <img src="https://espresso.codeforces.com/aa1eece2e042a16fcbc09f2af100e73049fd8841.png" align="center" width="200px">

The figure shows the placement of the numbers from 1 to 10. The following actions are denoted by the arrows.
The leftmost topmost cell of the table is filled with the number 1. Then he writes in the table all positive integers beginning from 2 sequentially using the following algorithm.

First, Polycarp selects the leftmost non-filled cell in the first row and fills it. Then, while the left neighbor of the last filled cell is filled, he goes down and fills the next cell. So he goes down until the last filled cell has a non-filled neighbor to the left (look at the vertical arrow going down in the figure above).

After that, he fills the cells from the right to the left until he stops at the first column (look at the horizontal row in the figure above). Then Polycarp selects the leftmost non-filled cell in the first row, goes down, and so on.

A friend of Polycarp has a favorite number k. He wants to know which cell will contain the number. Help him to find the indices of the row and the column, such that the intersection of the row and the column is the cell containing the number k.

## Input
The first line contains one integer t (1≤t≤100) — the number of test cases. Then t test cases follow.

Each test case consists of one line containing one integer k (1≤k≤109) which location must be found.

## Output
For each test case, output in a separate line two integers r and c (r,c≥1) separated by spaces — the indices of the row and the column containing the cell filled by the number k, respectively.
 </span>

<span>
# Example
## input
7
11
14
5
4
1
2
1000000000
## output
2 4
4 3
1 3
2 1
1 1
1 2
31623 14130
</span>
  

  
# CODE

```
#include<bits/stdc++.h>
#include<algorithm>
#include<climits>
#include<vector>
#include<queue>
#include<map>
#include<utility>
#include<unordered_map>
#include<set>
#include<unordered_set>
#include<cstdio>
#include<cstring>
#define input(x) cin>>x
#define output(x) cout<<x
#define outputwithspace(x) cout<<x<<" "
#define outputwithnewline(x) cout<<x<<"\n"
#define S string
#define PQ priority_queue
#define Q queue
#define lli long long int
#define pb push_back
#define pob pop_back
#define pof pop_front
#define si second
#define fi first
#define mp(x,y) make_pair(x,y)
#define minpq priority_queue<lli,vector<lli>,greater<lli>>
#define maxpq priority_queue<lli>
#define pairL pair<lli,lli>
#define pairC pair<char,char>
#define pairCL pair<char,lli>
#define pairFI pair<int,char>
#define pairFL pair<lli,char>
#define PairPP pair<pair<lli,lli>,pair<lli,lli>>
#define mapL map<lli,lli>
#define mapC map<char,char>
#define mapCL map<char,lli>
#define mapFL map<lli,char>
#define mapPL map<pairL,lli>
#define IterM map<char,lli>::iterator
#define umapL unordered_map<lli,lli>
#define umapC unordered_map<char,char>
#define umapFL unordered_map<lli,char>
#define SL set<lli>
#define SC set<char>
#define VL vector<lli>
#define VC vector<char>
#define VS vector<S>
#define VPL vector<pair<lli,lli>>
#define VPC vector<pair<char,lli>>
#define VPF vector<pair<lli,char>>
#define Itervp vector<pair<lli,lli>>::iterator
#define ForI(i,a,b) for(lli i=a;i<b;i++)
#define ForPI(i,a,b) for(lli i=a;i<=b;i++)
#define ForD(i,a,b) for(lli i=a;i>b;i--)
#define ForPD(i,a,b) for(lli i=a;i>=b;i--)
#define WhileI(a,b) while(a<b)
#define WhilePI(a,b) while(a<=b)
#define WhileD(a,b) while(a>b)
#define WhilePD(a,b) while(a>=b)
#define co count
#define all(x) x.begin(),x.end()
#define FAST1 ios_base::sync_with_stdio(false);
#define FAST2 cin.tie(NULL);
#define MAXI 1000000000
using namespace std;


int main(){
    lli t;
    input(t);
    while(t--){
        lli n,i,j;
        input(n);
        lli k=ceil(sqrt(n));
        lli st=k*k;
        //outputwithnewline(k);
        lli di=st - k + 1;
        //outputwithnewline(di);
        if(n>=di && n<=st){
            i=k;
            j=1+(st-n);
        }
        else{
            j=k;
            i=k-(di-n);
        }
        outputwithspace(i);outputwithnewline(j);
    }
}

```
  
  
