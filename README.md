# Codeforcescpp-385A
#include <bits/stdc++.h>

using namespace std;

int main(){
  int n,c,ele;
  vector<int> v;
  cin >> n >> c;
  for(int i=0;i<n;i++){
    cin >> ele;
    v.push_back(ele);
  }
  int m = v.at(0)-v.at(1)-c;
  for(int i=1;i<n-1;i++){
    m = max(m,v.at(i)-v.at(i+1)-c);
  }
  cout << (m > 0 ? m: 0);
  return 0;
}
