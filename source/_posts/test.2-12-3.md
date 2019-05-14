---
title: test.2.12-3
tags:
  - test.2.12-3
categories:
  - cpp.text
date: 2019-05-14 09:38:14
---

```
#include <stdio.h>
#define DAYS 365
int change(int years);

int main(void)
{
 int years;
 int ends;
 printf("输入你的年龄，0是退出。\n");
 while(years !=0){
  scanf("%d",&years);
  ends=change(years);
  printf("您的年龄换算成天数是%d\n",ends);
  printf("如果继续请继续输入年龄，否则=输入0\n");
 }
 return 0;
}
int change(int years)
{
 return(years*DAYS);
}
```
