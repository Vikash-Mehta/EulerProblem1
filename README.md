EulerProblem1
=============
import java.text.*;

public class Problem1{

public static int sum(int t){
    int i=1, sum=0;
	
	do{
		sum=sum+i;
		i++;

	  }while(i<=t);
 
    return(sum);
}

public static int multiples(int m, int n)
{
   int i=n/m ;

   return(m*sum(i));

}

public static int gcd(int a, int b)
{	
   if(a>b){

	while(b>0)
       {
	 int temp=b;
	  b=a%b;
         a=temp;
       }return(a);
   }

else{
	while(a>0)
       {	 
	int temp=a;
	a=b%a;
        b=temp;
       }return(b);
     }
}



public static int lcm(int a, int b)	
{
	int lcm;

	lcm=(a*b)/gcd(a,b);

	return(lcm);
}

public static void main(String[] args)
{
	int a=3, b=5, n=999;
	int sum;
	
	sum=multiples(a,n)+multiples(b,n)-multiples(lcm(a,b),n);
	
	System.out.println(+sum) ;
}

}

