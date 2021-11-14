#1
class d():
    def __init__(self,a):
        self.a=a
    def solve(self):
        while self.a>=1:
            print(self.a,end=" ")
            self.a=self.a-1 
        print(" ")
        
a = int(input())
while a>=1:
    b=d(a)
    b.solve()
    a=a-1
    
#2
b = int(input())
s=0
for i in range(1,b+1):
    s=s+i

print("Sum of first {} numbers is: {}".format(b,s))
print("Average of {} numbers is: {}".format(b,s/b))     

#3
#●The number must be divisible by 3;
#●If the number is greater than 120, then skip it and move to thenext number;
#●If the number is greater than 300, then stop the loop.

numbers = [12, 75, 151, 108, 147, 324, 30]
for i in numbers:
    if i>300:
        break;
    elif i>120:
        continue;
    elif i%3==0:
        print(i)
        
#4
m = int(input("Enter starting number: "))
n = int(input("Enter ending number: "))
l = []

for i in range(m,n+1):
    if m>1:
        for j in range(2,i):
            if(i%j==0):
                break;
        else:
            l.append(i)
            
print("Prime numbers between {} and {} are:".format(m,n))
for i in l:
    print(i)
    
#5
f = int(input("Enter number of terms: "))

f1, f2 = 0, 1
count = 1

if f <= 0:
   print("You should enter a positive number")

elif f == 1:
   print("Fibonacci sequence:")
   print(f1)

else:
   print("Fibonacci sequence:")
   while count <= f:
       print(f1,end=" ")
       f_new = f1 + f2
       f1=f2
       f2=f_new
       count += 1
