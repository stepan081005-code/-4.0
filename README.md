#include <iostream>
#include <vector>
#include <clocale>
using namespace std;

int main()
{
    setlocale(LC_ALL, "Russian");

    cout << "Добро пожаловать в игру!!!\nСегодня 01.06.2026. Вы просыпаетесь на кровати в спальне\n";

    struct next
    {
        string room;
        string room2;
        string room3;
    };

    struct house
    {
        int nam;
        string room;
        vector<next> nextroom;
        vector<string> back;

    };

    struct player
    {
        string room;
        string hands;
        string back;
        string items;

    };


    vector<house> myrooms = {
    {0," спальня  ",{{" прихожая "}},{""}},
    {1," прихожая ",{{" спальня2 "},{" коридор "}},{" спальня \n"}},
    {2," спальня2 ",{{" балкон "}},{"прихожая"}},
    {3," коридор  ",{{" кухня   "},{" туалет " }, { " ванная " }},{ " прихожая \n"}},
    {4," кухня    ",{},{" коридор \n"}},
    {5," туалет   ",{},{" коридор \n"}},
    {6," ванная   ",{},{" коридор \n"}},
    {7," балкон   ",{},{" спальня2 \n"}}
    };

    //for (const house& item : myrooms) {
    //    cout << item.nam;
    //    cout << item.room;
    //    for (const next& room : item.nextroom) {
    //        cout << " можно перейти в: ";
    //        cout << room.room;
    //        cout << room.room2;
    //        cout << room.room3;
    //    }
    //    for (const string& room : item.back) {
    //        cout << " можно вернуться в: ";
    //        cout << room;
    //        if (room == "")
    //            cout << "некуда\n";
    //        }
    //}

}
