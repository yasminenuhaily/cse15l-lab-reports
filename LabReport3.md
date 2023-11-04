## Lab Report 3

**Part 1- Bugs** <br>
Chosen bug: `reverseInPlace` method. <br>
- A failure-inducing input for the buggy program: <br>
 ` @Test
   public void testReverseInPlace1()
   {
    int[] input1 = {1, 2};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{2,1},input1);
   } `
  - An input that doesn't induce a failure: <br>
  ` @Test
    public void testReverseInPlaceWorks()
    {
      int[] input1 = {1};
      ArrayExamples.reverseInPlace(input1);
      assertArrayEquals(new int[]{1},input1);
    } `
  - Symptom on JUNIT of the tests: <br>
    ![Image](junit_symptom.png) <br>

  - Buggy Code Before:
    ` static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }`
  - Code After:
   `static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length-i-1] = temp;
    }
  } ` <br>
 <p> These fixes address the issue of the code by directly fixing the bugs. The original error in this code was that it did not store the value of `arr[i]` before modifying it, thus resulting in duplicate values of what was originally stored within `arr[arr.length-1-i]` , which is remedied with the assigning of a temp variable. Additionally, the code looped through the entirety of the array, causing it to, if the temp variable were now there, reverse the array back to its original order, hence the fix of only looping through `arr.length/2` . </p>
