You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order, and each of their nodes contains a single digit. Add the two numbers and return the sum as a linked list.<br />

You may assume the two numbers do not contain any leading zero, except the number 0 itself.<br />

Idea:<br />
At ith position of link list, is 10^(i-1) value mult with the val in the node, which can generate the result and carry bits 0 or 1<br />
So the algorithmn goes:<br />
suppose L1 has n number and L2 has m number<br />
Carry = 0<br />
For i in range (max(m,n)):<br />
  if (i == 0):<br />
    Result[i] = (L1[i] + L2[I] % 10);<br />
    Carry = int((L1[i] + L2[I])/10);<br />
  if(i < m)&&(i <n):<br />
    Result = ((L1[i] + L2[I] + Carry) % 10)<br />
    Carry = int((L1[i] + L2[I] + Carry) / 10)<br />
   elif(i < m) && (i >= n):<br />
    Result = (L1[i] + Carry) % 10;<br />
    Carry = int((L1[i]+Carry)/10)<br />
   elif(i >= m) && (i < n ):<br />
    Result = (L2[i] + Carry) % 10;<br />
    Carry = int((L2[i]+Carry)/10)<br />
 Set three ListNode head, prev, current<br />
 IF head = nullptr // First Node<br />
 head = Current<br />
 IF prev != nullptr // Not First Node<br />
 prev->next = current<br />
 prev = current<br />
 
 IF only one node head = 0 return new ListNode(0)<br />
    
