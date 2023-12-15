# Function3
def calculate_miles_per_gallon(miles, gallons):
    if gallons == 0:
        return 0.0
    else:
        return miles / gallons

def main():
    trip_count = 0

    try:
        while True:
            # User input for trip information
            destination_city = input("Enter destination city (Ctrl+Z to stop): ")
            miles = float(input("Enter miles traveled: "))
            gallons = float(input("Enter gallons used: "))

            # Calculate miles per gallon
            mpg = calculate_miles_per_gallon(miles, gallons)

            # Display trip information
            print(f"Destination City: {destination_city}, Miles: {miles}, MPG: {mpg:.2f}")

            # Increment trip count
            trip_count += 1

    except EOFError:
        # Display the number of trips made
        print(f"\nNumber of Trips Made: {trip_count}")

if __name__ == "__main__":
    main()
