package adivinanumero;

/**
 *
 * @author carlo
 */
import java.util.Scanner;
import java.util.Random;

public class Adivinanumero {
    public static void main(String[] args) {
        try (Scanner scanner = new Scanner(System.in)) {
            Random random = new Random();
            int numeroSecreto = random.nextInt(100) + 1;
            int intentos = 10;
            boolean acertado = false;
            
            System.out.println("Bienvenido al juego de adivinar el numero!");
            System.out.println("He generado un numero entre 1 y 100. Intenta adivinarlo!");
            
            while (intentos > 0 && !acertado) {
                System.out.print("Introduce un numero: ");
                int numeroUsuario = scanner.nextInt();
                
                if (numeroUsuario == numeroSecreto) {
                    acertado = true;
                    System.out.println("Felicidades Has adivinado el numero en " + (11 - intentos) + " intentos.");
                } else if (numeroUsuario < numeroSecreto) {
                    intentos--;
                    System.out.println("El numero es mayor. Intentos restantes: " + intentos);
                } else {
                    intentos--;
                    System.out.println("El numero es menor. Intentos restantes: " + intentos);
                }
            }
            
            if (!acertado) {
                System.out.println("Lo siento, te has quedado sin intentos. El numero era: " + numeroSecreto);
            }
        }
    }
}
