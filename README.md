# Python-
Lab_Program 

#program_1
#binary_search

def bsearch(alist,key):
    start=0
    end=len(alist)-1
    while start <= end:
        mid=(start+end)//2
        if alist[mid]>key:
            end=mid-1
        elif alist[mid]<key:
            start=mid+1
        else:
            return mid
    return -1
alist=(input("enter the elements"))
alist=alist.split()
alist=[int(x) for x in alist]
key=int(input("enter the element to search"))
index=bsearch(alist,key)
if index <0:
    print("not found")
else:
    print("{}found at location{}".format(key,index))

#linear_search
def lsearch(m,n,x):
    for i in range(0,n):
        if m[i]==x:
            return i
    return -1
y=int(input("enter the number of elements"))
m=[]
for i in range(y):
    element=int(input("enter the elements"))
    m.append(element)
x=int(input("enter the number to search"))
n=len(m)
result=lsearch(m,n,x)
if result==-1:
    print("not found")
else:
    print("found at location",result)

    
#program_2

import bisect
def insert(list,n):
    bisect.insort(list,n)
    return list
list=(input("enter the numbers"))
list=list.split()
n=(input("enter the number to insert"))
print(insert(list,n))

#stack_stimulation
n=int(input("enter the number of elements"))
stack=[]
for i in range(0,n):
    element=input("enter elements")
    stack.append(element)
print(stack)
print(stack.pop())
print(stack.pop())

#program_3
#inheritance

class Animal:
    def eat(self):
        print("eating")
class dog(Animal):
    def bark(self):
        print("barking")
class cat(dog):
    def sound(self):
        print("sound")
ob=cat()
ob.eat()
ob.bark()
ob.sound()

#encapsulation
class Employee:
    def __init__(self,name,project):
        self.name = name
        self.project = project
    def work(self):
        print(self.name,"is working on ",self.project)
e=Employee("manu","web")
e.work()

#overloading
class Multi:
    def multi(self,a,b,c =None):
        if c is None:
            return a*b
        else:
            return a*b*c
c=Multi()
print(c.multi(2,4))
print(c.multi(2,4,6))
