# Java
1
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("a = \n");
        int a = scanner.nextInt();
        System.out.println("b = \n");
        int b = scanner.nextInt();
        System.out.println("c = \n");
        int c = scanner.nextInt();
        int z = ((a -3) * b / 2) + c;
        System.out.println("z = "+ z);
    }
}

2

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("a = \n");
        int a = scanner.nextInt();
        System.out.println("b = \n");
        int b = scanner.nextInt();
        System.out.println("c = \n");
        int c = scanner.nextInt();
        double x = (b + Math.sqrt(Math.pow(b, 2) + 4 * a * c)) / (2 * a) - Math.pow(a, 3) * c + Math.pow(b, -2) ;
        System.out.println("ответ: "+ x);
    }
}

3

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("x = \n");
        int x = scanner.nextInt();
        System.out.println("y = \n");
        int y = scanner.nextInt();
        double a = (Math.sin(x)+Math.cos(y))/(Math.cos(x) - Math.sin(y)) * Math.tan(x * y) ;
        System.out.println("ответ: "+ a);
    }
}

4

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Введите nnn.ddd: ");
        double s = scanner.nextDouble();

        int integerPart = (int) s;
        double fractionalPart = s - integerPart;

        double reversedNumber = (fractionalPart * 1000) + (integerPart / 1000.0);

        System.out.println("Полученное значение числа: " + reversedNumber);
    }
}

5

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Введите значение длительности времени в секундах: ");
        int T = scanner.nextInt();

        int hours = T / 3600;
        int minutes = (T % 3600) / 60; 
        int seconds = (T % 3600) % 60; 
        System.out.printf("%02dч %02dмин %02dс", hours, minutes, seconds);
    }
}

6
 
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("x = ");
        int x = scanner.nextInt();
        System.out.print("y = ");
        int y = scanner.nextInt();
        if(x >= -2 && x <= 2 && y >= 0 && y <= 4 || x >= -4 && x <= 4 && y <= 0 && y >= -3) {
            System.out.println("true");
        }
        else{
            System.out.println("false");
        }
    }
}

1

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("1 угол: ");
        double angle1 = scanner.nextDouble();

        System.out.print("2 угол: ");
        double angle2 = scanner.nextDouble();

        double angle3 = 180 - angle1 - angle2;

        if (angle1 > 0 && angle2 > 0 && angle3 > 0) {
            System.out.println("Треугольник существует.");

            if (angle1 == 90 || angle2 == 90 || angle3 == 90) { // проверка на прямоугольность треугольника
                System.out.println("Треугольник прямоугольный.");
            } else {
                System.out.println("Треугольник не прямоугольный.");
            }
        } else {
            System.out.println("Треугольник не существует.");
        }
    }
}

2

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("a: ");
        int a = scanner.nextInt();

        System.out.print("b: ");
        int b = scanner.nextInt();

        System.out.print("c: ");
        int c = scanner.nextInt();

        System.out.print("d: ");
        int d = scanner.nextInt();

        int min1 = Math.min(a, b);
        int min2 = Math.min(c, d);
        int result = Math.max(min1, min2);

        System.out.println("max[min(a, b), min(c, d)] = " + result);
    }
}

3

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("координаты точки A:");
        System.out.print("x1 = ");
        int x1 = scanner.nextInt();
        System.out.print("y1 = ");
        int y1 = scanner.nextInt();

        System.out.println("координаты точки B:");
        System.out.print("x2 = ");
        int x2 = scanner.nextInt();
        System.out.print("y2 = ");
        int y2 = scanner.nextInt();

        System.out.println("координаты точки C:");
        System.out.print("x3 = ");
        int x3 = scanner.nextInt();
        System.out.print("y3 = ");
        int y3 = scanner.nextInt();

        double slopeAB = (double) (y2 - y1) / (x2 - x1); //  угловой коэффициент
        double slopeBC = (double) (y3 - y2) / (x3 - x2);

        if (slopeAB == slopeBC) {
            System.out.println("Точки A, B и C лежат на одной прямой.");
        } else {
            System.out.println("Точки A, B и C не лежат на одной прямой.");
        }
    }
}

4

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Введите размеры прямоугольного отверстия:");
        System.out.print("A = ");
        int A = scanner.nextInt();
        System.out.print("B = ");
        int B = scanner.nextInt();

        System.out.println("Введите размеры кирпича:");
        System.out.print("x = ");
        int x = scanner.nextInt();
        System.out.print("y = ");
        int y = scanner.nextInt();
        System.out.print("z = ");
        int z = scanner.nextInt();

        if ((x <= A && y <= B) || (x <= B && y <= A) ||
                (x <= A && z <= B) || (x <= B && z <= A) ||
                (y <= A && z <= B) || (y <= B && z <= A)) {
            System.out.println("Кирпич пройдет через отверстие.");
        } else {
            System.out.println("Кирпич не пройдет через отверстие.");
        }
    }
}

5

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите значение x: ");
        double x = scanner.nextDouble();

        double result;
        if (x <= 3) {
            result = Math.pow(x, 2) - 3 * x + 9;
        } else {
            result = 1 / (Math.pow(x, 3) + 6);
        }

        System.out.println("Значение функции F(x) = " + result);
    }
}

1

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите целое положительное число: ");
        int number = scanner.nextInt();

        int sum = 0;
        for (int i = 1; i <= number; i++) {
            sum += i;
        }

        System.out.println("Сумма чисел от 1 до " + number + " равна " + sum);
    }
}

2

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите начало отрезка a: ");
        double a = scanner.nextDouble();

        System.out.print("Введите конец отрезка b: ");
        double b = scanner.nextDouble();

        System.out.print("Введите шаг h: ");
        double h = scanner.nextDouble();

        for (double x = a; x <= b; x += h) {
            double y;
            if (x > 2) {
                y = x;
            } else {
                y = -x;
            }
            System.out.println("Значение функции Y при x = " + x + ": " + y);
        }
    }
}

3

public class Main {
    public static void main(String[] args) {
        long sum = 0;
        for (int i = 1; i <= 100; i++) {
            sum += (long) i * i;
        }

        System.out.println("Сумма квадратов первых ста чисел: " + sum);
    }
}

4

import java.math.BigInteger;

public class Main {
    public static void main(String[] args) {
        BigInteger product = BigInteger.ONE;
        for (int i = 1; i <= 200; i++) {
            BigInteger square = BigInteger.valueOf(i).pow(2);
            product = product.multiply(square);
        }

        System.out.println("Произведение квадратов первых двухсот чисел: " + product);
    }
}

6

public class Main {
    public static void main(String[] args) {
        for (char c = 0; c < 128; c++) {
            System.out.println("Символ: " + c + ", Численное обозначение: " + (int) c);
        }
    }
}

7

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите начало промежутка m: ");
        int m = scanner.nextInt();

        System.out.print("Введите конец промежутка n: ");
        int n = scanner.nextInt();

        for (int num = m; num <= n; num++) {
            System.out.print("Делители числа " + num + ": ");
            for (int i = 2; i < num; i++) {
                if (num % i == 0) {
                    System.out.print(i + " ");
                }
            }
            System.out.println();
        }
    }
}

8

import java.util.HashSet;
import java.util.Scanner;
import java.util.Set;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите первое число: ");
        int number1 = scanner.nextInt();

        System.out.print("Введите второе число: ");
        int number2 = scanner.nextInt();

        Set<Integer> digits1 = getDigits(number1);
        Set<Integer> digits2 = getDigits(number2);

        Set<Integer> commonDigits = new HashSet<>(digits1);
        commonDigits.retainAll(digits2);

        System.out.println("Цифры, входящие в запись обоих чисел: " + commonDigits);
    }

    private static Set<Integer> getDigits(int number) {
        Set<Integer> digits = new HashSet<>();
        while (number != 0) {
            int digit = number % 10;
            digits.add(digit);
            number /= 10;
        }
        return digits;
    }
}


