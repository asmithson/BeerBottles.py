# BeerBottles.py
# beer bottles song program
def countdown_bottles(num_bottles):
    """
    Function to manage the countdown of bottles and print the lyrics.
    """
    while num_bottles > 1:
        print(f"{num_bottles" bottles of beer on the wall, {num_bottles} of beer.")
        num_bottles -=1
        print(f"Take one down and pass it around, {num_bottles} bottles of beer on the wall.\n")

    # Special case for one bottle
    if num_bottles ==1:
        print("1 bottle of beer on the wall, 1 bottle of beer.")
        print("Take it down and pass it around, no more bottles of beer on the wall.\n)
    elif num_bottles == 0:
        print("No more bottles of beer on the wall, no more bottles of beer.")
        print("Go to the store and buy some more, 99 bottles of beer on the wall!\n")

def main():
    """
    Main function to handle user input and execute the countdown.
    """ 
    # Start
    print("Welcome to the 'Bottles of Beer' countdown program!")

    # Ask user for the number of bottles
    while True:
        try:
            user_input = int(input("How many bottles of beer are on the wall? "))
            if user_input < 0:
                print("Please enter a number greater than or equal to 0.")
                continue
            break
        except ValueError:
            print("Invalid input! Please enter a whole number.")
    # Pass number of bottles to the function
    countdown_bottles(user_input)

    # End
    print("Thanks for using the 'Bottles of Beer' program!")
if__name__ == "__main__":
    main()
