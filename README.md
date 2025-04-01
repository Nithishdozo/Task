class Node {
    int value;
    Node next;
    
    Node(int value) { 
        this.value = value; 
    }
}

public class LinkedListSum {

    public Node sumTwoNumbers(Node list1, Node list2) {
        Node dummyHead = new Node(0);
        Node current = dummyHead;
        int carry = 0;

        while (list1 != null || list2 != null || carry > 0) {
            int num1 = (list1 != null) ? list1.value : 0;
            int num2 = (list2 != null) ? list2.value : 0;
            int sum = num1 + num2 + carry;

            carry = sum / 10;
            current.next = new Node(sum %
