“冒泡”这个名字的由来是因为越大的元素会经由交换慢慢“浮”到数列的顶端，故
名。

这里以从小到大排序为例进行讲解。
基本思想及举例说明
冒泡排序的基本思想就是不断比较相邻的两个数，让较大的元素不断地往后移。经
过一轮比较，就选出最大的数；经过第2轮比较，就选出次大的数，以此类推。

下面以对 3  2  4  1 进行冒泡排序说明。

第一轮 排序过程:
3  2  4  1    （最初）;
2  3  4  2    （比较3和2，交换）;
2  3  4  1    （比较3和4，不交换）;
2  3  1  4    （比较4和1，交换）;
第一轮结束，最大的数4已经在最后面，因此第二轮排序只需要对前面三个数进行再
比较。

第二轮 排序过程:
2  3  1  4 （第一轮排序结果）;
2  3  1  4 （比较2和3，不交换）;
2  1  3  4 （比较3和1，交换;
第二轮结束，第二大的数已经排在倒数第二个位置，所以第三轮只需要比较前两个
元素。

第三轮 排序过程:
2  1  3  4  （第二轮排序结果）
1  2  3  4  （比较2和1，交换）
至此，排序结束。

算法：

#include<stdio.h>
#include<stdlib.h>
#define N 8

void bubble_sort(int a[],int n);
//一般实现
void bubble_sort(int a[],int n)//n为数组a的元素个数
{
//一定进行N-1轮比较
  for(int i=0; i<n-1; i++)
    {
        //每一轮比较前n-1-i个，即已排序好的最后i个不用比较
        for(int j=0; j<n-1-i; j++)
        {
            if(a[j] > a[j+1])
            {
                int temp = a[j];
                a[j] = a[j+1];
                a[j+1]=temp;
            }
        }
    }
}
//优化实现
void bubble_sort_better(int a[],int n)//n为数组a的元素个数
{
    //最多进行N-1轮比较
    for(int i=0; i<n-1; i++)
    {
        bool isSorted = true;
        //每一轮比较前n-1-i个，即已排序好的最后i个不用比较
        for(int j=0; j<n-1-i; j++)
        {
            if(a[j] > a[j+1])
            {
                isSorted = false;
                int temp = a[j];
                a[j] = a[j+1];
                a[j+1]=temp;
            }
        }
        if(isSorted) break; //如果没有发生交换，说明数组已经排序好了
    }
}
int  main()
{
    int num[N] = {89, 38, 11, 78, 96, 44, 19, 25};
    bubble_sort(num, N); //或者使用bubble_sort_better(num, N);
    for(int i=0; i<N; i++)
        printf("%d  ", num[i]);
    printf("\n");
    system("pause");
    return 0;
}
