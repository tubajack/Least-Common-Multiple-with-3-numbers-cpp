# Least-Common-Multiple-with-3-numbers-cpp
C++ program. LCM with 3 numbers 


#include <iostream>
using namespace std;

int lcm(int, int, int);

int main(){

    int leastcommon;
    int L1, L2, L3;
    while(cin >> L1 >> L2 >> L3){
        leastcommon = lcm(L1, L2, L3);
        cout << leastcommon << endl;
    }
    return 0;
}

int lcm(int a, int b, int c){
    int L1 = a;
    int L2 = b;
    int L3 = c;
    long long int maxpower, flag = 0, leastcommon;

    if(a >= b && a >= c){
        maxpower = a;
    }
    else if(b >= a && b >= c){
        maxpower = b;
    }
    else if(c >= a && c >= b){
        maxpower = c;
    }
    for(int i = 1; flag == 0; i++){
        leastcommon = maxpower * i;
        if((leastcommon % a == 0) && (leastcommon % b == 0) && (leastcommon % c == 0)){
            flag = 1;
        }
    }
    return leastcommon;
}
