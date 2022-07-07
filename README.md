# Sovmestnaya-rabota

// Казино.cpp: определяет точку входа для консольного приложения.
//

#include "stdafx.h"

#include <iostream>

#include <string> 

#include <cstdlib> 

#include <ctime>

using namespace std;

void rules();

int main()
{
	setlocale(LC_ALL, "RUS");
	
    int balance; // Баланс игрока
    
    int bettingAmount; //Количество ставок
    
    int guess; //Угадал или неугадал
    
    int dice; // Загадывается рандомное число
    
    char choice; // Выбор
    
    srand(time(0)); // Рандомный генератор
    
    cout << "\n\t\t========Добро пожаловать в казино=======\n\n";
    
    cout << "\n\nВыберите начальный баланс : $";
    
    cin >> balance; //Ваш баланс
    
    do
    
    {
        system("cls");// Отчистка экрана
	
        rules(); //Правила
	
        cout << "\n\nВаш текущий баланс $ " << balance << "\n";
	
// Указать размер ставки

        do
        {
	
            cout << "Теперь укажите ставку : $";
	    
            cin >> bettingAmount; //Ставка
	    
            if(bettingAmount > balance)// Сравнение ставки с балансом
	    
                cout << "Баланс ставок не может быть больше текущего баланса!\n"
		
                       <<"\nПовторно введите баланс\n ";
		       
        }while(bettingAmount > balance);// Сумма ставки больше баланса
	
