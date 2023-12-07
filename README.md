1)import matplotlib.pyplot as plt
import numpy as np

def quadratic_model(time,a,b,c):
  temp=a*time**2+b*time+c
  return temp
a=0.2
b=-2
c=40
time_values=np.linspace(0,10,100)
y_values=quadratic_model(time_values,a,b,c)
plt.plot(time_values,y_values)
plt.show()

2)import matplotlib.pyplot as plt
import numpy as np

def quadratic_model(time,a,b,c):
  temp=a*time**2+b*time+c
  return temp
a=int(input("enter the value of a"))
b=int(input("enter the vaue of b"))
c=int(input("enter the value of c"))

time_values=np.linspace(0,10,100)
y_values=quadratic_model(time_values,a,b,c)
plt.plot(time_values,y_values)
plt.show()


3)import matplotlib.pyplot as plt
def quadratic_weather_model(time, a, b, c):
      temperature = a * (time ** 2) + b * time + c
      return temperature

def main():
      print("Quadratic Weather Modeling")
      print("==========================")

      try:
          with open('multi.txt', 'r') as file:
              lines = file.readlines()

          time_values = list(range(0, 11)) 
          plt.figure(figsize=(8, 6))

          for line in lines:
              coefficients = line.split()
              a, b, c = map(float, coefficients)

              temperature_values = [quadratic_weather_model(t, a, b, c) for t in time_values]

              plt.plot(time_values, temperature_values, marker='o', linestyle='-', label=f'a={a}, b={b}, c={c}')

          plt.title('Temperature Variation Over Time')
          plt.xlabel('Time')
          plt.ylabel('Temperature')
          plt.grid(True)
          plt.xlim(0, 10)
          plt.legend()
          plt.show()

      except FileNotFoundError:
          print("File not found. Please make sure 'multi.txt' exists.")

if _name_ == "_main_":
      main()

      file:single.txt
      values:



      
4)import matplotlib.pyplot as plt
def quadratic_weather_model(time, a, b, c):
      temperature = a * (time ** 2) + b * time + c
      return temperature

def main():
      print("Quadratic Weather Modeling")
      print("==========================")

      try:
          with open('multi.txt', 'r') as file:
              lines = file.readlines()

          time_values = list(range(0, 11)) 
          plt.figure(figsize=(8, 6))

          for line in lines:
              coefficients = line.split()
              a, b, c = map(float, coefficients)

              temperature_values = [quadratic_weather_model(t, a, b, c) for t in time_values]

              plt.plot(time_values, temperature_values, marker='o', linestyle='-', label=f'a={a}, b={b}, c={c}')

          plt.title('Temperature Variation Over Time')
          plt.xlabel('Time')
          plt.ylabel('Temperature')
          plt.grid(True)
          plt.xlim(0, 10)
          plt.legend()
          plt.show()

      except FileNotFoundError:
          print("File not found. Please make sure 'multi.txt' exists.")

if _name_ == "_main_":
      main()

      file:multi.txt
      values




      5)import matplotlib.pyplot as plt
import numpy as np

# Get user input for the coefficients
a = int(input("Enter the value of a: "))
b = int(input("Enter the value of b: "))
c = int(input("Enter the value of c: "))

# Generate x values
x = np.linspace(-10, 10, 400)

# Calculate y values for the first function
y1 = a*x**2 + b*x + c

# Plot the first function
plt.plot(x, y1, label=f'{a}x^2 + {b}x + {c}')

# Hard-coded coefficients for the second function
a = 1
b = -3
c = 2

# Calculate y values for the second function
y2 = a*x**2 + b*x + c

# Plot the second function
plt.plot(x, y2, label=f'{a}x^2 + {b}x + {c}')

# Add title, labels, legend, and grid
plt.title('Plot of the quadratic functions')
plt.xlabel('x')
plt.ylabel('y')
plt.legend()
plt.grid(True)

# Display the plot
plt.show()
