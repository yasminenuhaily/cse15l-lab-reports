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
    ![Image](junit_symptom.png)
