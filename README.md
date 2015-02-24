# hello-world
first repository
#include<stdlib.h>
long long int ans(int n,int max){
int i;long long int res=1;
for(i=1;i<=n;i++){ 
res=(res*i)%max;
} 
return res; 
} 
int main(void) {
int t,n,k,*arr,i,max;
scanf("%d",&t);
while(t){
t--;
scanf("%d%d",&n,&k);
arr=(int*)malloc(k*sizeof(int));
for(i=0;i<k;i++){
scanf("%d",&arr[i]);
if(arr[i]>max)
max=arr[i];
}
printf("%lld\n",ans(n,max));
free(arr);
}
return 0;
}
