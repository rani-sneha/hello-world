# hello-world

import java.util.*;
public class MiniProject1 {

      public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter a large numer :");
		String num=sc.nextLine();
		int l=num.length();
		String st="", num2, str="", st2;
		int num3;
		char temp;
		StringBuffer num1= new StringBuffer(num);
				for(int i=0; i<l; i++) {
					for(int j=0; j<l; j++) {
						if(num.charAt(i)==num.charAt(j) && i!=j) 
							num1.setCharAt(j, '*');
						}
					}
		num2=num1.toString();
		for(int i=0; i<l;i++) {
			if(num2.charAt(i)!='*') {
				str+=num2.charAt(i)+ ",";
				st+=num2.charAt(i);
			}
				}
		StringBuffer str1 =new StringBuffer(str);
		str1.setCharAt(l-1, '.');
		System.out.println("The unique digits present in "+num+" are " +str1);
		StringBuffer st1=new StringBuffer(st);
		for(int i=0; i<st1.length(); i++) {
			for(int j=0; j<st1.length(); j++) {
				temp=st1.charAt(i);
				st1.setCharAt(i,st1.charAt(j));
				st1.setCharAt(j,temp);
			}
		}
		st2=st1.toString();
		num3=Integer.parseInt(st2);
		System.out.println("The largest number possible out of these unique digits is "+num3);
	}

}
