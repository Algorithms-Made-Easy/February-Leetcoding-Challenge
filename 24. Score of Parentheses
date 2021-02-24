class Solution {
    public int scoreOfParentheses(String S) {
        int count = 0; 
        Stack<Integer> st = new Stack<>();
        for(char c : S.toCharArray()) {
            int val = 0;
            if(c=='(') st.push(0);
            else {
                //Calculate the score
                while(st.peek() != 0) val+=st.pop();
                val = Math.max(2*val,1);   //() gives 1
                st.pop();
                st.push(val);
            }
        }
        while(!st.isEmpty()) count+=st.pop();
        return count;
    }
}
