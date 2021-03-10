# hello-world

    import java.util.*;
public class MiniProject1 
{
	public static void main(String[] args) 
	{
		Scanner sc=new Scanner(System.in);
			
		//Inputting a large number as a string
		
		System.out.println("Enter a large number :");
		String num=sc.nextLine();
		
		// Initialization of variables
		
		String re_num=num;
		int l=num.length();
		String st="", st2, str="";
		long n=0L;
		char temp;
		
	   //Calculation of unique digits Starts here
       //It extracts the unique numerical values in string st 
		             
		             for(int i=0; i<l; i++) 
		             {
                         if(num.charAt(i) != '*') 
                        {
						  st+=num.charAt(i) + ",";
						  str+=num.charAt(i);
						  num=num.replace(num.charAt(i), '*');
					    }
					 }
		             
      //Printing of Unique digits with proper punctuation
		             
		StringBuffer st1=new StringBuffer(str);
		st=st.substring(0, st.length()-1)+".";
		System.out.println("The unique digits present in "+re_num+" are " +st);
		
	  //Calculating the largest number
		
		for(int i=0; i<st1.length(); i++) {
			for(int j=i; j<st1.length(); j++) {
				if(st1.charAt(j)>st1.charAt(i)) {
				temp=st1.charAt(i);
				st1.setCharAt(i,st1.charAt(j));
				st1.setCharAt(j,temp);
				}
			}
		}
		
     //Printing the largest Number
		
		st2=st1.toString();
		n =Long.parseLong(st2);
		System.out.println("The largest number possible out of these unique digits is "+n);
 sc.close();
	   } 
	}


