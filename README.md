# C-1
在一个有序数组中查找具体的某个数字n
折半查找法
#define _CRT_SECURE_NO_WARNINGS 1
#include <stdio.h>
int main()
{
int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
int left = 0;
int right = sizeof(arr)/sizeof(arr[0])-1;
int k = 7;
int mid = 0;
while (left <= right)
{
mid = (right - left) / 2 + left;
if (arr[mid] < k)
{
left = mid + 1;
}
else
if (arr[mid]>k)
{
right = right - 1;
}
else
break;
}
if (left <= right)
printf(“找到了，下标是%d\n”, mid);
else
printf(“找不到\n”);
system(“pause”);
}
