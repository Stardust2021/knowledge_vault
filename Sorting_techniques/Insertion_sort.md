#include<stdio.h>
void Insertion (int A[],int n)
{
    int i,j,x;
    for(i=1;i<n;i++)
    {
        j=i-1;
        x=A[i];
        while(j>-1 && A[j]>x)          //refer youtube videos
        {
            A[j+1]=A[j];
            j--;
        }
        A[j+1]=x;
    }
}
int main()
{
    int A[]={10,8,9,7,1,3,56,8,77},n=10,i;
    Insertion(A,n);
    for(int i=0;i<10;i++)
    printf("%d ",A[i]);
}