# OOP
Object Oriented Programming
import java.util.Scanner;

public class Testing {

	public static void main(String[] args) {
		printFeverLimits();
		
		Scanner in = new Scanner(System.in);
		
		String subject;
		int temperature;
		
		System.out.println("Subject (human, dog, horse)");
		subject = in.nextLine();
		
		System.out.println("Temperature?");
		temperature = Integer.parseInt(in.nextLine());
		
		if (hasFever(subject, temperature)==true)
		{
			System.out.println("Subject has fever");
		}
		else 
		{	
			System.out.println("Subject has no fever");
		}
		

	} // End of the Main
	
	public static void printFeverLimits()
	{
		System.out.println("Fever Limits");
		System.out.println("- human 37c\n- dog 39c\n- horse 38c");
	}
	
	public static boolean hasFever(String subject, int temperature)
	{
		
		boolean hasFever=false;
		
		if (subject.equals("human") && temperature > 37)
		{
			hasFever=true;
		}
		
		if (subject.equals("dog") && temperature > 39)
		{
			hasFever=true;
		}
		
		if (subject.equals("horse") && temperature > 38)
		{
			hasFever=true;
		}
		
		return hasFever;
	}
	
}