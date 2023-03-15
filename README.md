#include <iostream>
using namespace std;

int main()
{
    int startH = 0, startM = 0, endH = 0, endM = 0;//先設定開始和結束的名稱

    cin >> startH >> startM;//開始的時間
    cin >> endH >> endM;//結束的時間
    int time = (endH * 60 + endM) - (startH * 60 + startM);//計算總時數
    if (time <= 120 && time >= 0) {
        cout << time / 30 * 30 << endl;//這定兩小時內的費用
    }
    else if (time > 120 && time <=240)
    {
        cout << (time - 120) / 30 * 40 + 120 << endl;//四個小時的費用+兩個小時的費用
    }
    else
    {
        cout << (time - 240) / 30 * 60 + 120 + 160 << endl;//四個小時的費用+四個小時的費用+兩個小時的費用
    }
    return 0;
}
