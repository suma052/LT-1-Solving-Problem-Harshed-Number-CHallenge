# Task-1
```java
public class Harshad {
    public static void main(String[] args) {
        if (args.length == 0) {
            System.out.println("No input provided");
            return;
        }
        for(int i = 0; i < args.length; i++) {
            int x = Integer.parseInt(args[i]);
            int sum = 0, temp = x;
            while (temp > 0) {
                sum += temp % 10;
                temp /= 10;
            }
            if (sum != 0 && x % sum == 0) System.out.println("YES");
            else System.out.println("NO");
        }
    }
}
```
# Task-2
```java
class Solution {
    int dSum(int t){
     int sum = 0;
    while(t != 0){
        sum = sum + (t % 10);
        t = t/10;
    }
    return sum;
    }
    public int sumOfTheDigitsOfHarshadNumber(int x) {
        int s = dSum(x);
        if(x % s == 0) return s;
        else return -1;
    }
}
```
