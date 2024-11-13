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
