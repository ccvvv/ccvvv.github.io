---
title: for循环输出图形
tags:
  - for循环
categories:
  - cpp
date: 2019-05-23 18:54:49
---

### 最初三角图形
```
#include<stdio.h>
int main(void)
{
		int i,j;
		for (i=1;i<=3;i++){
			for (j=0;j<i;j++){
				printf("0");
			}
		printf("\n");
		}
		return 0;
}
```
#### 输出如下
```
0
00
000
```
---
### 让三角左右颠倒过来
```
/*原理和上面那个一样。只是让三角形左右颠倒的话需要额外创建变量k以输出空格。*/
#include<stdio.h>
int main(void)
{
		int i,j,k;
		for (i=1;i<=3;i++){
			for (k=3;k>i;k--){
				printf(" ");
			}
			for (j=0;j<i;j++){
				printf("0");
			}
		printf("\n");
		}
		return 0;
}
```
#### 输出如下
```
  0
 00
000
```
---
