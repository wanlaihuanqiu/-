#include <stdio.h>
#include<string.h>
void main()
{ 
	char c[100];
	printf("输入一句优美的英文：");
	gets(c);
	printf("输出你需要统计的单词：");
	char ch[10];
	gets(ch);
		int count=0;
		for(int i=0;i<sizeof(ch);i++)
		{
			if(c[i]>='A'&&c[i]<='Z')
				c[i]=c[i]-32;
			for(int b=0;b<sizeof(ch);b++)
				if((c[i]==ch[b] || c[i+1]==ch[b+1]) && (c[i]!=' '&&c[i+1]!=' '))
						count++;
		}
	printf("%d",count);
}
