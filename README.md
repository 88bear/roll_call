# roll_call

# 打開meeting
* 1.點開顯示所有參與者
* 2.點F12
* 3.點console
* 4.點禁止符號刪除警告標語
* 5.複製下面註解的程式碼
* 6.回到chrome貼上後按Enter
* 7.複製擷取到的名單
* 8.回到這裡
* 9.按Run
* 10.貼上

``` cpp
#include <bits/stdc++.h>
using namespace std;

set<string> check;
map<string,int> num;

void init(set<string> &all){
  all.insert("name");num["name"] = number;
}

int main() {
  string input;
  init(check);

  while(getline(cin,input)){
    set<string> all,notsign,twice;
    init(all);

    stringstream ss(input);
    string name;
    while(ss >> name){
      if(all.count(name)){
        all.erase(name);
      }else if(check.count(name)){
        twice.insert(name);
      }else{
        notsign.insert(name);
      }
    }
    cout << '\n';
    if(!all.empty()){
      cout << "未到: ";
      for(auto i:all) cout << i << "(" << num[i] << ")" << ' ';
      cout << '\n';
    }else{
      cout << "全到\n";
    }
    if(!twice.empty()){
      cout << "重複參與者: ";
      for(auto i:twice) cout << i << ' ';
      cout << '\n';
    }
    if(!notsign.empty()){
      cout << "未登錄參與者: ";
      for(auto i:notsign) cout << i << ' ';
      cout << '\n';
    }
  }
  return 0;
}
```
