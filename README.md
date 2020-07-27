# C--7.27
#include<stdio.h>//用递归的思想将1234 ---> 1 2 3 4

void print(int x)
{
	if (x >= 9)
	{
		print(x /10);
	}
	printf("%d ", x% 10);
}
int main()
{
	//1234 ---> 1 2 3 4
	int a = 1234;
	print(a);
	
	return 0;
}

#include<stdio.h>//用递归的思想输出字符串长度
#include<string.h>//不允许创建临时变量
int my_strlen(char* str)
{
	if (*str != '\0')
	{
		return 1+my_strlen(str+1);

	}
	else
	return 0;
}
int main()
{
	char arr[] = "hello world";
	int len=my_strlen(arr);
	printf("%d\n", len);
	return 0;
}
