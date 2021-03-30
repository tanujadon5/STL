```c
// vectors are the containers in STL
//Dynamic array
#include<iostream>
#include<vector>
using namespace std;

int main(){
    vector<int> a; //vector object
    vector<int> b(5,10);//five int each with value 10-init a vector of zeroes(n,0)
    vector<int>c(b.begin(),b.end());//init. c with element of vector b
    vector<int>d {1,2,3,4,5};

    //Iterate over the vector
    //1.
    for(int i = 0; i<c.size();i++){ //size defines no. of elements
        cout<<c[i]<<",";
    }
    cout<<endl;
    //Iterate using iterators
    //2.
    for(auto it = b.begin(); it!=b.end();it++){//auto it = b.begin()
        cout<<(*it)<<",";
    }
    cout<<endl;
    //it is a pointer ,that'll iterate over diff. locations in dynamic array
    //it is defined inside the vector class
    //3.
    for(int x : d){
        cout<<x<<",";
    }
    cout<<endl;
    //for every element x that lies in vector d


    //user input elements and add them to the vector
    vector<int> v; //vector of integers v
    int n;
    cin>>n;
    for(int i = 0; i<n; i++){
        int no;
        cin>>no;
        v.push_back(no);
    }
    for(int x : v){
        cout<<x;
    }
    cout<<endl;
    /*pushback does 2 things
    i. adds element to the end of vector
    ii. expands the memory/ doubles the memory */

    //difference between vector d & v at memory level

    cout<<"vector v"<<endl<<v.size()<<endl;
    cout<<v.capacity()<<endl; //size fo underlying array--large as we used pushback
    cout<<v.max_size()<<endl;//maxm no. of elements a vector can hold in worst case

    cout<<"vector d"<<endl<<d.size()<<endl;
    cout<<d.capacity()<<endl;
    cout<<d.max_size()<<endl;

    




return 0;
}
```
