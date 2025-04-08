## Python Program to Insert String Values into a Circular Queue Using Function

## Aim:
To implement a circular queue in Python and create a function to insert string values into it.

## Procedure:

1.Define a class CircularQueue with:

 * Constructor to initialize size, queue, front, and rear.
  
 * enqueue() method to insert a string into the circular queue.
  
 * (Optional) display() method to view current elements in the queue.

2.In enqueue():

 * Check if the queue is full.
  
 * If not, insert the string at the correct position and update rear.

3.Take string input from the user and insert it using the enqueue() function.

4.Display the queue after insertion.

## Program:

```python
class Queue:
    def __init__(self, size):
        self.items = [0] * size
        self.max_size = size
        self.head, self.tail, self.size = 0, 0, 0

    def enqueue(self, item):
        if self.is_list_full():
            print(f'Queue is full')
            return

        #print(f'Inserting {item}')
        self.items[self.tail] = item
        self.tail = (self.tail + 1) % self.max_size
        self.size += 1

    def dequeue(self):
        item = self.items[self.head]
        self.head = (self.head + 1) % self.max_size
        self.size -= 1

        return item

    def is_list_full(self):
        if self.size == self.max_size:
            return True
        return False

    def is_empty(self):
        if self.size == 0:
            return True
        return False

size=int(input())
queue = Queue(size)
str=input()
str1=input()
str2=input()
queue.enqueue(str)
queue.enqueue(str1)
queue.enqueue(str2)  
print(queue.items)
#print(queue.head)
#print(queue.tail)
```
## Output:
![image](https://github.com/user-attachments/assets/25c1d112-7a7a-40cf-95db-7e3560a5d4ab)

## Result:
The program successfully inserts string values into the circular queue and displays the current contents of the queue.

