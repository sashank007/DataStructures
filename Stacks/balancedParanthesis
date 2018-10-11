# -*- coding: utf-8 -*-
"""
Created on Thu Oct 11 09:22:41 2018

@author: sasha
"""

class Stack():
    def __init__(self):
        
        self.items=[]
    def push(self,value):
        self.items.append(value)
        
    def pop(self):
        return self.items.pop()
        
    def is_empty(self):
        return self.items==[]
    def peek(self):
        return self.items[-1]
    def getStack(self):
        return self.items
    
def is_match(leftParen,rightParen):
   
    if rightParen==')' and leftParen=='(':
        return True
    elif rightParen=='}' and leftParen=='{':
        return True
    elif rightParen==']' and leftParen== '[':
        return True
    else:
        return False
    
def is_parenBalanced(string):
    s = Stack()
    is_Balanced = True
    length = len(string)
    i=0
    while i<length and is_Balanced:
        
        if string[i] in "{[(":
            s.push(string[i])
        else:
            if s.is_empty():
                is_Balanced=False
            else:
                topElement  = s.pop()
 
                if not is_match(topElement,string[i]):
                    is_Balanced=False
        i=i+1
    if s.is_empty() and is_Balanced:
        return True
    else:
        return False

x= [ "{{}}" , "{}]" , "[[[[[]]]]]" , "[[[["]
for i in x:
    balance=is_parenBalanced(i)
    n="" if is_parenBalanced(i) else "not"
    print(("Value {} is {} balanced").format(i ,n))
