# Các kiến thức C++ cần có

## Nhập, xuất dữ liệu thông qua file

### Cú pháp

- Có khá nhiều cách để nhập và in ra dữ liệu qua file trong C++ nhưng mình sẽ hướng dẫn cách đơn giản và thuận tiện nhất đó là dùng hàm freopen().

Cấu trúc của hàm freopen() như sau: `FILE * freopen ( const char * filename, const char * mode, FILE * stream );` trong đó:

- filename: là tên file được mở
- mode: là cách truy cập file. Trong khóa học này, ta sẽ chỉ quan tâm đến hai cách truy cập file là “r” để đọc và “w” để ghi
- stream: con trỏ tới đối tượng FILE được nhận diện để mở lại
  Ví dụ:

```c++
#include<bits/stdc++.h>
using namespace std;

int main (){
    freopen("text.txt","w",stdout);
    cout << "Hello World" << endl;

    return 0;
}
```

Khi này, nếu các bạn vào folder chứa file code vừa thực thi sẽ thấy có một file text là “text.txt”. Các bạn mở với Notepad hoặc Codeblocks sẽ thấy dòng chữ “Hello World”.
Để đọc dữ liệu

```c++
#include<bits/stdc++.h>
using namespace std;

int main (){
    freopen("text.txt","r",stdin);
    string s;
    getline(cin, s);
    cout << s << endl;

    return 0;
}
```
