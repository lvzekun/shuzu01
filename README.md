# shuzu01
package shuzu01;

import java.util.Scanner;
import java.lang.*;
public class Test {
	
	private static boolean flase;





	@SuppressWarnings("unused")
	public  static void main(String arg[])
	{
		int i,j=0;
		Scanner input =new Scanner(System.in);
		System.out.println("请输入一个数组的长度");
		int length=input.nextInt();
	 int []arry=new int[length];
		//判断数组输入整数
		System.out.println("请输入一个数组");
		for(i=0;i<length;i++ )
		{
			int a=input.nextInt();
			isNumeric(a);
			if(false)
				{
				  System.out.println("请输入一个整数");
				int s=input.nextInt();
				   
				  arry[i]=s;
				}
			arry[i]=a;
			j++;
		}
		if(j>length)
		{
			System.out.println("输入整数超额");
		}
		 int Maxsum=0,max,num=1,count=0;
		int sum=0;
		//Maxsum是子数组和最值，max是整数最值
		 //sum是子数组和，coun他表示复数个数
		 
		 for(i=0;i<length;i++)
		 {
			 if(sum<0)
			 {
				 sum=arry[i];
			 }
			 else
			 {
				 sum+=arry[i];
			 }
			 if(Maxsum<sum)
			 {
				 Maxsum=sum;
			 }
		 }
		//最大元素数组中
		 max=arry[0];
		 //数组全是负数
		 for(i=0;i<length;i++)
		 {
			 if(arry[i]<0)
			 {
				 count++;
			 }
			 if(arry[i]>0)
			 {
				 max=arry[i];
			 }
			 if(count==length)
			 {
				 Maxsum=max;
			 }
		 }
			
		 System.out.println("子数组最大值"+Maxsum);
				
		
		
		
		//输出数组
		for(i=0;i<length;i++ )
		{
			System.out.println(arry[i]);
		}
	
	}




//判断函数
	public static boolean isNumeric(int a)
	{
		     if (!Character.isDigit(a))
		      {	   
			     return false;
		      }
		  
		  
		   return true;
		 }

}
