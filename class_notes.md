# Class Notes

## A Stack

``` Ruby
#we want to hide the ability to see the secret codes with a inspector method

class Stack
    def initialize
        @secret_codes = []
    end

    def push(value)
        secret_codes << value
        returns self
    end

    def pop
        secre_code.pop
    end

    def peek
        secret_codes.last
    end

    def size
        secret_codes.length
    end

    def empty?
        secret_codes.empty?
    end

    def inspect
        "#<Stack:#{self.object_id}>"
    end
    private
    attr_reader :secret_codes
end

```

## MyQueue

```Ruby

#here we dont have a inspector because its not part of our rules to not let us see the the queue i.e we dont care if they see it.

class MyQueue
    def initialize
        @inner_array = []
    end

    def enqueue(el)
        inner_array.push(el)
    end

    def  dequeue
        inner_array.shift
    end

    def show
        inner_array.dup
    end

    def empty?
        inner_array.empty?
    end



    private
    attr_reader :inner_array

end
```

## Trees

```Ruby

class Node
    attr_reader :value, :children
    def initialize(valye, children = [])
        @value = value
        @children = children
    end

    def children_values
        @children.map { |child| child.value}
    end



end

d = Node.new('d')
e = Node.new('e')
f = Node.new('f')
g = Node.new('g')
b = Node.new('b', [d,e])
c = Node.new('b', [f,g])
a = Node.new('b', [b,c])

```

![[Pasted image 20230519104116.png]]

## Traversing Through a Tree

For tree traversal you can use BFS which will check all the nodes at each level which is very helpful when your tree is very wide but not very long.
Also for **BFS** you dont need to use recursion which will use less memory.

When using DFS you're using recursion and this methodology is much better when your tree is very long but not wide. This is not to say DFS is better than BFS but its a different strategy to solving the problem at hand. **DFS** uses a lot more memory becaus it is stack dependant unlike **BFS**.
