## Lab Report 3

** Part 1- Bugs ** <br>
Chosen bug: 'reverseInPlace' method. <br>
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
  } `
