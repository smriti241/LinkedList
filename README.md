# LinkedList
//Insert 
    static SinglyLinkedListNode insertNodeAtHead(SinglyLinkedListNode llist, int data)
    {
         SinglyLinkedListNode temp = new SinglyLinkedListNode(data);   
            temp.next=llist;
           return temp;
    }
    
//
static SinglyLinkedListNode insertNodeAtTail(SinglyLinkedListNode head, int data)
    {
      SinglyLinkedListNode temp = head;
           SinglyLinkedListNode newNode = new SinglyLinkedListNode(data);
            if(head==null)
            {
                    head=newNode;
            }
            else
            {
            while(temp.next!=null)
            {
                    temp=temp.next;
            }
            temp.next=newNode ;
            }
            return head;
    }
    
 //
 static SinglyLinkedListNode insertNodeAtPosition(SinglyLinkedListNode head, int data, int position) {
            SinglyLinkedListNode temp = head;
            SinglyLinkedListNode newNode = new SinglyLinkedListNode(data);
            SinglyLinkedListNode temp1 = null;
            int n=0;
            if(head==null)
            {
                        head=newNode;
            }
            else
            {
                while((n+1)!=position)
                {
                        temp=temp.next;
                        temp1=temp.next;
                        n++;
                }
                    temp.next=newNode;
                    newNode.next=temp1;
            }
           return head;     
    }
//
static void printLinkedList(SinglyLinkedListNode head) 
    {
            SinglyLinkedListNode temp = head;
            if(head!=null)
            {
                    while(temp!=null)
                    {
                            System.out.println(temp.data);
                            temp=temp.next;
                    }
            }
    }
    //
    static SinglyLinkedListNode deleteNode(SinglyLinkedListNode head, int position) {
         SinglyLinkedListNode temp = head;
         SinglyLinkedListNode temp1=temp.next;
            if(head!=null)
            {
                
                    if(position==0)
                    {
                     head=head.next;
                            return head;
                    }
                    int n=0;
                    while((n+1)!=position)
                    {
                            temp=temp.next;
                            temp1=temp.next;
                            n++;
                    }
                    temp.next=temp1.next;
            }
            return head;

    }
    //
     static void reversePrint(SinglyLinkedListNode head) 
    {
            SinglyLinkedListNode temp = head;
            SinglyLinkedListNode temp2 = head;
        if(head!=null)
        {
                int size=0;
                while(temp.next!=null)
                {
                        temp=temp.next;
                        size++;
                }
                
               int arr[] = new int[size+1];
                for(int i=size;i>=0;i--)
                {
                        arr[i]=temp2.data;
                        temp2=temp2.next;
                }
                for(int i=0;i<=size;i++)
                        System.out.println(arr[i]);
        }
    }
