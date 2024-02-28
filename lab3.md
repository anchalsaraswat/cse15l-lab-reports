# Anchal Saraswat CSE 15L Lab Report 3

## Part 1 - Bugs
**Failure Inducing Input for Buggy Program:**
```
  @Test
  public void testReverseInPlace2() {
    int[] input2 = {7, 8 ,9};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{9, 8 ,7}, input2);
  }
```
  

**Non Failure Inducing Input:**

```
@Test 
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
  }
```


**Method with Bug (reverseInPlace):**

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
**Output when Running JUnit test with bug in method:**

<img width="927" alt="lab3pic1" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/10f43d12-3941-405c-8485-0ca7c64994f2">


**Corrected Code:**

```
static void reverseInPlace(int[] arr) {
    int left = 0;
    int right = arr.length - 1;
    while (left < right) {
        int val = arr[left];
        arr[left] = arr[right];
        arr[right] = val;
        left++;
        right--;
    }
}
```

**Output when Running JUnit test with corrected method:**

<img width="821" alt="lab3pic2" src="https://github.com/anchalsaraswat/cse15l-lab-reports/assets/44505854/56e93631-0aee-4667-a1db-823b5aac1595">
