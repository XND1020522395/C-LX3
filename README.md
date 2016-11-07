# C-LX3
// 2.cpp : 定义控制台应用程序的入口点。
//

#include "stdafx.h"
#include "iostream"

class CPerson
{
public:
	CPerson()
	{
		strcpy_s(name, "aaa");
		age = 20;
	}
	CPerson(int a)
	{
		strcpy_s(name, "ccc");
		age = a;
	}
	CPerson(char *n, int a)
	{
		strcpy_s(name, n);
		age = a;
	}
	int indata()
	{
		std::cin >> name;
		std::cin >> age;
		return 0;
	}
	int outdata()
	{
		std::cout << "姓名:" << name << std::endl;
		std::cout << "年龄：" << age << std::endl;
		return 0;
	}
private:
	char name[16];
	int age;
};

int main()
{
	CPerson myself;
	CPerson man1("bbb", 30);
	CPerson man2(40);
	myself.outdata();
	man1.outdata();
	man2.outdata();
    return 0;
}

