You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order, and each of their nodes contains a single digit. Add the two numbers and return the sum as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

Idea:
At ith position of link list, is 10^(i-1) value mult with the val in the node, which can generate the result and carry bits 0 or 1
So the algorithmn goes:
suppose L1 has n number and L2 has m number
Carry = 0
For i in range (max(m,n)):
  if (i == 0):
    Result[i] = (L1[i] + L2[I] % 10);
    Carry = int((L1[i] + L2[I])/10);
  if(i < m)&&(i <n):
    Result = ((L1[i] + L2[I] + Carry) % 10)
    Carry = int((L1[i] + L2[I] + Carry) / 10)
   elif(i < m) && (i >= n):
    Result = (L1[i] + Carry) % 10;
    Carry = int((L1[i]+Carry)/10)
   elif(i >= m) && (i < n ):
    Result = (L2[i] + Carry) % 10;
    Carry = int((L2[i]+Carry)/10)
 Set three ListNode head, prev, current
 IF head = nullptr // First Node
 head = Current
 IF prev != nullptr // Not First Node
 prev->next = current
 prev = current
 
 IF only one node head = 0 return new ListNode(0)
    
