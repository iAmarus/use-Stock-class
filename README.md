import java.util.*;

public class Test {

	public static void main(String[] args) {
		//variables
		Scanner input = new Scanner(System.in);
		Random dice = new Random();
		int random = dice.nextInt(100);
		String name;
		String symbol;
		double previousClosingPrice;
		double currentPrice;
		
		Stock stock = new Stock();
		//ask a user to enter stock name
		System.out.println("Enter Stock name: " );
		 name = input.nextLine();
		//ask a user to enter stock symbol
		System.out.println("Enter Stock symbol : ");
		symbol = input.next();
		//ask a user to enter previous closing price
		System.out.println("Enter the previous closing price : ");
		previousClosingPrice = input.nextDouble();
		//ask a user to enter current price
		System.out.println("Enter the current price : ");
		currentPrice = input.nextDouble();
		
		System.out.println("Stock name : " + stock.getName(name));
		System.out.println("Stock symbol : " + stock.getSymbol(symbol));
		System.out.println("Stock ID : " + random);
		
		stock.previousClosingPrice = previousClosingPrice;
		stock.currentPrice = currentPrice;
		System.out.printf("Price-change percentage: %.2f%%\n", 
			stock.getChangePercent());
		
	}
}
