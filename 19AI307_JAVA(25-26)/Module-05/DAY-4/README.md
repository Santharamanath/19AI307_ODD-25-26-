# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to implement a extending thread class.

## AIM:
To write a Java program to create a thread by extending the Thread class.

## ALGORITHM :
1. Start the program.
2. Create a class that extends the Thread class.
3. Override the run() method.
4. Write the task to be executed inside the run() method.
5. Create an object of the thread class.
6. Call the start() method to start the thread.
7. Display the thread execution message.
8. End the program.
   
## PROGRAM:
 ```
/*
Program to implement multithreading using Thread class in Java
Developed by: Santha Ramanath M
RegisterNumber:  212223220097
*/
```

## SOURCE CODE:
```
class MyThread extends Thread
{
    public void run()
    {
        System.out.println("Thread is running");
    }
}

public class Main
{
    public static void main(String[] args)
    {
        MyThread t = new MyThread();

        t.start();
    }
}
```

## OUTPUT:
<img width="1299" height="394" alt="image" src="https://github.com/user-attachments/assets/a432a51c-eb18-4556-939e-4ea75f498c29" />

## RESULT:
The Java program was executed successfully and the thread was created and executed successfully by extending the Thread class.
