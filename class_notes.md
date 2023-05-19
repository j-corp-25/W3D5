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
