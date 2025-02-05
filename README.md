#include<stdio.h>
int main()
{
    int n,m;
    printf("enter the no of rows and col:");
    scanf("%d %d",&n,&m);
    int mat[n][m];
    printf("enter the matrix vallues: \n");
    for(int i=0;i<n;i++){
        for(int j=0;j<m;j++){
            scanf("%d",&mat[i][j]);
        }
    }
    int left=0,top=0,right=m-1,bottom=n-1;
    while(left<=right && top<=bottom){
       for(int i=left;i<=right;i++){
        printf("%d ",mat[top][i]);
       }
       top++;
       for(int i=top;i<=bottom;i++){
        printf("%d ",mat[i][right]);
       }
       right--;
       if(top<=bottom){
        for(int i=right;i>=left;i--){
            printf("%d ", mat[bottom][i]);
            }
            bottom--;
       }
       if(left<=right){
        for(int i=bottom;i>=top;i--){
            printf("%d ",mat[i][left]);
        }
        left++;
       }
    }

    return 0;
}
