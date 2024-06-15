# python-week-5
1.
def find_substring(string1, string2):
    index = string1.find(string2)
    return index if index != -1 else -1;


string1=input()
string2 =input()

print(find_substring(string1, string2))

2.
S = input().strip()
s_list = list(S)
start = 0
end = len(s_list) - 1

while start < end:
    if not s_list[start].isalpha():
        start += 1
    elif not s_list[end].isalpha():
        end -= 1
    else:
        s_list[start], s_list[end] = s_list[end], s_list[start]
        start += 1
        end -= 1

print(''.join(s_list))

3.
a=input()
i=0
x=''
y=''
z=''
while(i<len(a)):
    if(a[i]=='@'):
        break
    else:
        x+=a[i]
    i+=1
i+=1
while(i<len(a)):
    if(a[i]=='.'):
        break
    else:
        y+=a[i]
    i+=1
i+=1
while(i<len(a)):
    z+=a[i]
    i+=1
print(z)
print(y)
print(x)

4.
def are_strings_balanced(s1,s2):
    return set(s1) <=set(s2)
s1=input()
s2=input()
print(are_strings_balanced(s1,s2))

5.
str=input()
lettercount=0
digitcount=0
digitcount=0
specialcount=0
for char in str:
    if char.isalpha():
        lettercount+=1
    elif char.isdigit():
        digitcount+=1
    else:
        specialcount+=1
print(lettercount)
print(digitcount)
print(specialcount)

6.
T = int(input())

for _ in range(T):
    string1 = input().lower()
    string2 = input().lower()

    if string1 < string2:
        print("-1")
    elif string1 > string2:
        print("1")
    else:
        print("0")

7.
# List of keywords
keywords = ["break", "case", "continue", "default", "defer", "else", "for", "func", "goto", "map", "range", "return", "struct", "type", "var"]

# Input from user
user_input = input().strip()

# Check if input is a keyword
if user_input in keywords:
    print(user_input, "is a keyword")
else:
    print(user_input, "is not a keyword")

8.
a=input()
a=a.lower()
b=a.split()
l1=[]
for i in b:
    s=i[::-1]
    if(i==s):
        continue
    else:
        l1.append(i)
for i in l1:
    print(i,end=' ')

9.
sen=input()
word=sen.split()
longestword=""
maxlen=0
for word in word:
    if len(word)>maxlen:
        longestword=word
        maxlen=len(word)
print(longestword)
print(maxlen)

10.
def remove_common_characters(s1, s2):
    return ''.join([char for char in s1 if char not in s2])

# Test the function with the sample input
sample_input_s1 =input()
sample_input_s2 =input()
sample_output = remove_common_characters(sample_input_s1, sample_input_s2)
print(sample_output)
