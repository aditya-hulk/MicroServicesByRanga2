# ***Section-11. Introduction to JUNIT***
# 263 Step-1 What is Junit and Unit Testing?
apne s/w ki jar ya war file deploy karke test karna  usko --> ***system testing or integration testing kehte***..

apne individual method ya group of method ya particular class ki test karna called as ***Unit test.***

![Alt text](image-1.png)
# 264 Step-2 Your first JUnit project and Green Bar
### We need a piece of code for which we write unit test. So let's create java project

![Alt text](image.png)
![Alt text](image-2.png)
![Alt text](image-3.png)
### Let's create a class
```java
package com.adi.junit;

public class MyMath {

	//{1,2,3}=> 1+2+3=6 ((pass an array with number) and it return sum of it)
	public int calculateSum(int[] numbers) {
		
		int sum =0;
		for(int number : numbers) {
			sum += number;
		}
		
		return sum;
	}
}
```
### Write Junit Test for this method
![Alt text](image-4.png)
![Alt text](image-5.png)
### So all our source code is present in src folder and test related stuff (junit test) present in test folder
### Create Unit test
![Alt text](image-6.png)
### Provide appropriate details
![Alt text](image-7.png)
![Alt text](image-8.png)
Assertion
-	दृढ़ कथन, निश्‍चयपूर्वक कथन, दावा

![Alt text](image-9.png)
### Run it
![Alt text](image-10.png)
![Alt text](image-11.png)
### Red bar indicates test fail
### Now make this unit test pass & see Famous Green Bar which comes as test passes
![Alt text](image-12.png)
![Alt text](image-13.png)
### Write test for MyMathTest class
![Alt text](image-14.png)
### Now check the result against expected value
![Alt text](image-15.png)
### What happen if you change expected result to 5
```java
package com.adi.junit;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.Test;

class MyMathTest {

	@Test
	void test() {

		MyMath math = new MyMath();

		int numbers[] = { 1, 2, 3 };

		int result = math.calculateSum(numbers);

		System.out.println(result);

		int expectedResult = 5; //Changing to 5

		assertEquals(expectedResult, result);
	}

}
```
![Alt text](image-16.png)
# 265 Step-3 Your first code and first unit test


