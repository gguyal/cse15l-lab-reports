# Lab Report 2

## Part 1: String Server

**The Code**
![Image](https://cdn.discordapp.com/attachments/787224374381117460/1069821874302890025/Screen_Shot_2023-01-30_at_7.22.19_PM.png)

**First Example**
![Image](https://media.discordapp.net/attachments/787224374381117460/1069821874671996958/Screen_Shot_2023-01-30_at_7.24.31_PM.png?width=1786&height=907)

Our first example here is when you first use the path "add-message" through our created url, which in this case is "http://localhost:4001/add-message?s=Hello"

- When using this path we are using the method "handleRequest" called
- In this method, the code checks, if the path contains "add-message" in which in this case it does
- The method then runs the next part of the code which basically splits our url path after our "add-message", with an "=" and each word in the path split by the "=" sign will be added to a string list called "parameters"
- When you type in our specific url path, the first word following the add-message path, will always be an "s" because the code will read this
  - This is so that the first item in the parameters list will be "s" and it will check if it is "s" and run the following code
- However, I implemented a num variable in the code to see if it is the first time, the add-message path is called, in this example it is, therefore, it does not run our first if-statement but instead it runs our second if-statement
  - I also implemented another String called "path" which in this if statement it stores, the first index in parameters, which is stored as the word proceding the = sign in our path, which in this case it is "Hello"
  - The value of num is the incremented, and then the code returns our "path" string

**Second Example**
![Image](https://media.discordapp.net/attachments/787224374381117460/1069821874927833168/Screen_Shot_2023-01-30_at_7.24.57_PM.png?width=1796&height=906)

Our second example is when you use the path "add-message" after it has already been used

- Similarly, this example also uses the method "handleRequest"
- However, up to the if statements at line 15, everything is different
- Since this code has already have been ran once, that means num is incremented by 1
  - This means that our first if statement will run since it also checks if num is greater than 0, which now it is
- The different thing about this example and the last example, is that our string "path" adds the new add-message word with the previously ran words in the url
- The code then returns our string "path" in the form of a list of all of the add-messages we have typed in the url

## Part 2

The bug that we are going to be investigating is within the reverseInPlace method

**Failure Inducing:**

```
@Test
public void testReverseInPlace(){
    int[] input1 = {0, 1, 2, 3, };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3 ,2 ,1 ,0}, (input1));
}
```

**Does not induce Failure:**

```
@Test
public void testReverseInPlace(){
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
}
```

**Failure Inducing Symptom:**

![Image](https://media.discordapp.net/attachments/787224374381117460/1069840557578399764/Screen_Shot_2023-01-30_at_8.40.15_PM.png)

**Does Not Induce Failure Symptom:**

![Image](https://media.discordapp.net/attachments/787224374381117460/1069840557280591993/Screen_Shot_2023-01-30_at_8.39.34_PM.png?width=1880&height=318)

Before:

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

After:

```
static void reverseInPlace(int[] arr) {
    int temp = 0;
    for(int i = 0; i < arr.length/2; i += 1) {
      temp = arr[i];;
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
```

What the before code did, was simply traverse through an array, and then make the current index, equal to the mirrored index on the other side of the list.
To explain, take the array ( 0, 1, 4, 2, 9 ) The code would take the first index ( 0 ) and make it the last index ( 9 ), if we were on the second index ( 1 ), 
we would make it the third index ( 2 ). This results in the product of a mirrored list, keeping the values on the left half of the index. So with our example 
the resulted array would be ( 9, 1, 4, 1, 9 ).

With our new code, we have to make a temporary int value to store an index value before it is changed. We traverse the array, however we traverse it up to the 
half-way point of the array using arr.length/2. We then take the current index point and store it into the temp int value. Similar to our old code, we store the 
mirrored index into our current index. Then we take that mirrored index and store our temporarily stored int value into that index. So that the two indices basically 
swap places. This continues until the half-way point of the array, this works with both odd-length and even-length arrays because odd-length arrays, the middle index 
always stays the same, and even-length arrays do not have a middle value to worry about. Which after everything, the code now returns a reversed array.

## Part 3

One thing that I learned in week 3, was the concept of bugs, and using JUnit to test and solve them. Prior to what I learned in week 3, I have always thought that 
bugs were the compiler errors you would get from wrong code. However, it is sinmply just wrongly coded methods, that does not return what you intend it to do.
In other coding classes, I would always struggle with running methods, and receiving wrong outputs, without knowing why and going through the hassle of constantly 
running the code. With learning JUnit, it aids me as, creating testers to locate different bugs in methods is really helpful. So learning basics of JUnit was really 
helpful.


