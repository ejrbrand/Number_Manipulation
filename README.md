
public class Number_Manipulation {

	public static int reverseNumber(int n)
	{
		int reverse = 0;
		while(n != 0)
		{
			reverse = (reverse * 10) + (n % 10);
			n /= 10;
		}
		return reverse;
	}
	
	public static int decimalToBinary(int n)
	{
		int binary[] = new int[32];
		int i = 0;
		while(n> 0)
		{
			binary[i++] = n % 2;
			n /= 2;
		}
		
		String answer = "";
		for(int j = i - 1; j >= 0; j--)
		{
			answer += binary[j];
		}
		return Integer.parseInt(answer);
	}
	
	public static int binaryToDecimal(int n)
	{
		String binary = Integer.toString(n);
		return Integer.parseInt(binary, 2);
	}
	
	public static String decimalToHex(int n )
	{
		int remainder;
		String output = "";
		
		char hex[] = {'0', '1', '2', '3', '4', '5', '6', '7', '8', '9', 'A', 'B', 'C', 'D', 'E', 'F'};
		
		while(n > 0)
		{
			remainder = n % 16;
			output += hex[remainder];
			n /= 16;
		}
		return output;
	}

	
	public static void main(String[] args) {
		System.out.println("Reversing the number 567: " + reverseNumber(567));
		System.out.println("Decimal to binary conversion: " + decimalToBinary(45));
		System.out.println("Binary to decimal conversion: " + binaryToDecimal(1111));
		
		System.out.println("Decimal to hexadecimal conversion: " + decimalToHex(3456));
		
	}
}
