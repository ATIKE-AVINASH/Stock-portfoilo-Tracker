# Stock-portfoilo-Tracker
stock_prices = {
"AAPL": 180,
"TSLA": 250,
"GOOGL": 140,
"MSFT": 330,
"AMZN": 135
}

total_amount = 0

print("Available Stocks:")
for stock in stock_prices:
print(stock, "- $", stock_prices[stock])

n = int(input("\nHow many different stocks do you want to enter? "))

file = open("portfolio.txt", "w")
file.write("Stock Portfolio\n")
file.write("-------------------------\n")

for i in range(n):
stock_name = input("\nEnter Stock Name: ").upper()

if stock_name in stock_prices:  
    quantity = int(input("Enter Quantity: "))  

    price = stock_prices[stock_name]  
    investment = price * quantity  

    total_amount = total_amount + investment  

    print("Investment in", stock_name, "= $", investment)  

    file.write(f"{stock_name}  Quantity: {quantity}  Price: ${price}  Total: ${investment}\n")  

else:  
    print("Stock not available.")

file.write("-------------------------\n")
file.write(f"Total Investment = ${total_amount}")

file.close()

print("\nTotal Investment Value = $", total_amount)
print("Portfolio saved successfully in portfolio.txt")

Same code, Change from $ symbol to rupee symbol and change the stock names to india top companies
