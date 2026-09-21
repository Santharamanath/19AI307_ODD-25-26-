# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Create a program that reads a thread name and a priority (1–10), sets that priority to a new thread, prints both values.
Input:
Two lines: <threadName>, <priority>
Output:
Thread <threadName> priority set to <priority>

## AIM:
To write a Java program to create a thread, set its name and priority, and display the details.

## ALGORITHM :
1. Start the program.
2. Read the thread name and priority from the user.
3. Create a thread object.
4. Set the thread name using setName().
5. Set the thread priority using setPriority().
6. Display the thread name and priority.
7. End the program.
   
## PROGRAM:
 ```
/*
Program to implement thread priority using Java
Developed by: Santha Ramanath M
RegisterNumber:  212223220097
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        int priority = sc.nextInt();

        Thread t = new Thread();

        t.setName(threadName);
        t.setPriority(priority);

        System.out.println("Thread " + t.getName() + " priority set to " + t.getPriority());
    }
}
```

## OUTPUT:
<img width="1305" height="421" alt="image" src="https://github.com/user-attachments/assets/eeb88f1e-f93f-45dd-834f-83000f671341" />

## RESULT:
The Java program was executed successfully and the thread name and priority were set and displayed successfully.
