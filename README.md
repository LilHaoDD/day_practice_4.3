# 	day_practice_4.3  c语言
daily_practice_4
#first   i got to learn C  and  then  Python
#include<stdio.h>

int main()
{
	char a = 'a';
	char* p = &a;
	*p='b';
	printf("%p\n",p);
	printf("%d\n",sizeof(p));
	return 0 ;
}


#include <math.h>
int main()
{
	double a,b,c,disc,x1,x2,p,q;
	scanf("%lf%lf%lf",&a,&b,&c);
	disc=sqrt(b*b-4*a*c);
	p = -b/(2*a);
	q = -disc/(2*a);
	x1=p+q;
	x2=p-q;
	printf("x1=%7.2f\n x2=%7.2f\n",x1,x2);
	return 0;
}

#	接下来是python的学习 练习代码
##先是对 函数的学习  包括两种使用形式
#第一种是 
#def fun(参数)：
#表达式
#return 可有可无
第二种是 lambda 隐式表达   用于可一行表达出参数之间关系

def happy():
    print('happy birthday to you!')
def happyB(name):
    happy()
    happy()
    print('happy birthday to {}'.format(name))
    happy()
happyB('Mike')
print()
happyB('Lilly')


f=lambda x,y:x+y
print(f(10,20))

def dup(str,times=2):    #  可以int and int  int * char   no  char* char  so   int and char
    print(str*times)
dup("knock~")
dup(2,'times')
def vfunc(a,*b):    #*b  represents  variable parts   must be set in the last position. and  output in type (turple)
    print(type(b))
    for n in b:
        a += n
    return a
print(vfunc(1,2,3,4,5))


n = 1
def vfunc(a,b):
    global n
    n = b
    return a*b
s=vfunc(1,2)
print(s,n)

ls=[]
def vfunc1(a,b):
    ls=[]
    ls.append(b)
    return a*b
s=vfunc1(2,3)
print(ls,s)


#之后便是对datetime库的学习， 主要学习的是datetime.datetime()中的知识，对时间的表示 引用， 改变时间的表示格式，转化为字符串，同时使用datetime计时仍有疑惑


import time
import datetime as dt
today=dt.datetime.now()
today1=dt.datetime.utcnow()
someday=dt.datetime(2022,4,4,12,23,25,25)
print(today)
print(today1)
print(someday)
print(someday.year)
print(someday.month)
print(someday.max)
print(someday.min)
print(someday.isoformat())
print(someday.isoweekday())
print(someday.strftime('%Y-%b-%d-%a-%X'))

print('today is {0:%Y}-{0:%b}-{0:%d}-{0:%a}-{0:%X}'.format(someday))
import datetime
import datetime as dt
today = dt.datetime.now()
print(today)
a=str(today)
print(a,type(today),type(a))
print(today.strftime('%Y-%m-%d'))
print(today.strftime('%Y-%B-%d'))
print(today.strftime('%Y-%b-%d'))

#time
x=1
sum=1
today = dt.datetime.now()
start = today.strftime("%Y,%m,%d %H:%M:%S")
for i in range(1,100):
    sum += x
    x *= i
print(sum)
today1 = dt.datetime.now()
end = today1.strftime("%Y,%m,%d %H:%M:%S")
time = today1-today
print("{0:}".format(time))

![image](https://user-images.githubusercontent.com/102724466/161427771-19497a28-9e4a-4777-a6a1-fba5e183c31f.png)
## 之后考虑用图片上传每天的代码！
