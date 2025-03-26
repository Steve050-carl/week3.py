
def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount.
    If the discount is 20% or higher, apply the discount; otherwise, return the original price.
    """
    if discount_percent >= 20:
        return price - (price * (discount_percent / 100))
    return price

# Prompt user for input
try:
    price = float(input("Enter the original price: "))
    discount_percent = float(input("Enter the discount percentage: "))
    
    # Calculate final price
    final_price = calculate_discount(price, discount_percent)
    
    # Print the result
    print(f"Final price after discount: ${final_price:.2f}")
except ValueError:
    print("Please enter valid numerical values.")
