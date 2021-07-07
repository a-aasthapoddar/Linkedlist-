# Linkedlist-
Implementing linkedlist using java


  //creating a node
class Node{
  int data;
  Node next;
}
  //class linkedlist to insert and print elements in list
class linkedlist{
  Node head;
  
  public void insert(int data){     //insert method to take elements for list
    Node node = new Node();
    node.data = data;
    
    if(head == null){
      head = node;
    }else{
      Node n = head;
      while(n.next!=null){
        n = n.next;
      }
      n.next = node;
    }
  }
  
  public void printlist(){         //print method to print the list
    Node node = head;
    while(node!=null){
      System.out.print(node.data+" ");
      node = node.next;
    }
  }
}

public class Main{                //main class
  public static void main(String [] args){          //main method
    linkedlist list = new linkedlist();
    
    list.insert(5);
    list.insert(20);
    list.insert(15);
    list.insert(11);
    
    list.printlist();
  }
}


OUTPUT-
5 20 15 11
