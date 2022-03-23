#include<stdio.h>
#include<string.h>
int times(char s[],char substr[])
{
	int i =0, j, times=0;
	while(s[i])
	{
		j =0;
		while (substr[j])
		{
			if (substr[j] !=s[i + j])
				break;
			j++;
		}
		if (!substr[j])
		{
			times++;
			i += j -1;
		}
		i++;
	}
	return times;
}

int main()
{
	char s[100] =" ";
	printf("请输入字符串\n");
	gets(s);
	char substr[100]=" ";
	printf("请输入你想要统计的字符(小写)\n");
	scanf("%s",&substr);
	printf("次数有%d次\n",times(strlwr(s),substr));
		return 0;
}
