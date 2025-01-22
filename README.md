![components on breadboard 1](https://github.com/user-attachments/assets/5d1ede47-da76-4232-8688-e5806aea86a7)


https://github.com/user-attachments/assets/ad7c3026-5107-43ad-ad03-d96fab2edc1f

# height-and-distance
Python (Programming Language), Math functions (for trigonometric calculations), Mathematical Formulas (Trigonometry, Pythagorean theorem), Arduino, Raspberry Pi, Sensors, Electronics, Problem Solving.
Design a device that uses the Pythagorean theorem and basic trigonometry to accurately measure the height and distance of object in real- world applications.
 Measured horizontal distance and angle of elevation to calculate the height or distance of objects.
 Applied trigonometric functions such as tangent and Pythagorean theorem to compute accurate measurements.
 Utilized Arduino for automated calculations and results display.
 Integrated hardware components such as inclinometer/protractor for angle measurement and a tape measure or laser rangefinder for distance measurement.
Implemented a user-friendly interface with real-time result display.
import math

# Function to calculate height
def calculate_height(distance, hypotenuse):
    height = math.sqrt(hypotenuse**2 - distance**2)
    return height

# Function to calculate distance
def calculate_distance(height, hypotenuse):
    distance = math.sqrt(hypotenuse**2 - height**2)
    return distance

# Main program
def main():
    choice = input("Do you want to calculate height (h) or distance (d)? ").lower()
    
    if choice == 'h':
        distance = float(input("Enter the distance from the object: "))
        hypotenuse = float(input("Enter the length of the hypotenuse: "))
        height = calculate_height(distance, hypotenuse)
        print(f"The height of the object is {height} units.")
    
    elif choice == 'd':
        height = float(input("Enter the height of the object: "))
        hypotenuse = float(input("Enter the length of the hypotenuse: "))
        distance = calculate_distance(height, hypotenuse)
        print(f"The distance from the object is {distance} units.")
    
    else:
        print("Invalid choice. Please choose 'h' for height or 'd' for distance.")

if __name__ == "__main__":
    main()
