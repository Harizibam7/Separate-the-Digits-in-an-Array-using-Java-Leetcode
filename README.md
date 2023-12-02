# Separate-the-Digits-in-an-Array-using-Java-Leetcode

    class Solution {
        public int[] separateDigits(int[] nums) {
            int size =0;
            List<Integer> list = new ArrayList<>();
            for(int num:nums){
                List<Integer> cur = new ArrayList<>();
                while(num!=0){
                    int rem = num%10;
                    cur.add(rem);
                    num/=10; 
                }
                for(int i = cur.size()-1;i>=0;i--){
                    list.add(cur.get(i));
                    size++;
                }
            }
            int[] digits = new int[size];
            int j =0;
            for(int i: list){
                digits[j++] = i; 
            }
            return digits;
        }
    }
