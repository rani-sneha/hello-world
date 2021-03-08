# hello-world
import java.util.*;
public class MiniProject1 {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter a large numer :");
		String num=sc.nextLine();
		int l=num.length();
		String st="", nums, st2;
		int n;
		char temp;
				for(int i=0; i<l; i++) {
		
						if(num.charAt(i) != '*') {
						st+=num.charAt(i) + ",";
							num=num.replace(num.charAt(i), '*');
						}
					}
		StringBuffer st1=new StringBuffer(st);
		st1.setCharAt(l-1, '.');
		System.out.println("The unique digits present in "+num+" are " +st1);
		for(int i=0; i<st1.length(); i++) {
			for(int j=0; j<st1.length(); j++) {
				temp=st1.charAt(i);
				st1.setCharAt(i,st1.charAt(j));
				st1.setCharAt(j,temp);
			}
		}
		st2=st1.toString();
		n =Integer.parseInt(st2);
		System.out.println("The largest number possible out of these unique digits is "+n);
	}

}
