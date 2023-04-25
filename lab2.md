# Part 1: StringServer
![code](https://user-images.githubusercontent.com/130100567/234160365-a9520742-a679-4d9a-b1c6-3f3d7185d2e4.png)

testing on local server

---
![save1](https://user-images.githubusercontent.com/130100567/234160408-a8621396-a71e-4e38-b1b3-c7641b2a8ecf.png)
---

the url is calling the handleRequest method in the StringServer.java file, 
1. it takes in a url as its argument 
2. it checks if the path of the url is equal to "/add-message"
3. if the path correct then the method checks for if the query of the url has "s=" in it 
4. finally if all of those steps are true (which they are in this case), 
because this is the first time I'm inputting a string, the string variable str is emtpy therefore the strg is just the string being inputted.

---
![save2](https://user-images.githubusercontent.com/130100567/234160423-515dc74f-fc0f-46a2-b79a-581f39d3599a.png)
---

the url is calling the handleRequest method in the StringServer.java file, 
1. it takes in a url as its argument 
2. it checks if the path of the url is equal to "/add-message"
3. if the path correct then the method checks for if the query of the url has "s=" in it 
4. finally if all of those steps are true (which they are in this case), 
since this is the second time I'm calling the method, there's already a previous string input that was saved so the page first prints the previously save string and then the new string on the next line. 
in the actual code itself, the str variable is now both those strings

---
# Part 2: Debugging
Method: reversed(int[] arr)

bug -  how the new array list newArray is intinally made only intializes the length of the old array to newArray.
- A test that the reverse method passes is when the input is an empty string
```
import static org.junit.Assert.*;
import org.junit.*;
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
- Inputs that will always fail testing for this method are non empty string such as {1, 2, 3}. The expected output is {3, 2, 1}
```
import static org.junit.Assert.*;
import org.junit.*;
  @Test
  public void testReversed() {
    int[] input2 = {1, 2, 3};
    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input2));
  }
```
![testing reverse](https://user-images.githubusercontent.com/130100567/234168216-3f669de7-da28-496e-85b3-33d03e828f1f.png)
According to JUnit, the reverse method is outputting {0, *, *} instead of the expected output

newArray is basically always empty because only the length is intialized.
```
public class ArrayExamples {
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
}
 ```

To fix this I created an additional loop that makes newArray a deep copy of the old array
```
public class ArrayExamples {
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i<arr.length; i++){
      newArray[i] = arr[i];
    }
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
}
```

---
# Part 3: Reflection
Before lab 2 and 3 I didn't know how to use the JUnit assert methods myself. I'm really grateful we had a whole lab dedicated to debugging and creating testers because I really needed it. The debugging was a good brain teaser but not too challenging allowing me to focus on figureing out how to use the JUnit tests and reading the expected vs observed messages.
