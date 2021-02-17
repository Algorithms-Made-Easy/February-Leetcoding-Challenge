class Solution {
    public int maxArea(int[] height) {
        int water = 0, left = 0, right = height.length-1;
        
        while(left < right) {
            water = Math.max(water, Math.min(height[left], height[right]) * (right-left));
            if(height[left] > height[right]) right--;
            else left++;
        }
        return water;
    }
}
