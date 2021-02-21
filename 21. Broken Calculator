class Solution {
    public int brokenCalc(int X, int Y) {
        if(X>=Y) return X-Y;
        
        if(Y%2==0){
            return 1 + brokenCalc(X,Y/2);
        }
        
        return 1 + brokenCalc(X,Y+1)
    }
}

class Solution {
    public int brokenCalc(int X, int Y) {
        int result=0;
        
        while(Y>X){
            result++;
            if(Y%2==0){
                Y/=2;
            }
            else{
                Y++;
            }
        }
        
        return result+(X-Y);
    }
}
