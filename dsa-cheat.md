# DSA CHEAT SHEET 
---

### 1 . to find the middle node of a linked list 
have 2 pointer slow and fast. move the slow pointer by one and the fast pointer by two until the fast pointer reaches the end, eventually the slow pointer will stop at the middle node 

---
### 2 . find the intersection node of two linked lists 
have 2 pointers both starting at each linked list, move the pointer simultaneously, once a pointer reaches the end of the linked list move the pointer to the head of the other linked list, repeat this until both the pointers meet at the intersection node

---
### 3 . a linked list has its end node pointing to a node X of the same linked list forming a partial circular linked list, find the node X
have 2 pointers slow and fast. move the slow pointer by 1 and the fast pointer by 2 until they both meet. once the meet each other move either of the pointer to the head of the linked list and continue moving both the pointer with step 1 until the meet, the meeting node is the node X 

---
### 4. reverse a linked list 

##### iterative method
have three pointers prev, temp, front. prev points to null, temp points to head. make front point to the right immediete node after temp, make temp point to prev, move prev to temp and temp to front. do this until temp reaches null and return prev.

##### recursive method
have a function called reverse that returns the last node of the linked list as its base case. the function is called within itself with head's next node as a input parameter. the function now returns the last node of the sub linked list and the last node is captured with a new ptr newhead, create a new ptr front with the node value head.next, make front point to head and head point to null, return the new head which is the last node of the og linked list but the first node of the reversed linked list

### 5. delete the kth node of a linked list from the last
have 2 pointers at the head, move a pointer k times forward, once the pointer reaches the kth position move both the pointers until the first pointer reaches the end, eventually the second pointer lands on the kth position from the last

### 6. reverse nodes in k groups- linked list 
point currentgroupstart to head and previousgrouptail to nullptr. use a function to get the kthnode from the current group starting at currentgroupstart. create a pointer nextgroupstart pointing to kthnode->next and then make kthnode->next point to nullptr to temporarily break the list. now reverse the sub-linked list that starts from currentgroupstart and spans k nodes. create a new pointer reversedgrouphead pointing to the head of the reversed sublist. also create a pointer reversedgrouptail pointing to currentgroupstart (which becomes the tail after reversal).if currentgroupstart is the head, it means we just reversed the first group of size k, so we update head to reversedgrouphead. otherwise, we connect the previousgrouptail->next to reversedgrouphead, linking the previous group with the newly reversed one.finally, connect reversedgrouptail->next to nextgroupstart to restore the link to the remaining list, update previousgrouptail to reversedgrouptail, and move currentgroupstart to nextgroupstart to repeat the process for the next group.
