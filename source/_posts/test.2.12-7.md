---
title: test.2.12-7
tags: test.2.12-7
categories: cpp.test
---
```
#include<stdio.h>
void sm(void);
void br(void);

int main(void)
{
	sm(),sm(),sm(),br();
	sm(),sm(),br();
	sm(),br();
	return 0;
}

void sm(void)
{
	printf("smile!");
}
void br(void)
{
	printf("\n");
}
```

