def calculate_discount(price, discount_percent):
    # Check if the discount is 20% or higher
    if discount_percent >= 20:
        # Calculate the discount amount
        discount_amount = (discount_percent / 100) * price
        # Calculate the final price after applying the discount
        final_price = price - discount_amount
        return final_price
    else:
        # Return the original price if the discount is less than 20%
        return price

def main():
    # Prompt the user to enter the original price and discount percentage
    original_price = float(input("Enter the original price: "))
    discount_percentage = float(input("Enter the discount percentage: "))

    # Calculate the final price using the calculate_discount function
    final_price = calculate_discount(original_price, discount_percentage)

    # Print the final price
    if final_price == original_price:
        print("No discount applied. The price remains: ", final_price)
    else:
        print("The final price after applying the discount is: ", final_price)

if __name__ == "__main__":
    main()
