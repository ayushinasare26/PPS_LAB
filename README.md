1. Write a program to calculate the area of a circle and print the result as shown in the displayed test cases.
radius = int(input('Enter the radius : '))
PI = 3.14
Area = PI * radius * radius;
if(radius<0):
	print("Enter a positive value upto 100")
else:
	print("Area of circle = %f"%Area)


2. You are given a length L and breadth B and your task is to find the Area of the Rectangle.
L=int(input("L:"))
B=int(input("B:"))
Area = L * B
print(f'{Area}')


3. You are given a side S and your task is to find the Area of the square
S=int(input("S:")) # Make use of the value of S read using the input function.
Area = S**2
print(f'{Area}')


4. Write a Python program to print the area of a triangle.
Base = float(input('Base: '))
Height = float(input('Height: '))
Area = "{:.2f}".format(0.5 * Base * Height)
print("Area:",Area)


5. Write a Python program to find the roots of a quadratic equation by taking the coefficients from the user.
import math
import cmath
a = float(input('a: '))
b = float(input('b: '))
c = float(input('c: '))
x = b**2 - 4*a*c
if(x>0):
	root1 = (-b+math.sqrt(x))/(2*a)
	root2 = (-b-math.sqrt(x))/(2*a)
	print(f'The roots are: {root1:.2f} and {root2:.2f}')
elif x == 0:
	root = -b/(2*a)
	print(f'The root is: {root:.2f}')
else:
	real_part=-abs(b/(2*a))
	img_part=(cmath.sqrt(abs(x))/(2*a)).real
	print(f'The roots are: {real_part:.2f}{img_part:+.2f}j and {real_part:.2f}{-img_part:+.2f}j')


6. Write a Python program to find the largest of three numbers.
a = float(input('Enter the first number: '))
b = float(input('Enter the second number: '))
c = float(input('Enter the third number: '))
if(a>=b) & (a>=c):
	largest=a
elif(b>=a) & (b>=c):
	largest=b
else:
	largest=c
print('Largest number:',largest)


7. Write a program to read temperature in Celsius and print the temperature in fahrenheit.
C = float(input("celsius: "))
F = 1.8 * C + 32.0
print(f'fahrenheit: {F}')


8. Write a Python program to perform union, intersection and difference operations on Set A and Set B.
a = list(map(int,input("Set A: ").split()))
A = set(a)
b = list(map(int,input("Set B: ").split()))
B = set(b)
union_set = A.union(B)
intersection_set = A.intersection(B)
difference_set = A.difference(B)
print(f'Union:  {union_set}')
print(f'Intersection:  {intersection_set}')
print(f'Difference:  {difference_set}')


9. Write a Python program to check if a given year is a leap year or not.
year = int(input('Enter a year: '))
if(year%4==0 and year%100!=0) or (year%400==0):
	print(f'{year} is a leap year')
else:
	print(f'{year} is not a leap year')


10. Write a Python program to calculate the average marks for 5 subjects. The program should prompt the user to input the marks for each subject. After receiving the input, it should compute the average marks and then determine the corresponding grade based on the following grading system:
A: 90 - 100
B: 80 - 89
C: 70 - 79
D: 60 - 69
F: Below 60
a = float(input('subject 1: '))
b = float(input('subject 2: '))
c = float(input('subject 3: '))
d = float(input('subject 4: '))
e = float(input('subject 5: '))
average = (a+b+c+d+e)/5.0
print('Average Marks: %.2f'%average)
if(average>=90  and average<=100):
	print('Grade: A')
elif(average>=80 and average<= 89):
	print('Grade: B')
elif(average>=70 and average<=79):
	print('Grade: C')
elif(average>=60 and average<=69):
	print('Grade: D')
else:
	print('Grade: F')


11. Write a Python program that prompts the user to input a date (year, month, and day) and checks if it is a valid date. If the entered date is valid, the program should increment the date by one day and display the incremented date. The program should take into account leap years when determining the number of days in February.
year = int(input('year: '))
m = int(input('month: '))
d = int(input('day: '))
leap = (year % 4 == 0 and year %100 != 0) or (year % 400 == 0)
month_days = [31,28+leap,31,30,31,30,31,31,30,31,30,31]
if m<1 or m>12 or d<1 or d>month_days[m-1]:
	print("invalid")
else:
	print("valid")
	d+=1
	if d>month_days[m-1]:
		d = 1
		m+=1
		if m>12:
			m = 1
			year += 1
	print(f"incremented date: {year}-{m:02d}-{d:02d}")


12. Write a python program to print factorial of given number.
def factorial(n):
	if n==0 or n==1:
		return 1
	else:
		return n * factorial(n-1)
num = int(input("Enter a number : "))
if num<0:
	print("Enter a positive number")
else:
	print(f"Factorial of given number is : {factorial(num)}")


13. Write a Python program to print the following pattern.
def inverted_star_pattern(n):
	for i in range(n, 0, -1):
		print('* '*i)
rows = int(input("Enter a number : "))
inverted_star_pattern(rows)


14. Write a Python program that prompts the user to input three digits (0-9) and checks if the entered digits are valid. If the digits are valid, the program generates all possible combinations of these three digits and prints them. Each combination is formed by arranging the digits in different orders. If the input is not valid (digits are not between 0 and 9), the program should display as "Invalid".
digit1 = int(input("digit1 (0-9): "))
digit2 = int(input("digit2 (0-9): "))
digit3 = int(input("digit3 (0-9): "))
if(0<=digit1<=9 and 0<=digit2<=9 and 0<=digit3<=9):
	digits =[digit1,digit2,digit3]
	print(f"{digits[0]}{digits[1]}{digits[2]}")
	print(f"{digits[0]}{digits[2]}{digits[1]}")
	print(f"{digits[1]}{digits[0]}{digits[2]}")
	print(f"{digits[1]}{digits[2]}{digits[0]}")
	print(f"{digits[2]}{digits[0]}{digits[1]}")
	print(f"{digits[2]}{digits[1]}{digits[0]}")
else:
	print("Invalid")


15. Write a Python program to perform multiplication of two matrices.
def matmult(A, B):
	rowsA,rowsB=len(A),len(B)
	colsA,colsB=len(A[0]),len(B[0])
	if(colsA!=rowsB):
		print("Cannot multiply the two matrices. Incorrect dimensions.")
		return None
	result = []
	for i in range(rowsA):
		row =[]
		for j in range(colsB):
			row.append(0)
		result.append(row)
	for i in range(rowsA):
		for j in range(colsB):
			for k in range(colsA):
				result[i][j]+=A[i][k]*B[k][j]
	return result
def readmatrix(name = ''):
	matrix=[]
	row=[]
	print(f"Enter values for {name}")
	m=int(input("Number of rows, m = "))
	n=int(input("Number of columns, n = "))
	for i in range(m):
		row=[]
		for j in range(n):
			row.append(int(input(f"Entry in row: {i+1} column: {j+1}\n")))
		matrix.append(row)
		row=[]
	return matrix
matrixa = readmatrix('matrix - A')
matrixb = readmatrix('matrix - B')
print("Matrix - A =", matrixa)
print("Matrix - B =", matrixb)
print("Matrix - A * Matrix- B =", matmult(matrixa, matrixb))


16. Write a Python program that prints prime numbers less than n which represents the upper limit.
n = int(input('Enter upper limit: '))
for num in range(2,n):
	for i in range(2, num):
		if num %i == 0:
			break
	else:
		print(num)


17. Write a program to count the number of vowels using sets in a given string.
def vowel_count(str):
	count = 0
	vowel = set("aeiouAEIOU")
	for char in str:
		if char in vowel:
			count+=1
	return count
str = input()
vowel_count(str)
print(vowel_count(str))


18. Write a Python program to find whether a given string is a palindrome or not.
str = str(input())
if str == str[::-1]:
	print("palindrome")
else:
	print("not a palindrome")


19. Write a Python program that takes a sentence as input, removes punctuations from the sentence, and displays the modified sentence.
s = input("")
m_s=""
for char in s:
	if char.isalnum() or char.isspace():
		m_s+=char
print(m_s)


20. Write a Python program to find the reverse of a string.
str = input()
print(str[::-1])


21. Write a program to print the sum of digits of a number.
def numsum(num):
	sum = 0
	while (num != 0):
		sum += (num % 10)
		num = num // 10
	return sum
num = int(input("num: "))
ans = numsum(num)
print("sum: %d" % ans)


22. Take an integer n from the user. Your task is to Write a program to find out the sum of the digits of the given number using the process of recursion. Print the result as shown in the Test cases. 
The program defines the Sumof() function.
In the main program it takes the input n and sends it to the Sumof() function.
The Sumof() function contains base and recursive criterion.
def Sumof(n):
	if n<10:
		return n
	return(n%10)+Sumof(n//10)
n = int(input())
print(Sumof(n))


23. Write a Python program that functions as a simple phone book manager with a menu-driven interface. The program prompts the user to choose from the following options:
Add Contact
Remove Contact
Display
Quit
phone_book={}
while True:
	print("1. Add Contact")
	print("2. Remove Contact")
	print("3. Display")
	print("4. Quit")
	choice= input("Enter choice (1-4): ")
	if choice=='1':
		name= input("Name: ")
		number = input("Phone number: ")
		phone_book[name]=number
	elif choice == '2':
		name = input("Name: ")
		if name in phone_book:
			del phone_book[name]
		else:
			print("Not found")
	elif choice == '3':
		if phone_book:
			print(phone_book)
		else:
			print("{}")
	elif choice =='4':
		break
	else:
		print("Invalid")


24. Write a python program to define a module to find Fibonacci Numbers and import the module to another program.
import fibonacci_module
def main():
	try:
		n=int(input("Enter the max value: "))
		if n>0:
			fib_series=fibonacci_module.generate_fibonacci_sequence(n)
			print(f"Fibonacci series upto {n} :")
			print(" ".join(map(str,fib_series)),end=" ")
		else:
			print("Please enter a positive integer")
	except ValueError:
		print("invalid input! Please enter a valid integer.")
if __name__ == "__main__":
	main()


25. Implement a Python program using a class named Complex to perform operations on complex numbers. The class has the following methods:
initComplex(): A method that takes user input for the real and imaginary parts to initialize a complex number.
display(): A method that displays the complex number in the form "a + bi".
sum(): A method that computes the sum of two complex numbers and stores the result in the current instance.
The program creates three instances of the Complex class, initializes two complex numbers, displays them, computes their sum, and displays the result.
class Complex ():
	def __init__(self):
		self.real=0
		self.imaginary=0

	def initComplex(self):
		self.real=int(input("Real Part: "))
		self.imaginary=int(input("Imaginary Part: "))

	def display(self):
		if self.imaginary>=0:
			print(f"{self.real}+{self.imaginary}i")
		else:
			print(f"{self.real}{self.imaginary}i")

	def sum(self,c1,c2):
		self.real = c1.real+c2.real
		self.imaginary = c1.imaginary+c2.imaginary
c1 = Complex()
c2 = Complex()
c3 = Complex()
print("complex number 1")
c1.initComplex()
c1.display()
print("complex number 2")
c2.initComplex()
c2.display()
print("Sum:",end=" ")
c3.sum(c1,c2)
c3.display()


26. Follow the instructions to create a Python program modeling cars with specific types: Car1 and Car2. Begin by defining a base class Car with attributes brand, price, model, and color. Subsequently, create two derived classes, Car1 and Car2, both inheriting from the Car class. Each derived class should introduce its attributes, and:
Implement a method display_details in the base class Car to print the common attributes (brand, price, model, color).
Override the display_details method in each derived class (Car1 and Car2) to print the brand, price, model, and color respectively.
class Car:
	def __init__(self,brand,price,model,color):
		self.brand=brand
		self.model=model
		self.price=price
		self.color=color
	def display(self):
		print(f"{self.brand}")
		print(f"{self.price}")
		print(f"{self.model}")
		print(f"{self.color}")
class Car1(Car):
	def display(self):
		super().display()
class Car2(Car):
	def display(self):
		super().display()
def get_car_details():
	brand = input("brand: ")
	price = float(input("price: "))
	model = input("model: ")
	color = input("color: ")
	return brand, price, model, color
print("Details for Car 1:")
car1_brand, car1_price, car1_model, car1_color = get_car_details()
car1=Car1(car1_brand,car1_price,car1_model,car1_color)
print("Details for Car 2:")
car2_brand, car2_price, car2_model, car2_color = get_car_details()
car2=Car1(car2_brand,car2_price,car2_model,car2_color)
print("Car 1 Details:")
car1.display()
print("Car 2 Details:")
car2.display()
