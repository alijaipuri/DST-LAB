class QueueUsingTwoStacks:
    def __init__(self):
        self.stack_in = []  
        self.stack_out = []  

    def enqueue(self, value):
        self.stack_in.append(value)

    def dequeue(self):
        if not self.stack_out:
            while self.stack_in:
                self.stack_out.append(self.stack_in.pop())
        if self.stack_out:
            self.stack_out.pop()

    def peek(self):
        if not self.stack_out:
            while self.stack_in:
                self.stack_out.append(self.stack_in.pop())
        if self.stack_out:
            return self.stack_out[-1]

if __name__ == "__main__":
    q = QueueUsingTwoStacks()
    n = int(input())  
    for _ in range(n):
        query = input().split()
        command = int(query[0])
        if command == 1:
            value = int(query[1])
            q.enqueue(value)
        elif command == 2:
            q.dequeue()
        elif command == 3:
            print(q.peek())
