# code12
#include <stdio.h>

void hanoi(int n, char a, char b, char c)//将a中的n个盘，移动到c中
{
	if (n == 1)
	{
		printf("%c->%c\n",a,c);//表示将a中最上面的一个盘移动到c上
	}
	else
	{
		hanoi(n - 1, a, c, b);//将a中最上面的n-1个盘移动到b中
		printf("%c->%c\n",a,c);//表示将a中最上面的一个盘移动到c上,即a中现所剩的最后一个大盘
		hanoi(n - 1, b, a, c);//利用递归，将b中的n-1个盘移动到c中
	}
}
 
int main()
{
	int n;
	scanf("%d", &n);
	char A = 'a', B = 'b', C = 'c';
	hanoi(n, A, B, C);
	return 0;
}
