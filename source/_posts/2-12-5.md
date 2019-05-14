---
title: test.2.12-5
tags:
  - test.2.12-5
categories:
  - cpp.text
date: 2019-05-14 11:36:55
---

```
#include <stdio.h>
void bra(void);
void ic(void);
void commia(void);//输出逗号函数
void br(void);//输出换行函数
int main(void)
{
 bra(),commia(),ic(),br();
 ic(),commia(),br();
 bra(),br();
 return 0;
}

void bra(void)
{
 printf("Brazil,Russia");
}
void ic(void)
{
 printf("India,China");
}
void commia(void)
{
 printf(",");
}
void br(void)
{
 printf("\n");
}
```
