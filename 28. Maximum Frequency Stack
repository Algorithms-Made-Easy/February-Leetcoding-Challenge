//Using Stack
class FreqStack {
    Map<Integer, Integer> freqMap;
    Map<Integer, Stack<Integer>> freqStack;
    int maxFreq;
    public FreqStack() {
        freqMap = new HashMap<>();
        freqStack = new HashMap<>();
        maxFreq = 0;
    }
    //Increment value in freqMap, 
    //updating the maxFreq
    //Adding value in dfreqStack
    public void push(int x) {
        int freq = freqMap.getOrDefault(x,0)+1;
        freqMap.put(x, freq);
        if(freq > maxFreq) maxFreq = freq;
        freqStack.computeIfAbsent(freq, f->new Stack()).push(x);
    }
    
    //Return and remove the top of maxFreq
    //Update maxFreq (Decrementing, if applicable)
    //Update freqMap
    public int pop() {
        Stack<Integer> s = freqStack.get(maxFreq);
        int top = s.pop();
        if(s.isEmpty()) maxFreq--;
        freqMap.put(top, freqMap.get(top)-1);
        return top;
    }
}

//Using ArrayList
class FreqStack {
    Map<Integer, Integer> freqMap;
    ArrayList<ArrayList<Integer>> freqStack;
    int maxFreq;
    public FreqStack() {
        freqMap = new HashMap<>();
        freqStack = new ArrayList<>();
        freqStack.add(new ArrayList<Integer>());
        maxFreq = 0;
    }
    //Increment value in freqMap, 
    //updating the maxFreq
    //Adding value in dfreqStack
    public void push(int x) {
        int freq = freqMap.getOrDefault(x,0)+1;
        freqMap.put(x, freq);
        if(freq > maxFreq) maxFreq = freq;
        //freqStack.computeIfAbsent(freq, f->new Stack()).push(x);
        if(freqStack.size() <= freq) freqStack.add(new ArrayList());
        freqStack.get(freq).add(x);
    }
    
    //Return and remove the top of maxFreq
    //Update maxFreq (Decrementing, if applicable)
    //Update freqMap
    public int pop() {
        ArrayList<Integer> s = freqStack.get(maxFreq);
        int top = s.remove(s.size()-1);
        if(s.isEmpty()) maxFreq--;
        freqMap.put(top, freqMap.get(top)-1);
        return top;
    }
}
