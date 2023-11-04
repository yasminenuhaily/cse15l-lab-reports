## Lab Report 3

** Part 1- Bugs ** <br>
Chosen bug: 'reverseInPlace' method. <br>
- A failure-inducing input for the buggy program: <br>
  @Test <br>
 ` public void testReverseInPlace1()
   {
    int[] input1 = {1, 2};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{2,1},input1);
   } `
  
