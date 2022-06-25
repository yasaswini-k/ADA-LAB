#include <stdio.h>
#include<time.h>
int main()
{
int a[100], n, i, j, position, swap;
time_t start,end;
printf("Enter number of elements");
scanf("%d", &n);
printf("Enter %d Numbers", n);
for (i = 0; i < n; i++)
scanf("%d", &a[i]);
start=time(NULL);
for(i = 0; i < n - 1; i++)
{
position=i;
for(j = i + 1; j < n; j++)
{
if(a[position] > a[j])
position=j;
}
if(position != i)
{
swap=a[i];
a[i]=a[position];
a[position]=swap;
}
}
end=time(NULL);
printf("Sorted Array:");
for(i = 0; i < n; i++)
printf("%d", a[i]);

   printf("Time is %fs",difftime(end,start));
return 0;
}
