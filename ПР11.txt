#include <iostream> 
#include <iomanip> 
#include "windows.h"
#include "string.h"
#include <cstdlib>
using namespace std;
int main()
{
	SetConsoleCP(1251);
	SetConsoleOutputCP(1251);
	char s1[100];
	cout << "Введіть символи: " << endl;
	gets_s(s1);
	int n=0;
	for (int i = 0; i < strlen(s1); i++)
		if (s1[i] == ' ')
		{
			n += 1;
		}
	if (n > 1)
	{
		for (int i = 0; i < strlen(s1); i++)
		{
			if (s1[i] == ' ')
			{
				for (i = i + 1; i < strlen(s1); i++) {
					if (s1[i] == ' ')
					{
						break;
					}
				cout << s1[i];

				}

			}

		}
	}
	else
	{
		cout << " ";
	}
	cout << endl;
	system("pause");
	return 0;
}
