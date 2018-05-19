# pangram
#include<iostream>
using namespace std;

bool che(string &str)
{
    int count[26] = {0}, i, j;
    for(i = 0; i < str.length(); i++)
    {
        if (str[i] >= 65 && str[i] <= 90)
            j = str[i] - 65;
        else if(str[i] >= 97 && str[i] <= 122)
            j= str[i] - 97;

        count[j] = count[j]++;
    }
    for (int i=0; i<=26; i++)
        if (count[i] == 0)
            return (false);

    return true;
}

int main()
{
    string str;
    cout<<"enter the string";
    cin>>str;
    if(che(str) == true)
            cout<<"Is a Pangram";
        else
            cout<<"Not a Pangram";

    return 0;
}
