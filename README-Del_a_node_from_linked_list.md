# LeetCode-June-2020-challenge
This repo has Java solutions to all the LeetCode June 2020 challenge questions. 

#Delete a node from Linked List

/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 * 
 * public delete(ListNode node){
 * }
 */
 
1. The trick here in this question is no head is given pointing to the linked list.
2. When head is given, traversing would have been damn easy.
3. When the head is not given, and only the node that has to be deleted is given, we have to make use of this node to traverse in the following way.
   a. Before starting, look at the definition of Linked List as above.
   b. Let's say node that has to be deleted is A.
   c. Now, replace the value in A with the value in the node pointed by A.next
   d. And now, traverse the remaining nodes by using the above steps and replace the values in the remaining nodes.
   
E.g :

Input : [7,2,9,1] , Node = 2
Solution : 
  a. [7,9,9,1]   --- 2 is replaced with the value the node 2.next is pointing i.e., 9 and traverse to next node, 9.
  b. [7,9,1,1]   --- the same as above 
  c. [7,9,1]  -- Output

