# NUMEROPRIMO
NUMERO ENTERO
    import java.util.Scanner;

public class NumeroPrimo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Solicitar al usuario un número entero
        System.out.print("Ingresa un número entero: ");
        int numero = scanner.nextInt();
        
        // Verificar si el número es primo
        if (esPrimo(numero)) {
            System.out.println(numero + " es un número primo.");
        } else {
            System.out.println(numero + " no es un número primo.");
        }

        scanner.close();
    }

    // Método que determina si un número es primo
    public static boolean esPrimo(int num) {
        if (num <= 1) {
            return false;
        }

        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                return false; // Tiene un divisor, no es primo
            }
        }
        return true; // No tiene divisores, es primo
    }
}
