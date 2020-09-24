## Sorting Algorithm



### 快速排序

```java
import java.util.Random;

public class quicksort {

    public static void swap(int index1, int index2, int[] nums) {
        int temp = nums[index1];
        nums[index1] = nums[index2];
        nums[index2] = temp;
    }

    public static void quicksort(int left, int right, int[] nums) {
        if(left < right) {

            int returningPivotIndex = partition(left, right, nums);

            quicksort(left, returningPivotIndex-1, nums);
            quicksort(returningPivotIndex+1, right, nums);
        }
    }

    public static int partition(int left, int right, int[] nums) {

        Random rand = new Random(0);
        int pivotIndex = rand.nextInt(right-left+1) + left;
        int pivotValue = nums[pivotIndex];
        swap(pivotIndex, right, nums);

        int i = left;

        for(int j = left; j < nums.length-1; j++) {

            if(nums[j] < pivotValue) {
                swap(i, j, nums);
                i++;
            }

        }


        swap(i, right, nums);
        return i;
    }

    public static void main(String[] args) {

        int[] nums = new int[] {2,4 ,5,10, 77, 53, 0, 2, 42, 45, 95,23,21};
        quicksort(0, nums.length-1, nums);
        for(int num : nums) {
            System.out.print(num + " ");
        }
    }
}

```



