# Coffee.java-168-
Given values such as tax rate, price, and flavor of a particular coffee, this code produces the ultimate price of the coffee
package edu.ilstu.labquiz1;

public class Coffee
{
	private String flavor;
	private double priceOfCoffee;
	private static final double SALES_TAX_RATE = 0.1078;
	
	public String getFlavor() 
	{
		return flavor;
	}
	
	public void setFlavor(String flavor) 
	{
		this.flavor = flavor;
	}
	
	public double getPriceOfCoffee() 
	{
		return priceOfCoffee;
	}
	
	public void setPriceOfCoffee(double priceOfCoffee)
	{
		this.priceOfCoffee = priceOfCoffee;
	}
	
	/**
	 * This method updates the price of coffee by the rate increased passed in
	 * 
	 * @param rateIncrease rate the price of coffee will increase
	 */
	public void increasePrice(double rateIncrease)
	{
		priceOfCoffee += priceOfCoffee * rateIncrease;
	}
	
	/**
	 * This method calculates the cost of buying coffee by adding the cost of the order
	 * to the tax amount.
	 * 
	 * @param numberOfCups number of cups ordered
	 * @return the cost of the number of coffees ordered
	 */
	public double calculateCost(int numberOfCups)
	{
		return numberOfCups*priceOfCoffee*(SALES_TAX_RATE)+ (priceOfCoffee);
	}
}
