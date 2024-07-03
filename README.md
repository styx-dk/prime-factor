#include <stdio.h>
int main() {
	int ar[20],i,j,k,n,f[100],fact=1,temp;
   printf("enter no of elements:");
   scanf("%d",&n);
   printf("enter the array");
   for(i=0;i<n;i++){
	scanf("%d",&ar[i]);
   }
   for(k=0;k<n;k++){
   i=ar[k];
   	for(j=2;j<=i/2;j++){
       	if(i%j==0){
           	fact++;
       	}
   	}
     	printf("\n%d",fact);

   f[i]=fact;
 fact=1;
   }
	for(k=0;k<n-1;k++){
    	for(i=k+1;i<n;i++){
    	if(f[ar[k]]>f[ar[i]]){
        	temp=ar[k];
        	ar[k]=ar[i];
        	ar[i]=temp;
    	}
    	}
	}
	printf("\nsorted array: \n");
	for(i=0;i<n;i++){
    	printf("%d\t",ar[i]);
	}
	return 0;
}
