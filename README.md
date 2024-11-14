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
//答案不对，回去继续研究。
