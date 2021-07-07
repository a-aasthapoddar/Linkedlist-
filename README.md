# Linkedlist-
Implementing linkedlist using java


  
      class Node{
        int data;
        Node next;
      }
      
  
      class linkedlist{
        Node head;
        
 
        public void insert(int data){     
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
  
  
        public void printlist(){         
          Node node = head;
          while(node!=null){
            System.out.print(node.data+" ");
            node = node.next;
          }
        }
      }

 
      public class Main{               
        public static void main(String [] args){          
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
