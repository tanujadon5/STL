```c
#include<iostream>
#include<vector>
using namespace std;
int main(){
    vector<int> d = {10,30,50,60,70};
    //Push back time complexity is O(1)
    d.push_back(90);

    //Pop back - removes the last element from vector, doesn't return it - O(1)
    d.pop_back();

    //Insert some elemnts in the middle-O(N) N = no. of elements u'veadded
    d.insert(d.begin()+3,4, 60);//first specify the position ,no. of elemnts, value of each element

    for(int x: d){
        cout<<x<<",";
    }
    cout<<endl;
    //erase some elements in the middle
    d.erase(d.begin()+2);
    d.erase(d.begin()+2,d.begin()+4);//erase element from 2 to 3
    for(int x: d){
        cout<<x<<",";
    }
    cout<<endl;
    //size - returns no. of elements
    cout<<d.size()<<endl; 
    cout<<d.capacity()<<endl; //returns the no. of elements vector can hold
    //as we used insert function to add elemnts thus capacity is more than size

    //resize- returns the vector to the specified no. of elemnts ,capacity is not changed
    d.resize(9);
    cout<<d.capacity()<<endl;

    d.resize(20);//if the size is incfeasing more memory will be allocated
    cout<<d.capacity()<<endl;//capacity will change now as the size is increased

    for(int x :d){
        cout<<x<<",";
    }
    cout<<endl;
    //Remove all the elements of vector
    //cout<<d.clear()<<endl;
    //cout<<d.size()<<endl ; size - 0
    //cout<<d.capacity()<<endl; capacity - 20

    //empty - to check if vector is empty or not
    if(d.empty()){
        cout<<"This is an empty vector "<<endl;
    }
    else{
        cout<<"not";
    }

    //frontmost element and last element
    cout<<d.front()<<endl;
    cout<<d.back()<<endl;

    //Doubling is an expensive operation as everytime you pushback,
    //memory looks for larger(double the size) array and copy the elements into it
    //thus, we will use reserve function
    //when you insert 1 element - capacity - 1
    // --- ----- ---- 2 element - capacity - 4(doubles)
    //-----------------3 elemnt - capacity - 4
    //------------------4 elemnt - capacity - 8
    //-------------------5 elemnt - capacity - 8
    //unless we fill the 8th element, capacity will be 8

    vector<int> v;
    int n;
    cin>>n;
    //v.reserve(100);
    for(int i = 0; i<n; i++){
        int no;
        cout<<"enter the limit :"<<endl;
        cin>>no;
        v.push_back(no);
        cout<<"Capacity is "<<v.capacity()<<endl;
    }
    for(int x: v){
        cout<<x<<",";
    }
    cout<<endl;
    //doubling is time taking and expensive operation

    //thus use reserve function beforehand ,and tell compiler that this much memory you want



return 0;
}
```
