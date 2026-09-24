# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION

Create a Java program to demonstrate thread synchronization by allowing multiple threads to access a shared resource. Use the synchronized keyword to ensure that only one thread accesses the shared resource at a time.

## AIM

To write a Java program to demonstrate multithreading synchronization using the synchronized keyword and ensure that multiple threads access a shared resource safely.

## ALGORITHM
Start the program.
Create a shared resource class containing a synchronized method.
Define a method to display or update the shared resource.
Create a thread class that accesses the shared resource.
Create multiple thread objects using the same shared resource.
Start all the threads.
Use the synchronized keyword to allow only one thread to access the shared method at a time.
Display the execution of each thread.
Wait for all threads to complete using join().
Stop the program.
   
## PROGRAM:
 ```
/*
Program to implement thread synchronization using Java
Developed by: Santha Ramanath M
RegisterNumber: 212223220097
*/
```

## SOURCE CODE:
```


class SharedResource {

    synchronized void display(String threadName) {
        System.out.println(threadName + " entered the synchronized method.");

        for (int i = 1; i <= 3; i++) {
            System.out.println(threadName + " : " + i);

            try {
                Thread.sleep(500);
            } catch (InterruptedException e) {
                System.out.println(e);
            }
        }

        System.out.println(threadName + " exited the synchronized method.");
    }
}

class MyThread extends Thread {

    SharedResource resource;

    MyThread(SharedResource resource, String name) {
        super(name);
        this.resource = resource;
    }

    public void run() {
        resource.display(getName());
    }
}

public class Main {

    public static void main(String[] args) {

        SharedResource resource = new SharedResource();

        MyThread t1 = new MyThread(resource, "Thread-1");
        MyThread t2 = new MyThread(resource, "Thread-2");
        MyThread t3 = new MyThread(resource, "Thread-3");

        t1.start();
        t2.start();
        t3.start();

        try {
            t1.join();
            t2.join();
            t3.join();
        } catch (InterruptedException e) {
            System.out.println(e);
        }

        System.out.println("All threads completed successfully.");
    }
}
```

## OUTPUT:
<img width="1305" height="421" alt="image" src="https://github.com/user-attachments/assets/eeb88f1e-f93f-45dd-834f-83000f671341" />

## RESULT:
The Java program was executed successfully. Thread synchronization was implemented using the synchronized keyword, ensuring that multiple threads accessed the shared resource one at a time without simultaneous execution of the synchronized method.
