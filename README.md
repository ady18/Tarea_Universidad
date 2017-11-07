# Tarea_Universidad
/*
 * Utilizando C++, declara un vector de 10 posiciones que acepte valores  numéricos.
 * A través de la consola, solicita la captura de dichos valores.
 * Muestra en la pantalla el número menor de los valores capturados e indica la 
 * posición del mismo dentro del vector.
 */
package tarea_4;
import java.util.*;
/**
 *
 * @author Adirane
 */
public class Tarea_4 {
    public static void main(String[] args) {
        
        Scanner teclado = new Scanner(System.in); //Objeto de lectura desde el teclado
        int [] valores = new int[10]; //Arreglo de 10 elementos
        int valor_menor; //Variable para declarar el menor valor introducido por el usuario
        System.out.println("Ingresa los valores: "); //Mensaje en consola
        
        //Recorre el arreglo
        //Para i igual a cero, i menor que 10, i se incrementa en 1
        for(int i=0; i < 10; i++){
            System.out.print("Valor [" + (i+1) + "]: " ); //Imprime en consola pidiendo al usuario el valor correspondiente
            valores[i] = teclado.nextInt(); //Almacena el valor en el arreglo
        }

        valor_menor = valores[0]; //La variable es igual al arreglo  en la posición 0
        
        //Lee el arreglo
        //Para j=1 por cuenta que el arreglo está declarado en la posición 0, j menor que 10, j se incrementa
        for(int j=1; j < 10; j++){
            if(valores[j] < valor_menor){ //Si valores en la posición j es menor que valor_menor
                valor_menor = valores[j]; //valor_menor es igual al arreglo en cada posición de j hasta 10
                
                //Imprime en consola el menor valor introducido por el usuario                
                System.out.println("El menor número es " + valor_menor 
                        + " y está en la posición " + (j+1) + " del arreglo");
            }
        }
    }
    
}
