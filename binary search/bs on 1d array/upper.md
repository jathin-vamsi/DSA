- TC : O(log n)
- SC : O(1)
```java
public class Upperbound{
  public static int upperbound(int[] arr,int x){
    int left=0;
    int right=arr.length-1;
    int ans=arr.length;
    while(left<=right){
      int mid=left+(right-left)/2;
      if(arr[mid]>x){
      ans=mid;
      right=mid-1;
      }else {
      left=mid+1;
      }
    }
    return ans;
  }
  public static void main(String[] args){
    int[] arr={1,2,9,13,16,22,24,45};
    int x=10;
    int res=upperbound(arr,x);
    System.out.print("upper bound is found at : " +res);
  }

}
```
