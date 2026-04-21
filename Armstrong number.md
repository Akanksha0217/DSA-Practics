

## Uisng Python
```
num=153
n=num
sum=0
nod=len(str(num))
while n>0:
    digit=n%10
    sum += digit**nod
    n=n//10

if sum == num:
    print("Armstrong number")
else:
    print("Not an Armstrong number")
```
