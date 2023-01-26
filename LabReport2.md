Link to my [website](https://celestewv.github.io/cse15l-lab-reports)


*Author:* Celeste Walstrom-Vangor 
<br> *Data Created:* 01/11/23 
<br> *Class:* CSE 15L 


# Blog Post 2:

## Part 1
###
***

## Part 2
### Chosen Code from Lab 3 = Original Code from the ``` reversed(int[] arr) ``` method in ```ArrayExamples```

#### The Chosen Buggy Program Input/Test:
Orinal & Buggy Code:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
  
```
JUnit test:
```
@Test
  public void testReversed() {
    int[] input1 = { 1, 2, 3 };
    assertArrayEquals(new int[]{ 3, 2, 1 }, ArrayExamples.reversed(input1));
  }
```
Without debugging this code, this code did not produce the expected result. 
We expected the code to run on the inputed { 1, 2, 3 } and return { 3, 2, 1 }. 
However, with the bugs, the code returned the original inpu: { 1, 2, 3 }.

#### The Debugged Code:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for (int i = 0; i < arr.length; i++) {
      // System.out.println("Old array element = " + arr[i]);
      newArray[i] = arr[arr.length - i - 1];
      // System.out.println("New element = " + newArray[i]);

    }
    return newArray;
  }

```
The Test that Does not Induce Failure:
```
public void testReversed() {
    int input1[] = { 10, 20, 30, 40, 50 };
    assertArrayEquals(new int[] { 50, 40, 30, 20, 10 }, ArrayExamples.reversed(input1));
}
```
After fixing the bugs in the code, the previous test passed. We expected the input { 10, 20, 30, 40, 50 }
to produce the output { 50, 40, 30, 20, 10 }. We knew the basic code was debugged after receiving the correct
output.

#### Symptom
Here is the JUnit Test failing with the input { 10, 20, 30, 40, 50, 60 } before the code is debugged.
![Image](junitss.png)

Here is the JUnit Test passing with the same input as above now that code has been fixed.
![Image](passedjunitss.png)

***

## Part 3
