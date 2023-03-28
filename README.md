# 2023OOP
OOP객체지향
class Program
    {
        static void Main(string[] args)
        {
            Stack a = new Stack();

            a.Push(1);
            a.Push(2);
            a.Push(3);

            while (a.GetStackPointer() != -1)
            {
                Console.WriteLine(a.Pop());
            }

            Console.ReadLine();
        }
    }

    class Stack
    {
        private int[] stack;
        private int sp = -1;
        public Stack()
        {
            stack = new int[100];           
        }
        public Stack(int size)
        {
            stack = new int[size];
        }
       
        public void Push(int data)
        {
            stack[++sp] = data;
        }

        public int Pop()
        {
            return stack[sp--];
        }

        public int GetStackPointer()
        {
            return sp;
        }
    }
