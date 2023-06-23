Head is block or element which contain information related 
to node. A node is a combination or a set of int value and
link value, you can see it a next or address of a next node.

So, class will be create to make node.

Let's say you have 1 -> 2 -> 3 -> NULL,
So 1 is head = first element of a linked list is called head
or block. 1 is int value and have some random addess value.

So |1|0x0| -> |2|0x4| -> |3|0x8| -> NULL

```
class Node{
	public :
			int value;
			// poninter to a Node
			Node* next;

			Node(int val){
					this.data = val;
					this.next = NULL;
			}
}
```
So Node first say 1 is a head and having int value and next 
value. 
