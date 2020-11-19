# zadanie-19.11

#include <fstream>
#include <iostream>
#include <bitset>

using namespace std;

int zero(int var, int nr) {
    return ((~(0b1<<nr)) & var);
}


int main()
{
    ifstream file;
    ofstream file2;
    file.open("a.txt");
    file2.open("b.txt");
    int a1,a2;
    if (file.good())
    {
        while (!file.eof()) {
            file>>a1>>a2;
            file2<<zero(a1,a2)<<endl;
            cout<<zero(a1,a2)<<endl;
        }  
    }

    file.close();
    file2.close();
    

    return 0;
}
