import java.io.File;
import java.util.Scanner;

public class Ej_completo {
    public static Scanner scan = new Scanner(System.in);
        /*
        *. Escribir un programa en Java que para cualquier ruta indicada por el usuario,muestre:
            - Si el fichero existe o no
            - Si se trata de un directorio o de un fichero
            - En caso de ser un fichero, debe mostrar los siguientes datos:
            o Nombre
            o Tamaño
            o Permisos de lectura y escritura

            2. Partiendo del fichero de csv de ejemplo, crear un programa de Java que muestre los
            datos de todos aquellos restaurantes cuyo código postal empiece por 6.

            3. Partiendo del fichero de csv de ejemplo, crear un programa de Java que permita al
            usuario añadir datos nuevos a ese fichero, utilizando el mismo formato que los ya
            existentes.

            4. Partiendo del fichero de csv de ejemplo, crear un programa de Java que cree una
            copia de ese fichero llamada “Restaurants2.csv” que contenga los mismos datos
            excepto aquellos correspondientes a los restaurantes cuyo código postal empieza por 6.

            5. Crear un programa en Java que borre el fichero cuya ruta ha sido introducida por el
            usuario
        *
        */



    public static void main(String[] args) {

        start();

    }

    public static void start() {
        System.out.println("Introduzca una ruta y le dire si es fichero o directorio o si por el contrario no hay nada");

        String ruta = scan.next();

        File documento = new File(ruta);


        if(documento.exists()){
            System.out.println("El directorio existe");


        }else {
            System.out.println("El directorio no existe");
        }

        if(documento.isFile()){
            System.out.println("Es un fichero");

            System.out.println("El nombre del archivo es: " + documento.getName());
            System.out.println("El tamanio del archivo es: " + documento.getUsableSpace());
            System.out.println("Los permisos del archivo son: " +" leer: "+ documento.canRead() +" escribir: "+ documento.canWrite());

        }else {
            System.out.println("No es un fichero");
            System.out.println("El nombre del archivo es: " + documento.getName());
            System.out.println("El tamanio del archivo es: " + documento.getUsableSpace());
            System.out.println("Los permisos del archivo son: " +" leer: "+ documento.canRead() +" escribir: "+ documento.canWrite());

        }
    }
