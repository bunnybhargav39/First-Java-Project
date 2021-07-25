# First-Java-Miniproject
Scenario: You are an IT support Administartor Specialist and are charged with the task of creating email account for new hires.





/*You are an IT support Administrator Specialist and are charaged with the task of creating email account for new hires.*/


import java.util.Scanner;

public class Email
{

	public static void main(String[] args) 
	{
		String r=null;
		String s=null;
		String s1="@xxxxxxxcompany.com";
		Scanner sc=new Scanner(System.in);
		System.out.println("enter firstname :");
		String fn=sc.nextLine();
		System.out.println("enter last name:");
		String ln=sc.nextLine();
		System.out.println("email created: \n" +fn+ln+"@gmail.com");
		System.out.println("DEPARTMENT CODES \n 1.Sales \n 2.development \n 3.Accounting \n 0.none \n");
		System.out.println("enter department code:");
		int code=sc.nextInt();
		if(code==1)
		{
			System.out.println("DEPARTMENT MAIL: "+fn+ln+"sales"+"@gmail.com");
			r=fn+ln;
			s="sales";
			
		}
		else if(code==2)
		{
			System.out.println("DEPARTMENT MAIL: "+fn+ln+"dev"+"@gmail.com");
			r=fn+ln;
			s="dev";
		}
		else if(code==3)
		{
			System.out.println("DEPARTMENT MAIL: "+fn+ln+"acc"+"@gmail.com");
			r=fn+ln;
			s="acc";
		}
		else
		{
			System.out.println("DEPARTMENT MAIL: "+fn+ln+"@gmail.com");
			r=fn+ln;
			s="";
		}
		
			int length=8;
		String passwordset="abcdefghijklmnopqrstuvwxyz0123456789!@#$%";
		char[] password =new char[length];
		for(int i=0;i<length;i++)
		{
			int rand=(int)(Math.random()*passwordset.length());
			password[i]=passwordset.charAt(rand);
		}
		System.out.println("PASSWORD GENERATED :"+password);
		System.out.println("COMPANY EmailSsL:"+r+s+s1 );
		sc.close();
	}

}
