# Cse_15L Lab Report 2 - Servers and Bugs (Week 3)
## Part 1 StringServer
- image
- image 
- image

## Part 2
```@Test 
	public void testReverseInPlace() {
    int[] input1 = { 1,2,3,4,5 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 5,4,3,2,1 }, input1);
    int[] input2 = { 1,2,3,2,1 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 1,2,3,2,1 }, input2);
	}
  ```
- Above shown is a faliure inducing test followed by a non faliure inducing input
- the first input fails due to the list copying onto itself hence changing to the wrong elements
- the second input wont fail because the second half of the array is aldready the same as the first half.
### faulty code
```static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
```static void reverseInPlace(int[] arr) {
    int[] tmp = [arr.length];
    tmp = arr.clone();
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = tmp[arr.length - i - 1];
    }
  }```
