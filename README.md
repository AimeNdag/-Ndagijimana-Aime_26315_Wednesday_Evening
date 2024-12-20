1.IOException

import java.io.*;



public class IOExceptionExample {

    public static void main(String[] args) {

        try {

            BufferedReader reader = new BufferedReader(new FileReader("nonexistentfile.txt"));

            reader.readLine();

        } catch (IOException e) {

            System.out.println("IOException occurred: " + e.getMessage());

        }

    }

}
2. FileNotFoundException

import java.io.*;



public class FileNotFoundExceptionExample {

    public static void main(String[] args) {

        try {

            FileInputStream file = new FileInputStream("nonexistentfile.txt");

        } catch (FileNotFoundException e) {

            System.out.println("FileNotFoundException occurred: " + e.getMessage());

        }

    }

}

3. EOFException

import java.io.*;



public class EOFExceptionExample {

    public static void main(String[] args) {

        try {

            DataInputStream input = new DataInputStream(new FileInputStream("example.txt"));

            while(true) {

                System.out.println(input.readUTF());

            }

        } catch (EOFException e) {

            System.out.println("EOFException occurred: End of file reached.");

        } catch (IOException e) {

            System.out.println("IOException occurred: " + e.getMessage());

        }

    }

}

4. SQLException

import java.sql.*;



public class SQLExceptionExample {

    public static void main(String[] args) {

        try {

            Connection conn = DriverManager.getConnection("jdbc:invalid-url", "user", "password");

        } catch (SQLException e) {

            System.out.println("SQLException occurred: " + e.getMessage());

        }

    }

}

5. ClassNotFoundException

public class ClassNotFoundExceptionExample {

    public static void main(String[] args) {

        try {

            Class.forName("com.nonexistent.Class");

        } catch (ClassNotFoundException e) {

            System.out.println("ClassNotFoundException occurred: " + e.getMessage());

        }

    }

}

6. ArithmeticException

public class ArithmeticExceptionExample {

    public static void main(String[] args) {

        try {

            int result = 10 / 0;

        } catch (ArithmeticException e) {

            System.out.println("ArithmeticException occurred: " + e.getMessage());

        }

    }

}

7. NullPointerException

public class NullPointerExceptionExample {

    public static void main(String[] args) {

        try {

            String str = null;

            str.length();

        } catch (NullPointerException e) {

            System.out.println("NullPointerException occurred: " + e.getMessage());

        }

    }

}

8. ArrayIndexOutOfBoundsException

public class ArrayIndexOutOfBoundsExceptionExample {

    public static void main(String[] args) {

        try {

            int[] array = new int[5];

            int number = array[10];

        } catch (ArrayIndexOutOfBoundsException e) {

            System.out.println("ArrayIndexOutOfBoundsException occurred: " + e.getMessage());

        }

    }

}

9. ClassCastException

public class ClassCastExceptionExample {

    public static void main(String[] args) {

        try {

            Object x = new Integer(0);

            System.out.println((String)x);

        } catch (ClassCastException e) {

            System.out.println("ClassCastException occurred: " + e.getMessage());

        }

    }

}

10. IllegalArgumentException

public class IllegalArgumentExceptionExample {

    public static void main(String[] args) {

        try {

            Thread t = new Thread();

            t.setPriority(100);

        } catch (IllegalArgumentException e) {

            System.out.println("IllegalArgumentException occurred: " + e.getMessage());

        }

    }

}

11. NumberFormatException

public class NumberFormatExceptionExample {

    public static void main(String[] args) {

        try {

            int num = Integer.parseInt("XYZ");

        } catch (NumberFormatException e) {

            System.out.println("NumberFormatException occurred: " + e.getMessage());

        }

    }

}



