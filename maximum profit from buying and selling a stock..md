# 🚀 Question
Find the maximum profit from buying and selling a stock.

## 🧠 Problem
You are given an array where:
👉 arr[i] = price of stock on day i

You need to:
- Buy on one day
- Sell on a later day
- Maximize profit

## Solution 
### Using Python
```
arr = [7,1,5,3,6,4,8]

min_price = arr[0] #7 1
max_profit = 0 # 0  4  5
#price= 7 1 5  3 6 4
#profit = 0 4 2 5 3

for price in arr:
    
    if price < min_price:  #
        min_price = price
    
    profit = price - min_price

    if profit > max_profit:
        max_profit = profit

print(max_profit)
```

### Using Js
```
let arr = [7, 1, 5, 3, 6, 4];

let min_price = arr[0];
let max_price = 0;
let profit = 0;

for (let num of arr) {
  if (num < min_price) {
    min_price = num;
  }
  profit = num - min_price;
  if (profit > max_price) {
    max_price = profit;
  }
}
console.log(max_price);

```
