# 21.-Merge-Two-Sorted-Lists

# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def mergeTwoLists(self, list1, list2):
        k=[]
        temp=None
        head=None
        while list1:
            k.append(list1.val)
            list1=list1.next
        while list2:
            k.append(list2.val)
            list2=list2.next
        k.sort()
        for i in k:
            node=ListNode(i)
            if temp is None:
                head=temp=node
            else:
                temp.next=node
                temp=node
        return head
                    
