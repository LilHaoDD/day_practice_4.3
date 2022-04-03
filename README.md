# day_practice_4.3
daily_practice_4.3
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
