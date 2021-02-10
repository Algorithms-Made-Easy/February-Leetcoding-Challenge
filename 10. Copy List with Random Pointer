/*
// Definition for a Node.
class Node {
    int val;
    Node next;
    Node random;

    public Node(int val) {
        this.val = val;
        this.next = null;
        this.random = null;
    }
}
*/
class Solution {
    public Node copyRandomList(Node head) {
        if(head==null) return null;
        
        Map<Node,Node> map=new HashMap<>();
        
        Node curr=head;
        
        while(curr!=null){
            map.put(curr, new Node(curr.val));
            curr=curr.next;
        }
        
        for(Node key:map.keySet()){
            Node newNode=map.get(key);
            newNode.next=map.get(key.next);
            newNode.random=map.get(key.random);
        }
        
        return map.get(head);
    }
}

class Solution {
    public Node copyRandomList(Node head) {
        if(head==null) return null;
        
        Node temp=head;
        
        while(temp!=null){
            Node next=temp.next;
            Node random=temp.random;
            temp.next=new Node(temp.val,next,random);
            temp=temp.next.next;
        }
        
        //Update the random 
        Node newHead=head.next;
        temp=head;
        
        while(temp!=null){
            Node next=temp.next;
            if(next.random!=null) next.random=next.random.next;
            temp=next.next;
        }
        
        //Unwinding the list
        temp=head;
        
        while(temp!=null){
            Node copy=temp.next;
            temp.next=copy.next;
            if(copy.next!=null) copy.next=temp.next.next;
            temp=temp.next;
        }
        
        return newHead;
    }
}
