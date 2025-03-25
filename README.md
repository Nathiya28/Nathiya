Q1)  CALCULATING GAIN PERCENTAGE  
Vikram buys an old scooter for Rs. A and spends Rs. B on its repairs. If he sells the scooter for Rs. C ,
 what is his gain %?  
Write a program to compute the gain %.  
  
Output value should be displayed correct to 2 decimal places. (Use .2f method)  
Input Format 
The first input is an integer which corresponds to Cost price. The second input is an integer 
which corresponds to repair cost. The third input corresponds to the Selling price.   
 
Output Format 
Refer sample input and output for formatting specifications. The float values are displayed 
correct to 2 decimal places (Use .2f method)   
 
Code Constraints Sample 1  Input 
 
4700 
800 
5800 
 
Sample 1  Output 
5.45 
 
cp = int(input())
 ra = int(input())
 sp = int(input())
 cp += ra
 sp -= cp
 print("{:.2f}".format(sp*100/cp))
 Q2)  Wisconsin State Fair  
Wisconsin State Fair is one of the largest midsummer celebrations in the Midwest Allis, showcasing 
the agriculture skills and prowess of the state. The Event organizers hired few part-time employees to 
work at the fair and the agreed salary paid to them are as given below:  
Weekdays --- 80 / hour  
Weekends --- 50 / hour  
Justin is a part-time employee working at the fair. Number of hours Justin has worked in the 
weekdays is 10 more than the number of hours he had worked during weekends. If the total salary 
paid to him in this month is known, write a program to estimate the number of hours he had worked 
during weekdays and the number of hours he had worked during weekends.  
Input Format 
First line of the input is a float value that corresponds to the total salary paid to Justin.   
 
Output Format 
First line of the output should display the number of hours Justin has worked during the 
weekdays. Second line of the output should display the number of hours Justin has worked 
during the weekends. Refer sample input and output for formatting specifications.   
 
Code Constraints Sample 1  Input 
 
2750 
 
Sample 1  Output 
25.0 15.0
 
Sample 2  Input 
1250 
 
Sample 2  Output 
13.0 
3.0 
s = float(input())
 x = (s+500)//130
 print(x)
 print(x-10)
 Q3)  John's little brother is struggling with Maths. He decided to design a calculator with basic 
operations such as Addition, Subtraction, Multiplication and Division. The calculator should input 
two float numbers and an operator from the user. It should perform an operation according to the 
operator entered and must take input in given format.  
Input Format 
First line contains 2 float numbers separated by spaces. Second line contains operator which is
 going to perform on those inputs.   
Output Format 
Print the output   
 
Code Constraints 
Sample 1  Input 
20 8 
+ 
Sample 1  Output 
28.0 
 
 
Sample 2  Input 
20 8 - 
Sample 2  Output 
12.0 
  
Sample 3  Input 
20 8 
* 
Sample 3  Output 
160.0 
 
Sample 4  Input 
20 8 
/ 
Sample 4  Output 
2.5 
 
n=input().split()
 a=float(n[0])
 b=float(n[1])
 c=input()
 if c == '+':
    print(a+b)
 if c == '-':
    print(a-b)
 if c == '*':
    print(a*b)
 if c == '/':
    print(a/b)
 
Q4)  Transceiver Communication   
The ExCon Fair is the region's largest trade fair on Construction Equipment & Technology. The Event
 is targeted to be attended by approx. 30 million visitors. To ensure the smooth functioning of the event
 and the safety of the visitors, the Event Coordinator, Security Chief and Crowd Control Chief were 
instructed to carry two-way transceivers so they can stay in constant contact. Of course, these 
transceivers have a limited range so if two are too far apart, they cannot communicate directly.  The 
Event Coordinator invested in top-of-the-line transceivers which have a few advanced features. One is
 that even if two people cannot talk directly because they are out of range, if there is another 
transceiver that is close enough to both, then the two transceivers can still communicate with each 
other using the third transceiver as an intermediate device.  
There has been a minor emergency at the Event and the Event Coordinator needs to communicate 
with both the Security Chief and Crowd Control Chief right away. Help the Event Coordinator 
determine if it is possible for all three people to communicate with each other, even if two must 
communicate through the third because they are too far apart.  
Input Format 
The first line of the input contains a positive integer R ≤ 1,000 indicating that two transceivers
 can communicate directly without an intermediate transceiver if they are at most R meters 
away from each other. The remaining three lines of the input describe the current locations of 
the Event Coordinator, Security Chief and Crowd Control Chief, respectively. Each such line 
contains two integers X, Y (at most 10,000 in absolute value) indicating that the respective 
person is located at position X,Y.   
 
Output Format 
Output a single line containing a single string. If it is possible for all three to communicate 
then you should output "Yes". Otherwise, you should output "No". To be clear, we say that 
two transceivers are close enough to communicate directly if the length of the straight line 
connecting their X, Y coordinates is at most R. Refer to sample input and output for 
formatting specifications.   
 
Code Constraints Sample 1  Input 
 
1 
0 1 
00 
10 
 
Sample 1  Output 
0 1 
00 
10 
Yes 
 
 
Sample 2  Input 
2 
0 0 
0 2 
2 1 
 
Sample 2  Output 
0 0 
0 2 
2 1 
No 
 R = int(input())
 x1, y1 = map(int, input().split())  
x2, y2 = map(int, input().split())  
x3, y3 = map(int, input().split())  
dist_ec_sc = (x2 - x1) ** 2 + (y2 - y1) ** 2  
dist_ec_cc = (x3 - x1) ** 2 + (y3 - y1) ** 2 
dist_sc_cc = (x3 - x2) ** 2 + (y3 - y2) ** 2  
R_squared = R ** 2
 if (dist_ec_sc <= R_squared and dist_ec_cc <= 
R_squared) or \
 (dist_ec_sc <= R_squared and dist_sc_cc <= 
R_squared) or \
 (dist_ec_cc <= R_squared and dist_sc_cc <= 
R_squared):
 print("Yes")
 else:
 print("No")
 Q5)  Perfect number  
Write a python program to get a number from the user and find out whether the given number is a 
perfect number or not  
Explantion  
A perfect number is a positive integer that is equal to the sum of its positive divisors, excluding the 
number itself  
input - 6  
divisors - 1,2,3  
sum - 6  
If sum of divisors and original number are equal, it is a perfect number   
Input Format 
The input should be an integer   
Output Format 
Refer the sample output   
Code Constraints 
Sample 1  Input
 6 
Sample 1  Output 
Perfect number 
Sample 2  Input 
20 
Sample 2  Output 
Not a perfect number 
num=int(input())
 sum_v=0
 for i in range(1,num):
 if (num%i==0):
 sum_v=sum_v+i
 if(sum_v==num):
 print("perfect number")
 else:
 print("Not a perfect number")
Q6)  Write a program to print the series in descending order from the given value of n by using for 
loop.  
  
Example:  
Input:  
4  
Output:  
4 3 2 1  
Input Format 
Input consists of an integer.   
 
Output Format 
The output displays the series till the nth term. Refer sample input and output for better 
understanding.   
 
Code Constraints Sample 1  Input 
 
5 
 
Sample 1  Output 
5 4 3 2 1  
Sample 2  Input 
10 
 
Sample 2  Output 
10 9 8 7 6 5 4 3 2 1  
n = int(input())
 for i in range(n, 0, -1):
    print(i, end=" ")
 Q7)  Write a python function to find the Max of three numbers.  
Function Name: max_of_three()  
Input Format 
Input consists of an integer separated by a comma.   
 
Output Format 
Output prints a maximum of three numbers.   
 
Code Constraints Sample 1  Input 
 
3,-7,9 
 
Sample 1  Output 
9 
 
 
Sample 2  Input 
5,-3,6 
 
Sample 2  Output 
6 
 def max_of_three(a, b, c):
    if a >= b and a >= c:
        return a
    elif b >= a and b >= c:
        return b
    else:
        return c
              input_values = input().split(',')
 a = int(input_values[0])
 b = int(input_values[1])
 c = int(input_values[2])
 print(max_of_three(a, b, c))
 Q8)  Write a Python function to check whether a number is in a given range. Here n1 and n2 have 
represented the range. Print inside if the number is between range otherwise print outside.  
Function Name: test_range()  
  
Input Format 
The first line of the input represents the starting range n1 The second line of the input 
represents the ending range n2.   
 
Output Format 
Output prints whether a number is in a given range or not.   
 
Code Constraints Sample 1  Input 
 
100 
120 
111 
 
Sample 1  Output 
Inside 
 
 
Sample 2  Input 
10 
20 
25 
 
Sample 2  Output 
Outside 
n1=int(input())
 n2=int(input())
 def test_range(n):
 if n in range(n1,n2):
 print("Inside")
 else :
 print("Outside")
 r=int(input())
 test_range(r) 
Q9)  Adjacent Stick Game   
Mukesh and his friends have set out on a vacation to Coorg. They have booked accommodation in a 
resort and the resort authorities organize Campfires every night as a part of their daily activities. 
Mukesh volunteered himself for an activity called the "Adjacent Stick Game" where sticks of 
different lengths will be placed in a line and Mukesh needs to remove a stick from each adjacent pair 
of sticks. 
He then has to form a bigger stick by combining all the remaining sticks.  
Mukesh needs to know the smallest length of the bigger stick so formed and needs your help to 
compute the same. Given the number of sticks N and the lengths of each of the sticks, write a program
 to find the smallest length of the bigger stick that is formed.  
  
Input Format 
The first line of input contains an integer N denoting the number of sticks. Assume that the 
maximum value for N as 50. Assume that N is always even. The next line of input contains an
 N integer denoting the length of each of the sticks.   
 
Output Format 
Output the smallest length of the bigger stick that is formed. Refer sample input and output 
for formatting specifications.    
 
Code Constraints Sample 1  Input 
 
4 
4 2 3 5 
 
Sample 1  Output 
5 
 
 
Sample 2  Input 
4 
2 1 3 1 
 
Sample 2  Output 
2 
N = int(input())
 sticks = list(map(int, input().split()))
 result = []
 for i in range(0, N, 2):
    if sticks[i] > sticks[i+1]:
        result.append(sticks[i])
    else:
        result.append(sticks[i+1])
 print(min(result))
 
Q10)  Write a python code to accept a list of elements from the user and perform the Swapping of 
adjacent elements  
 
Input Format 
The first line of input must be the size of the list  The second line of input must be the 
elements of the list   
 
Output Format 
Refer the sample output   
 
Code Constraints Sample 1  Input 
 
5 
12 3 4 5 
 
Sample 1  Output 
21 4 3 5  
 
Sample 2  Input 
6 
12 34 56 78 90 100 
 
Sample 2  Output 
34 12 78 56 100 90  
N = int(input())
 elements = input().split()
 for i in range(N):
    elements[i] = int(elements[i])
 for i in range(0, N - 1, 2):  
    elements[i], elements[i + 1] = elements[i + 1], 
elements[i] 
print(*elements)
 Q11)  Write a Python program to replace ith value of tuples in a list.  
Input Format 
First line of the input consists of 4 integers corresponding to n (number of tuples), m (number 
of elements in each tuple), i (the index of the element to be changed in each tuples) and z ( the
 value to be replaces in the ith index. Followed by 'm' number of tuple elements for 'n' number 
of elements.   
 
Output Format 
Output displays the list of tuple after replacing the value 'z' in ith index of each tuple.   
 
Code Constraints Sample 1  Input 
 
3 3 3 100 
10 20 40 
50 60 90 
20 10 88 
 
Sample 1  Output 
[(10, 20, 100), (50, 60, 100), (20, 10, 100)] 
Sample 2  Input 
3 3 2 100 
10 20 40 
50 60 90 
20 10 88 
 
Sample 2  Output 
[(10, 100, 40), (50, 100, 90), (20, 100, 88)] 
n, m, i, z = map(int, input().split())
 modified_tuples = []
 for j in range(n):
    tuple_elements = tuple(map(int, input().split()))
    tuple_list = list(tuple_elements)
    tuple_list[i - 1] = z 
    modified_tuples.append(tuple(tuple_list))
 print(modified_tuples)
 Q12)  Given, a list of tuple , the task is to sort the list of tuples based on the sum of elements in the 
tuple.  
  
 
Input Format 
First line contains number of tuples N inside the list N lines contains tuple elements separated 
by spaces of length 2   
 
Output Format 
Output displays the list of tuples in sorted order.   
 
Code Constraints 
Each tuple is of length of 2 Tuple has only integer values (can include negative values)   
 
Sample 1  Input 
3 
2 3 
24 
30 
 
Sample 1  Output 
[(3, 0), (2, 3), (2, 4)] 
n = int(input())
 tuple_list = []
 for _ in range(n):
    tuple_elements = tuple(map(int, input().split()))
    tuple_list.append(tuple_elements)
 sorted_tuples = sorted(tuple_list, key=lambda x: 
sum(x))
 print(sorted_tuples) 
 
Q13)  Write a program to Convert key-values list to flat dictionary  
  
Create a dictionary {'month' : [1, 2, 3], 'name' : ['Jan', 'Feb', 'March']}.  
Convert this dictionary to flat dictionary.  
 
Input Format 
No Console Input   
 
Output Format 
Output consists of Flat dictionary.   
 
Code Constraints Sample 1  Input Sample 1  Output 
            {1: 'Jan', 2: 'Feb', 3: 'March'} 
d = {'month': [1, 2, 3], 'name': ['Jan', 'Feb', 'March']}
 flat_dict = dict(zip(d['month'], d['name']))
 print(flat_dict)
 
Q14)  A vegetable vendor wishes to store the vegetables she sells in her shop along with the price/kg. 
Write a python script to achieve this.   
  
She initially stored 5 Vegetables along with its price/kg. To this add a new vegetable with its price and
 also print the cost of given vegetable - print ‘Zero’ if not available. Finally update the cost of given 
vegetable.   
  
Assume while updating the cost of given vegetable, the given vegetable is already included.  
  
Refer Input format and Sample Input section for better understanding  
  
Input Format 
First 5  lines contains vegetable names (string) and its price/kg (float) separated by comma 
Next line contains new vegetable name and its price separated by comma Next line contains 
the name of the vegetable whose price needs to be displayed. If the given vegetable is not 
available print 'Zero' Next line contains vegetable name and its new price to be updated 
separated by comma.  Note: Vegetable names are of data type string Price/kg are of data type 
float   
Output Format 
First line of the output consists of price of the given vegetable. Second line of the output 
consists of updated price of the given vegetable name.    
Code Constraints Sample 1  Input 
Onion,45 
Tomato,15 
carrot,60 Peas,120
 Brinjal,45 
Beets,70 
Brinjal 
Onion,55 
Sample 1  Output 
45.0 
Onion,55 55.0 Brinjal 
Sample 2  Input 
Tomato,30 
Peas,100 
Peas,120 cucumber,55  
Zero carrot,45 120.0 
veg_dict = {}
 for i in range(0,5):
 name_price = input().split(',')
 veg_dict[name_price[0]] = 
f
 loat(name_price[1])
 new_veg = input().split(',')
 Beets,45 
Sample 2  Output 
veg_dict[new_veg[0]] = float(new_veg[1])
 veg_name = input()
 if veg_name in veg_dict.keys():
 print(veg_dict[veg_name])
 else:
 print("Zero")
 upd_price_veg = input().split(',')
 veg_dict[upd_price_veg[0]] = 
f
 loat(upd_price_veg[1])
 print(veg_dict[upd_price_veg[0]])
 Q15)  Write a program with class named Circle constructed by a radius and 
two methods which will compute the area and the perimeter of a circle.  
Class Name: Circle  
Method1: area  
Method2: perimeter  
Create an object for the class Circle and display the area and perimeter of a circle.  
Note: Use pi = 3.14  
Input Format 
The input contains positive integer representing radius of a circle   
Output Format 
The output displays the area and perimeter of a circle.   
Code Constraints 
Sample 1  Input 
8 
Sample 1  Output 
200.96 
50.24  
 
Sample 2  Input 
23 
 
Sample 2  Output 
1661.0600000000002 
144.44 
class Circle():
 def __init__(self, r):
 self.radius = r
 def area(self):
 return self.radius**2*3.14
 def perimeter(self):
 return 2*self.radius*3.14
 radius = int(input())
 NewCircle = Circle(radius)
 print(NewCircle.area())
 print(NewCircle.perimeter()) 
 
Q16)  Write a program to reverse a sentence word by word. Use Python class to achieve the result.  
Class name: python_string  method
 name: reverse_words  
  
Input Format 
The input contains a sentence.   
             Output Format 
The output displays reversing a given sentence word by word.   
 
Code Constraints Sample 1  Input 
 
Hello Python 
 
Sample 1  Output 
Python Hello 
Sample 2  Input 
Trees are beautiful gift to nature 
 
Sample 2  Output 
nature to gift beautiful are Trees 
class python_string:
 def __init__(self,inp_string):
 self.s = inp_string
 def reverse_words(self):
 return ' '.join(reversed(s.split()))
 s= input()
 reverse = python_string(s)
print(reverse.reverse_words())
 
Q17)  Write a program to create the following:  
Class Name: Pow  parameters:
 a, b (integers)  
Method: display (to print the value of a to the power of b)  
  
Class Name: Pow1 (child class of Pow)  parameters:
 inherited from Pow  
Method: display1 (to print the value of a*b)  
  
Create an object for Pow1. Using that object, call display and display1.  
 Refer sample input and output for formatting specifications.  
 Input Format 
The first line of the input contains an integer representing a The second line of the input 
contains an integer representing b   
 
Output Format 
The first line of the output contains the value of a to the power of b. The second line of the 
output contains the value of a * b.   
 
Code Constraints 
 
Sample 1  Input 
2 
5 
Sample 1  Output
 32 
10 
class Pow:
    def __init__(self, a, b):
        self.a = a
        self.b = b
    def display(self):
        return self.a ** self.b
 class Pow1(Pow):
    def __init__(self, a, b):
        super().__init__(a, b)
    def display1(self):
        return self.a * self.b
 a = int(input())
 b = int(input())
 obj = Pow1(a, b)
 print(obj.display())  
print(obj.display1())   
Q18)  MULTILEVEL INHERITANCE  
Create 3 classes Person, Staff, TemporaryStaff. Here Person class will be inherited by the Staff class 
and the Staff class will be again inherited by the TemporaryStaff class.  
  
In class Person, create the following attributes and methods  Attributes:
 name  
Methods: display1 - method to display name  
  
In class Staff, create the following attributes and methods  Attributes:
 staffid  
Methods: display2 - method to display staffid  
  
In class TemporaryStaff, create the following data members and methods  Attributes:
 days, hours_worked  
Methods: display3 - method to display days, hours_worked, and salary. (Salary is calculated by days *
 hours_worked * 50)  
  
Write a code to test the above class. Refer to sample input and output for exact requirements.  
Create an object for the class TemporaryStaff and call the methods display1, display2, display3  
  
Note:   
Salary per hour is fixed as Rs.50  
Use super() function  
  
Input Format 
The first line of the input consists of the Name of the person. The second line of the input 
consists of Staff ID. The third line of the input consist of No of days worked. The fourth line 
of the input consist of No of hours worked per day.   
Output Format 
Display the staff details along with Salary as shown in the sample output   
 
Code Constraints 
Sample 1  Input 
John 
101 
15 
5 
Sample 1  Output 
Person Name:John 
Staff id:101 
Number of days:15 
Number of hours worked:5 
Total Salary:3750 
 
 # Class Person
 class Person:
    def __init__(self, name):
        self.name = name
    def display1(self):
        print(f"Person Name:{self.name}")
 class Staff(Person):
    def __init__(self, name, staffid):
        super().__init__(name) 
        self.staffid = staffid
    def display2(self):
        print(f"Staff id:{self.staffid}")
 class TemporaryStaff(Staff):
    def __init__(self, name, staffid, days, hours_worked):
        super().__init__(name, staffid)  
        self.days = days
        self.hours_worked = hours_worked
    def display3(self):
        salary = self.days * self.hours_worked * 50 
        print(f"Number of days:{self.days}")
        print(f"Number of hours worked:{self.hours_worked}")
        print(f"Total Salary:{salary}")
 name = input()        
staffid = int(input())  
days = int(input())     
hours_worked = int(input())
 temp_staff = TemporaryStaff(name, staffid, days, 
hours_worked)
 temp_staff.display1()
 temp_staff.display2()
 temp_staff.display3()
 Q19)  To understand the concept of IOError in Exception handling, Write a program to open the 
random file in read mode.  
If the file is not present, raise an IO Error.  
Refer Sample input and output for better understanding.  
Input Format 
Input consists of filename with proper extension.   
Output Format 
Output displays IO Error exception.   
Code Constraints
 Sample 1  Input 
sample.txt 
Sample 1  Output 
[Errno 2] No such file or directory: 'sample.txt' 
f
 ilename = input()
 try:
 with open(filename, 'r') as file:
 content = file.read()
 print(content)
 except IOError as e:
 print(e)
 Q20)  Peter at Challenger Series  
The Table tennis Challenger Series is the springboard to fame for the future stars of professional table 
tennis. Peter is very passionate about table tennis and made his debut in the first league match of the 
Series against a prominent player Horejsi.  
Peter found some statistics of matches which described who won the points in order. A game shall be 
won by the player first scoring 11 points except in the case when both players have 10 points each, 
then the game shall be won by the first player subsequently gaining a lead of 2 points. Could you 
please help Peter find out who the winner was from the given statistics? (It is guaranteed that statistics
 represent always a valid, finished match.) 
Input Format 
The first and only line of the input consists of a binary string S, which describes a match. '0' 
means Peter lose a point, whereas '1' means he won the point.   
Output Format 
Output on a separate line a string describing who won the match. If Peter won then print 
"Win" (without quotes), otherwise print "Lose" (without quotes). Refer sample input and 
output for formatting specifications.   
Code Constraints 
Sample 1  Input 
10111010111 
Sample 1  Output 
Win 
Sample 2  Input 
00000101011110000 
Sample 2  Output 
Lose 
s = input()
 if(s.count("0")>s.count("1")):
 print("Lose")
 else:
 print("Win")
 Q21)  Remove "the" occurrence   
After the weekend holidays, schools open today. The class teacher found many students were absent. 
So the very next day when students reach class, she announced to submit a leave letter. Shrawanti has 
the habit of including the word “the” frequently in all her sentences. The teachers found it and asked 
her to remove the occurrences of the word “the” from the letter. Can you please help her out?  
Write a program to remove the occurrence of “the” word from entered string.  
Input Format 
Get a sentence from the user.    
Output Format 
Remove "the" occurrence from the input string. Refer to the Sample input and output.   
Code Constraints 
Sample 1  Input 
remove the occurrence of the word from entered string 
Sample 1  Output 
Result string is 
remove occurrence of word from entered string 
Sample 2  Input 
Hello the welcome the to the programming the world 
Sample 2  Output 
Result string is 
Hello welcome to programming world 
s=input()
 print("Result string is")
 print(s.replace("the ",""))
 Q22)  Problem Statement:  
Alternating Code  
It is IPL season and the first league match of Dhilip’s favorite team, "Chennai Super Kings". The CSK
 team is playing at the IPL after 2 years and like all Dhoni lovers, Dhilip is also eagerly awaiting to see
 Dhoni back in action.  
After waiting in long queues, Dhilip succeeded in getting the tickets for the big match. On the ticket, 
there is a letter code that can be represented as a string of upper-case Latin letters.  
Dhilip believes that the CSK Team will win the match in case exactly two different letters in the code 
alternate. Otherwise, he believes that the team might lose. Please see the note section for the formal 
definition of alternating code.  
You are given a ticket code. Please determine, whether CSK Team will win the match or not based on 
Dhilip’sconviction. Print "YES" or "NO" (without quotes) corresponding to the situation.  Note:
 Two letters x, y where x != y are said to be alternating in a code if the code is of the form "xyxyxy...". 
Input Format  
The input must be a string   
Output Format   
Sample 1  Input 
Refer the sample output    
a = input()
 len_a = len(a)
 x = a[0]
 y = a[1]
 s = 0
 if x == y:
 s = 1
 else:
 Sample 2  Output xyxyxy 
for i in range(len_a):
 if i % 2 == 0:
 if x != a[i]:
 s = 1
 break
 else:
 if y != a[i]:
 s = 1
 break
 if s == 1:
 print("No")
 else:
 print("Yes") 
Sample 1  Output 
Yes 
Sample 2  Input Code Constraints 
No 
xxyy 
