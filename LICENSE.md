#Merge point in data structures using python
class Node: #node creation
    def __init__(self,data):
        self.data=data
        self.next=None
class Llist: #main logic for list
    def __init__(self):
        self.head=None
    def build(self,data):
        new_node=Node(data) #calling Node class for creation of new_node
        if self.head is None:
            self.head=new_node
        else:
            temp=self.head
            while temp.next is not None:
                temp=temp.next
            temp.next=new_node
    def get_intersction_node(self,other_list):
        a,b=self.head,other-list
        while a!=b:
            a=other_list.head if not a else a.next
            b=self.head if not b else b.next
        return a         
    
    def display(self):
        temp=self.head
        while temp is not None:
            print(temp.data,end="->")
            temp=temp.next
        print("None")
           
l1=Llist()
l1.build(1)
l1.build(2)
l1.build(3)
merge_node=Node(4)
l1.head.next.next.next=merge_node
l1.build(5)
l1.build(6)
l2=Llist()
l2.head=merge_node
l2.build(7)
l2.build(8)
l2.build(9)
l1.build(10)
l1.build(11)
print("List 1")
l1.display()
print("list 2")
l2.display()
merge_point=l1.get_intersection_node(12)
print("Merge point:",merge_point.data if merge_point else "no merge point")



