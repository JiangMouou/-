//详情见信息学奥赛1052计算邮资
  #include<stdio.h>
int main()
{
	int x, n, sum;
	char c;
	scanf("%d %c", &x, &c);
	sum = 8;
	if (x > 1000)
	{
			n = (x - 1000) / 500;
			if ((x - 1000) % 500 != 0)
				n ++ ;
			sum += 4 * n;
	}
	if (c == 'y'||c=='Y')
		sum += 5;
	printf("%d", sum);
	return 0;
}
//用于记录老师布置的作业和自己的练习

#include<stdio.h>
int main()
{
	int yu[12];
	int money;
	int cun = 0;
	int yue = 1;
	int s = 0;
	float sum;
	for (yue = 0; yue < 12; yue++)
	{
		scanf("%d", &yu[yue]);
		money = 300;
		money += s;
		if (money - yu[yue] < 0)
		{
			printf("%d", -(yue + 1));
			break;
		}
		if (money - yu[yue] > 100)
		{
			cun += ((money - yu[yue]) / 100 * 100);
			s = (money - yu[yue]) % 100;
		}
	}
	if (yue == 11)
	{
		sum = cun * 1.2;
		printf("%.2f", sum);
		return 0;
	}
}
//信息学奥赛1074
//答案没毛病，网站垃圾
#include<stdio.h>
int main()
{
	int yao, n;//药量和取药的人数
	int x=0;//没取到药的人
	int i;//计数器
	int qu;//每人取多少药
	scanf("%d%d", &yao,&n);
	for(i=0;i<n;i++)
	{
		scanf("%d", &qu);
		if(qu>yao)
				x++; 
		else
			yao -= qu;

	}
	printf("%d",x);
	return 0;
}

//1075



约三周的代码（因为U盘损坏，确实一部分）
辗转取余求两个数的最大公因数
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
int main()
{
	int x,y,n,a;
	n = 0;
	printf("请输入两个整数\n");
	scanf("%d%d",&y, &x);
	if (x < y)
	{
		a = x;
		x = y;
		y = a;
	}
	while (y!=0)
	{
		n = x % y;
		x = y;
		y = n;
	}
	printf("他们的最大公因数是%d", x);
	return 0;
}











#include<stdio.h>
int main()
{
	int a,b,c;
	a = 0;
	b = 1;
	c = 1;
	for (b=1; b <= 101; b += 2)
		{
			a += b*c;
			c = -c;
		}
	printf("%d", a);
	return 0;
}














#include  <stdio.h>
int fun(int  x)
{ int  n, s1, s2, s3, t;
  n=0;
  t=100;
/**********found**********/
  while(t<=999){
/**********found**********/
    s1=t%10;  s2=(t/10)%10;  s3=t/100;
/**********found**********/
    if(s1+s2+s3==x)
    {  printf("%d ",t);
       n++;
    }
    t++;
  }
  return  n;
}
void main()
{ int x=-1;
  while(x<0)
  { printf("Please input(x>0): ");  scanf("%d",&x);  }
  printf("\nThe result is: %d\n",fun(x));
}








求完数

#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
int main()
{
	int x, n, sum;
	printf("请输入一个整数\n");
	scanf("%d", &x);
	sum = 0;
	for (n = 1; n < x; n++)
	{
		if (x % n == 0)
		{
			sum += n;
		}
	}
	if (sum == x)
		printf("%d是完数", x);
	else
		printf("%d不是完数", x);
	return 0;
}






1月13号实训室面试题目第一题也是作业的第一道题

#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
int main()
{
	int x, n, sum;
	char c;
	scanf("%d %c", &x, &c);
	sum = 8;
	if (x<=1000)
		printf("%d",sum);
	else {
		if ((x - 1000) % 500 != 0)
		{
			n = (x - 1000) % 500 + 1;
			sum = 8 + 4 * n;
		}
		else
			n = (x - 1000) % 500;
	}
	if (c != 0)
		sum = sum + 5;
	else
		sum = sum;
	printf("%d", sum);
	return 0;
}
{{{{{{{{{{{{{{{{{{上为错误答案}}}}}}}}}}}}}}}}}
#include<stdio.h>
int main()
{
	int x, n, sum;
	char c;
	scanf("%d %c", &x, &c);
	sum = 8;
	if (x > 1000)
	{
			n = (x - 1000) / 500;
			if ((x - 1000) % 500 != 0)
				n ++ ;
			sum += 4 * n;
	}
	if (c == 'y'||c=='Y')
		sum += 5;
	printf("%d", sum);
	return 0;
}



#include <stdio.h>

int main() {
    int k, fib1 = 1, fib2 = 1, fibk = 0, i;

    // 读取输入的k值
    scanf("%d", &k);

    // 特殊情况处理，当k为1或2时，直接输出1
    if (k == 1 || k == 2) {
        printf("%d\n", fib1);
        return 0;
    }

    // 计算菲波那契数列的第k个数
    for (i = 3; i <= k; ++i) {
        fibk = fib1 + fib2; // 计算下一个数
        fib1 = fib2;       // 更新前一个数
        fib2 = fibk;       // 更新当前数
    }

    // 输出结果
    printf("%d\n", fibk);

    return 0;
}
1071










#include<stdio.h>
int main()
{
	int yu[12];
	int money;
	int cun = 0;
	int yue = 1;
	int s = 0;
	float sum;
	for (yue = 0; yue < 12; yue++)
	{
		scanf("%d", &yu[yue]);
		money = 300;
		money += s;
		if (money - yu[yue] < 0)
		{
			printf("%d", -(yue + 1));
			break;
		}
		if (money - yu[yue] > 100)
		{
			cun += ((money - yu[yue]) / 100 * 100);
			s = (money - yu[yue]) % 100;
		}
	}
	if (yue == 11)
	{
		sum = cun * 1.2;
		printf("%.2f", sum);
		return 0;
	}
}






1100（骑士的金币）
#include<stdio.h>
int main()
{
	int tian;
	scanf("%d", &tian);
	int sum = 0;
	int qian = 1;
	int n=1;
	for (int ri = 1; ri <= tian; ri++)
	{
		sum += qian;
		n++;
		if (n > qian)
		{
			qian++;
			n = 1;
		}
	}
	printf("%d", sum);
	return 0;
}





百钱买百鸡
#include<stdio.h>
int main()
{
	int g, m, c;
	int sum = 100;
	for (g = 0; g <= sum/5; g++)
	{
		for (m = 0; m <= sum/3; m++)
		{
			c = 100 - g - m;
			if (5 * g + 3 * m + c / 3 == sum && c % 3 == 0)
			{
				printf("%5d%5d%5d\n",g, m, c);
			}
		}
	}
	return 0;
}







数一的个数1095
#include<stdio.h>
int main()
{
	int x;
	scanf("%d", &x);
	int sum = 0;
	for (int n = 1; n <= x; n++)
	{
		int i = n;
		while(i>0)
		{
			if (i % 10 == 1)
				sum++;
			i /= 10;
		}
	}
	printf("%d", sum);
	return 0;
}





#include <stdio.h>
int main()
{
	int x;
	scanf("%d", &x);
	printf("%d=", x);
	int i = 1;
	for (i = 1; i <= x; i++)
	{
		if (x % i == 0 && i != 1)
		{
			x /= i;
			int z = i;
			printf("%d*", z);
		}
	}
	return 0;
}









#include <stdio.h>
#pragma warning (disable:4996)
void fun(long s, long* t)
{
    long sl = 10;
    s /= 10;
    /**********found**********/
    *t = s % 10;
    while (s > 0) {
        s /= 100;
        /**********found**********/
        t = s % 10 * sl + t;
        /**********found**********/
        sl /= 10;
    }
}

int main()
{
    long s, t;
    printf("\nPlease enter long number:");
    scanf("%ld", &s); fun(s, &t);
    printf("The result is: %ld\n", t);
}















2035
#include<stdio.h>
int main()
{
	int i, a[49];
	int in;
	scanf("%d", &in);
	for (i = 0; i < in; i++)
		scanf("%d", &a[i]);
	int x = a[0];
	for (i = 1; i < in; i++)
	{
		a[0] = a[i];
		a[i] = a[i + 1];
		a[i + 1] = a[0];
	}
	a[in - 1] = x;
	for (i = 0; i < in; i++)
		printf("%d ", a[i]);
	return 0;




冒泡排序
#include<stdio.h>
int main()
{
	int i, j, t;
	int a[10];
	for (i = 0; i < 10; i++)
		scanf("%d", &a[i]);
	for (i = 0; i < 9; i++)
	{
		for (j = 0; j < 9-i; j++)
		{
			if (a[j] > a[j + 1])
			{
				t = a[j];
				a[j] = a[j + 1];
				a[j + 1] = t;
			}
		}
	}
	for (i = 0; i < 10; i++)
	printf("%4d", a[i]);
	return 0;
}








#include<stdio.h>
int main()
{
	int i = 0;
	int a[10];
	int n, m;
	for (i = 0; i < 10; i++)
		scanf("%d", &a[i]);
	for (n = 1; n<=9-1; n++)
	{
		if (a[n] > a[n + 1])
		{
			m = a[n];
			a[n]=a[n+1];
			a[n+1]=m;
		}
	}



1107
#include <stdio.h>
#include <stdbool.h>

int main() {
    int L, M;
    scanf("%d %d", &L, &M);

    bool trees[L + 1];
    for (int i = 0; i <= L; i++) {
        trees[i] = true; // 初始化所有位置为有树
    }

    for (int i = 0; i < M; i++) {
        int start, end;
        scanf("%d %d", &start, &end);
        
        for (int j = start; j <= end; j++) {
            trees[j] = false; // 移除该区域的树
        }
    }

    int remaining_trees = 0;
    for (int i = 0; i <= L; i++) {
        if (trees[i]) { // 统计剩余的树
            remaining_trees++;
        }
    }

    printf("%d\n", remaining_trees); // 输出剩余的树的数量

    return 0;
}



#include<stdio.h>
int main()
{
	int m, n;
	int a[10000] = {0};
	scanf("%d%d", &m, &n);
	int cot=0;
	for (int i = 0; i <n; i++)
	{
		int x, y;
		scanf("%d%d", &x, &y);
		for (int j = x; j <= y; j++)
		{
			a[j] = 1;
		}
	}
	for (int i = 0; i < m; i++)
	{
		if (a[i] == 0)
		{
			cot++;
		}
	}
	printf("%d", cot);
	return 0;
}






2036开关门（补充：只有完全平方数的因数个数是奇数个）
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    for (int i = 1; i * i <= n; i++) {
        printf("%d ", i * i);
    }

    return 0;
}











#include<stdio.h>
int main()
{
	for (int i = 100; i < 1000; i++)
	{
		if (i % 10 == i / 100)
		{
			for (int j = 2; j * j <= i; j++)
			{
				if (i % j == 0)
					continue;
				else
					printf("%d ", i);
			}
		}
	}
	return 0;
}










k个3
#include<stdio.h>
int main()
{
	int x, y, z, a = 0, cot = 0;
	scanf("%d%d", &x, &y);
	if (x % 19 == 0)
	{
		for (z = 1; x > 0; x /= 10)
		{
			a = x % 3;
			if (a == 3)
			{
				cot ++;
			}
		}
		if (cot == y)
		{
			printf("YES");
		}
	}
	else
		printf("NO");
	return 0;
}










#include<stdio.h>
int main()
{
	int n;
	int a[10000];
	int b[10000];
	int c[10000];
	int d[10000];
	int x, y;
	int zong = -1;
	scanf("%d", &n);
	for (int i = 0; i < n; i++)
		scanf("%d %d %d %d", &a[i], &b[i], &c[i], &d[i]);
	scanf("%d %d", &x, &y);
	for (int i = n - 1; i >= 0; i--)
	{
		if (a[i] <= x && x <= a[i] + c[i] && b[i] <= y && y >= b[i] + d[i])
		{
			zong = i + 1;
			break;
		}
	}
	printf("%d", zong);
	return 0;
}






#include<stdio.h>
#include<string.h>
int main()
{
	char a[100000];
	int cnt[26] = { 0 };
	scanf("%s", a);
	for (int i=-;a[i];i++)
	{
		if()
	}
	return 0;
}
1130










#include<stdio.h>
int main()
{
	char a[10001];
	fgets(a, 10001, stdin);
	if (a[0] == ' ')
	{
		return 0;
	}
	else
	{
		for (int i = 0; a[i]; i++)
		{
			if (a[i] == ' ')
			{
				for (int j = i; a[j] != ' '; j--)
				{
					printf("%c", a[j]);
				}
			}
		}
	}
	return 0;
}
#include<stdio.h>
#include <string.h>
int main() {
    char a[501];//定义数组
    fgets(a, sizeof(a), stdin);//输入可以含空格的字符串
    int len = strlen(a);//获取字符串长度
    int start = 0;//起始位置
    for (int i = 0; i <= len; i++)//遍历字符串
    {
        if (a[i] == ' ' || a[i] == '\0' || a[i] == '\n')//遇到空格或字符串结束或换行符
        {
            for (int j = i - 1; j >= start; j--)//从当前位置向前输出
            {
                printf("%c", a[j]);//打印字符
            }
            if (a[i] != '\0' && a[i] != '\n')//遇到空格或字符串结束或换行符
            {
                printf("%c", a[i]);//打印空格或换行符
            }
            start = i + 1;//更新起始位置
        }
    }
    return 0;//结束程序
}//花括号，我也不知道为什么加注释了




yjwjwsld
ywdj2024
SJWDYWHY






12——5
#include<stdio.h>
int main()
{
	long a[100000],n,t;
	scanf("%d", &n);
	for (int i = 0; i < n; i++)
		scanf("%ld", &a[i]);
	for (int i = 0; i < n - 1; i++)
	{
		for (int j = 0; j < n - i - 1; j++)
		{
			if (a[j] > a[j + 1])
			{
				t = a[j];
				a[j] = a[j + 1];
				a[j + 1] = t;
			}
		}
	}
	for (int i = 0; i < n; i++)
	{
		if (a[i] != 0)
		{
			int cot = 1;
			for (int j = i + 1; j < n; j++)
			{
				if (a[i] == a[j])
				{
					cot++;
					a[j] = 0;
				}
			}
			printf("%ld %d\n", a[i], cot);
		}
	}
	return 0;
}
******************************************************************************************************************************************************
******************************************************************************************************************************************************
******************************************************************************************************************************************************
******************************************************************************************************************************************************
// 试验台的第一个实验，C语言实现顺序表的基本操作
// 实验内容：实现顺序表的基本操作，包括初始化、尾部添加元素、中间插入元素、删除元素、遍历输出、数据查找。
// 实验要求：1. 实现顺序表的基本操作，包括初始化、尾部添加元素、中间插入元素、删除元素、遍历输出、数据查找。
//          2. 实现结构体的使用，包括结构体的声明、结构体变量的定义、结构体变量的初始化、结构体变量的使用。
//          3. 实现malloc()函数和free()函数的使用。
// 实验难度：中级
// 实验时间：2025.4.12
#define _CRT_SECURE_NO_WARNINGS 1
#define MAXSIZE 100
typedef int ElemType;
#include<stdio.h>
#include<string.h>
typedef struct
{
	ElemType data[MAXSIZE];//不需要初始化 
	int length;
}
SqList;//定义顺序表结构
//在尾部添加元素
int appendElem(SqList* L, ElemType e)
{
	if (L->length >= MAXSIZE) {
		printf("顺序表已满\n");
		return 0;
	}
	L->data[L->length] = e;
	L->length++;
	return 1;
	printf("%d\n", L->length);
}
//中间插入元素
int insertElem(SqList* L, int pos, ElemType e)
{
	if (L->length >= MAXSIZE)
	{
		printf("顺序表已满\n");
		return 0;
	}
	if (pos<1 || pos>L->length)
	{
		printf("插入位置不合法\n");
		return 0;
	}
	if (pos <= L->length)
	{
		for (int i = L->length - 1; i >= pos - 1; i--)
		{
			L->data[i + 1] = L->data[i];
		}
		L->data[pos - 1] = e;
		L->length++;
		return 1;
	}
	return 1;
}
//删除元素
int deleteElem(SqList* L, int pos, ElemType* e)
{
	*e = L->data[pos - 1];
	if (pos < L->length)
	{
		for (int i = pos; i < L->length; i++)
		{
			L->data[i - 1] = L->data[i];
		}
	}
	L->length--;
	return 1;
}
//查找元素
int findElem(SqList* L, ElemType e)
{
	if (L->length == 0)
		return 0;
	for (int i = 0; i <= L->length; i++)
	{
		if (L->data[i] == e)
		{
			return i + 1;
		}
	}
	return 0;
}
//遍历输出
void listElem(SqList* L)
{
	for (int i = 0; i < L->length; i++) {
		printf("%d ", L->data[i]);
	}
	printf("\n");
}
void InitList(SqList* L)//初始化顺序表
{
	L->length = 0;
}
int main() {
	struct point {
		int x;
		int y;
		char zimu[20];
	};
	SqList list;
	InitList(&list);
	printf("初始化成功，目前长度占用%d\n", list.length);
	printf("目前占用内存%zu字节\n", sizeof(list.data));
	appendElem(&list, 100);
	appendElem(&list, 200);
	appendElem(&list, 300);
	appendElem(&list, 400);
	appendElem(&list, 500);
	listElem(&list);
	printf("目前长度占用%d\n", list.length);
	insertElem(&list, 3, 150);
	listElem(&list);
	deleteElem(&list, 4, &list.data[3]);
	listElem(&list);
	printf("500在第%d个位置\n", findElem(&list, 500));
	//输出被占用的内存大小
	//填入了两个数据，占用了两个空间，所以长度为2
	//没有.data时会多占用4字节（疑问）
	//下面是使用结构体的例子
	struct point p;
	p.x = 10;
	p.y = 20;
	strcpy(p.zimu, "字符串赋值strcpy()");
	printf("%s\n", p.zimu);
	printf("x=%d y=%d\n", p.x, p.y);
	struct point* pp = &p;
	pp->x = 30;
	(*pp).y = 40;
	printf("x=%d y=%d\n", p.x, p.y);
	ElemType a = 10;
	printf("a=%d\n", a);
	
	return 0;
}
//malloc()函数和free()函数的使用
//网课中第二个视频1小时左右教学使用
******************************************************************************************************************************************************
******************************************************************************************************************************************************
******************************************************************************************************************************************************
******************************************************************************************************************************************************
