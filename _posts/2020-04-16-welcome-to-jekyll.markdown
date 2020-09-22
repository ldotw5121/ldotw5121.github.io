---
layout: single
title:  "Welcome to Jekyll!"
date:   2020-04-16 01:31:35 +0900
categories: [ETC]
---
# 3주차 스택   201701721 황병화

1. **소스코드**

   ```c
   #include <stdio.h>
   #include <stdlib.h>
   #define MAX 8
   
   typedef int element;
   typedef struct{
   	element data[MAX];
   	int top;
   }stack;
   
   void initStack(stack* s) {
   	s->top = -1;
   }
   
   int isFull(stack* s) {
   	return (s->top == (MAX - 1));
   }
   
   
   void push(stack* s, element item) {
   	if (isFull(s)) {
   		printf("");
   		return;
   	}
   	else s->data[++(s->top)] = item;
   }
   
   
   int main() {
   	stack s;
   
   	int teemo = 1;
   	int soraka = 1;
   	int ashe = 1;
   	int kassadin = 1;
   	int lillia = 1;
   	int mejai;
   	
   	
   
   	initStack(&s);
   
   	mejai = s.top + 1;
   	mejai++;
   	
   	push(&s, soraka);
   	printf("선취점                     메사이의 영혼약탈자 %d 스택 \n", mejai);
   	mejai++;
   	push(&s, ashe);
   	
   	printf("더블킬                     메사이의 영혼약탈자 %d 스택 \n", mejai);
   	
   	mejai = s.top / 2 + 1;
   
   	printf("적에게 당했습니다          메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, teemo);
   	printf("적을 처치했습니다          메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, lillia);
   	printf("적을 처치했습니다          메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, kassadin);
   	printf("학살중입니다               메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai = s.top / 2 ;
   	printf("적에게 당했습니다          메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, teemo);
   	printf("적을 처치했습니다          메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, ashe);
   	printf("적을 처치했습니다          메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, soraka);
   	printf("더블킬                     메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, lillia);
   	printf("트리플킬                   메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, teemo);
   	printf("도저히 막을 수 없습니다    메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	push(&s, ashe);
   	printf("더블킬                     메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	push(&s, soraka);
   	printf("트리플킬                   메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	push(&s, lillia);
   	printf("쿼드라킬                   메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai = s.top / 2;
   	printf("적에게 당했습니다          메사이의 영혼약탈자 %d 스택 \n", mejai);
   
   	mejai++;
   	push(&s, kassadin);
   	printf("적을 처치했습니다          메사이의 영혼약탈자 %d 스택 \n", mejai);
   }
   ```

   

2. **실행결과**

![](https://user-images.githubusercontent.com/62733730/93905593-1922e500-fd36-11ea-9a07-5a21be4d753c.png)
