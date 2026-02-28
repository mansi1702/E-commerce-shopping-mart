# E-commerce-shopping-mart
# E-Commerce Shopping Mart

print("Welcome to E-Commerce Shopping Mart")

products = {
    1: {"name": "Laptop", "price": 55000},
    2: {"name": "Mobile Phone", "price": 25000},
    3: {"name": "Headphones", "price": 2000},
    4: {"name": "Smart Watch", "price": 3500},
    5: {"name": "Keyboard", "price": 1500}
}

cart_total = 0

print("\nAvailable Products:")
print("----------------------")
for key, value in products.items():
    print(f"{key}. {value['name']} - Rs.{value['price']}")

while True:
    choice = int(input("\nEnter product number to buy (0 to checkout): "))
    
    if choice == 0:
        break
    elif choice in products:
        quantity = int(input("Enter quantity: "))
        price = products[choice]["price"]
        total_price = price * quantity
        cart_total += total_price
        print(f"Added to cart: {products[choice]['name']} x {quantity}")
    else:
        print("Invalid product choice!")

print("\nCheckout Summary")
print("----------------------")
print(f"Total Amount Payable: Rs.{cart_total}")
print("Thank you for shopping with us!")
