
# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to write a string to a text file named output.txt.

## AIM:
To write a Java program to write a string into a text file named output.txt.

## ALGORITHM :
1. Start the program.
2. Import the FileWriter class.
3. Create a FileWriter object for output.txt.
4. Write a string into the file using the write() method.
5. Close the file using the close() method.
6. Display a success message.
7. End the program.
   
## PROGRAM:
 ```
/*
Program to implement file writing using Java
Developed by: Santha Ramanath M
RegisterNumber:  212223220097
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;

public class WriteToFileExample 
{
    public static void main(String[] args) 
    {
        String content = "This is the text to write to the file.";

        try (FileWriter writer = new FileWriter("output.txt")) 
        {
            writer.write(content);
            System.out.println("Successfully wrote to the file.");
        } 
        catch (IOException e)
        {
            System.out.println("An error occurred while writing to the file: " + e.getMessage());
        }
    }
}
```

## OUTPUT:
<img width="1294" height="268" alt="image" src="https://github.com/user-attachments/assets/2f176597-698a-4eab-8389-82b818ecba05" />

## RESULT:
The Java program was executed successfully and the string was written into the output.txt file successfully.
