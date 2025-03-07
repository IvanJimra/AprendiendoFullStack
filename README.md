📚 Glosario Completo de POO, Bases de Datos, GIT, SCRUM, Spring Boot y Angular
🧩 1. Conceptos Básicos de Programación
📌 1.1. Tipos de Variables
Definición: Las variables son contenedores que almacenan datos en memoria. En Java, los tipos de variables se dividen en:

Tipos Primitivos:

int: Números enteros (ej: int edad = 25;).

double: Números decimales (ej: double precio = 19.99;).

boolean: Valores booleanos (true o false).

char: Un solo carácter (ej: char letra = 'A';).

Tipos de Referencia:

String: Cadena de caracteres (ej: String nombre = "Juan";).

Array: Arreglo de elementos (ej: int[] numeros = {1, 2, 3};).

Objetos: Instancias de clases (ej: Alumno alumno1 = new Alumno();).

🔄 1.2. Ciclos y Condiciones
Ciclos:

For: Repite un bloque de código un número específico de veces.

java
Copy
for (int i = 0; i < 5; i++) {
    System.out.println("Iteración: " + i);
}
While: Repite un bloque de código mientras una condición sea verdadera.

java
Copy
int i = 0;
while (i < 5) {
    System.out.println("Iteración: " + i);
    i++;
}
Do-While: Similar al while, pero ejecuta el bloque al menos una vez.

java
Copy
int i = 0;
do {
    System.out.println("Iteración: " + i);
    i++;
} while (i < 5);
Condiciones:

If-Else: Ejecuta un bloque de código si una condición es verdadera, de lo contrario, ejecuta otro.

java
Copy
if (edad >= 18) {
    System.out.println("Mayor de edad");
} else {
    System.out.println("Menor de edad");
}
Switch: Evalúa una variable y ejecuta diferentes bloques de código según su valor.

java
Copy
switch (dia) {
    case 1: System.out.println("Lunes"); break;
    case 2: System.out.println("Martes"); break;
    default: System.out.println("Día no válido");
}
🛠️ 1.3. Funciones
Definición: Un bloque de código que realiza una tarea específica. Puede recibir parámetros y devolver un valor.

Sintaxis:

java
Copy
public int sumar(int a, int b) {
    return a + b;
}
Procedimientos: Son funciones que no devuelven ningún valor (void).

java
Copy
public void saludar(String nombre) {
    System.out.println("Hola, " + nombre);
}
🔗 1.4. Operadores Lógicos
Definición: Se utilizan para combinar o negar expresiones booleanas.

AND (&&): Devuelve true si ambas expresiones son verdaderas.

java
Copy
if (edad > 18 && tieneLicencia) {
    System.out.println("Puede conducir");
}
OR (||): Devuelve true si al menos una expresión es verdadera.

java
Copy
if (esEstudiante || esProfesor) {
    System.out.println("Acceso permitido");
}
NOT (!): Niega una expresión.

java
Copy
if (!esFinDeSemana) {
    System.out.println("Es día laboral");
}
🧬 2. Programación Orientada a Objetos (POO)
🏗️ 2.1. Clase
Definición: Es una plantilla que define las propiedades (atributos) y comportamientos (métodos) de un objeto.

Ejemplo:

java
Copy
public class Coche {
    String marca;
    String color;
    
    void arrancar() {
        System.out.println("El coche está arrancando.");
    }
}
🎯 2.2. Objeto
Definición: Es una instancia de una clase. Representa una entidad específica con sus propios valores para los atributos.

Ejemplo:

java
Copy
Coche miCoche = new Coche();
miCoche.marca = "Toyota";
miCoche.color = "Rojo";
miCoche.arrancar();
🔒 2.3. Encapsulamiento
Definición: Consiste en ocultar los detalles internos de un objeto y permitir el acceso a sus datos solo a través de métodos (getters y setters).

Ejemplo:

java
Copy
public class Alumno {
    private String nombre;
    
    public String getNombre() {
        return nombre;
    }
    
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
}
🧬 2.4. Herencia
Definición: Es un mecanismo que permite crear una nueva clase a partir de una clase existente. La nueva clase hereda los atributos y métodos de la clase base.

Tipos de Herencia:

Simple: Una clase hereda de una sola clase base.

java
Copy
public class Animal {
    void comer() {
        System.out.println("El animal está comiendo.");
    }
}

public class Perro extends Animal {
    void ladrar() {
        System.out.println("Guau guau");
    }
}
Multinivel: Una clase hereda de otra clase que a su vez hereda de otra.

java
Copy
public class Vehiculo {
    void mover() {
        System.out.println("El vehículo se está moviendo.");
    }
}

public class Coche extends Vehiculo {
    void arrancar() {
        System.out.println("El coche está arrancando.");
    }
}
Jerárquica: Varias clases heredan de una misma clase base.

java
Copy
public class Animal {
    void comer() {
        System.out.println("El animal está comiendo.");
    }
}

public class Perro extends Animal {
    void ladrar() {
        System.out.println("Guau guau");
    }
}

public class Gato extends Animal {
    void maullar() {
        System.out.println("Miau");
    }
}
🎭 2.5. Polimorfismo
Definición: Es la capacidad de un objeto de tomar muchas formas. Permite que un método se comporte de manera diferente según el objeto que lo invoque.

Tipos de Polimorfismo:

Sobrecarga de Métodos: Múltiples métodos con el mismo nombre pero diferentes parámetros.

java
Copy
public int sumar(int a, int b) {
    return a + b;
}

public double sumar(double a, double b) {
    return a + b;
}
Sobrescritura de Métodos: Una clase hija redefine un método de la clase padre.

java
Copy
public class Animal {
    void hacerSonido() {
        System.out.println("Sonido genérico");
    }
}

public class Perro extends Animal {
    @Override
    void hacerSonido() {
        System.out.println("Guau guau");
    }
}
🎨 2.6. Abstracción
Definición: Es el proceso de ocultar los detalles complejos y mostrar solo la funcionalidad esencial. Se logra mediante clases abstractas e interfaces.

Ejemplo:

java
Copy
public abstract class Vehiculo {
    public abstract void mover();
}
📜 2.7. Interfaces
Definición: Es una plantilla que define un conjunto de métodos que una clase debe implementar.

Ejemplo:

java
Copy
public interface Volador {
    void volar();
}
📦 2.8. Listas y HashMap
Listas: Colecciones dinámicas de elementos del mismo tipo.

java
Copy
List<String> nombres = new ArrayList<>();
nombres.add("Juan");
HashMap: Colección de pares clave-valor.

java
Copy
HashMap<String, Integer> edades = new HashMap<>();
edades.put("Juan", 25);
⚠️ 2.9. Excepciones
Definición: Mecanismo para manejar errores en tiempo de ejecución.

Ejemplo:

java
Copy
try {
    int resultado = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Error: División por cero");
}
🗃️ 3. Conceptos Avanzados de Bases de Datos
⚙️ 3.1. Triggers
Definición: Son procedimientos almacenados que se ejecutan automáticamente cuando ocurre un evento específico (INSERT, UPDATE, DELETE) en una tabla.

Ejemplo:

sql
Copy
CREATE TRIGGER before_insert_alumno
BEFORE INSERT ON Alumnos
FOR EACH ROW
BEGIN
    SET NEW.fecha_creacion = NOW();
END;
🔢 3.2. Secuencias
Definición: Son objetos que generan valores numéricos secuenciales, útiles para crear claves primarias autoincrementales.

Ejemplo:

sql
Copy
CREATE SEQUENCE seq_alumno
START WITH 1
INCREMENT BY 1;
📝 3.3. Procedimientos Almacenados
Definición: Son bloques de código SQL que se almacenan en la base de datos y se pueden ejecutar cuando sea necesario.

Ejemplo:

sql
Copy
CREATE PROCEDURE obtener_alumnos()
BEGIN
    SELECT * FROM Alumnos;
END;
👁️ 3.4. Vistas (Views)
Definición: Son consultas SQL almacenadas que actúan como tablas virtuales.

Ejemplo:

sql
Copy
CREATE VIEW vista_alumnos AS
SELECT nombre, edad FROM Alumnos WHERE edad > 18;
🛠️ 4. Control de Versiones (GIT)
📂 4.1. GIT
Definición: Es un sistema de control de versiones distribuido que permite rastrear cambios en el código fuente.

Funcionalidad Principal: Mantener un registro de toda la historia de los cambios en los archivos de un proyecto.

Ejemplo: Un desarrollador usa GIT para gestionar las versiones de un proyecto, permitiendo revertir cambios o colaborar con otros desarrolladores.

⌨️ 4.2. Comandos Básicos de GIT
git init: Inicializa un repositorio GIT en un directorio.

git add: Añade cambios al área de preparación (staging area).

git commit: Guarda los cambios en el repositorio local con un mensaje descriptivo.

git push: Sube los cambios al repositorio remoto.

git pull: Obtiene cambios del repositorio remoto y los fusiona con el repositorio local.

🌐 4.3. GitHub
Definición: Es un servicio basado en la web para alojar repositorios GIT. Permite a los desarrolladores colaborar en proyectos, revisar código y proponer cambios.

Diferencia entre GIT y GitHub:

GIT: Es el sistema de control de versiones.

GitHub: Es una plataforma que aloja repositorios GIT y ofrece herramientas adicionales para colaboración.

🏃 5. Metodología SCRUM
🎯 5.1. ¿Qué es SCRUM?
Definición: Es una metodología ágil para el desarrollo de proyectos, especialmente software. Se basa en un enfoque iterativo e incremental, donde el trabajo se divide en ciclos cortos llamados sprints.

Objetivo: Mejorar la eficacia en proyectos complejos e inciertos.

Ejemplo: Un equipo de desarrollo trabaja en un proyecto de software en sprints de 2 semanas, entregando incrementos funcionales al final de cada sprint.

👥 5.2. Roles en SCRUM
Scrum Master: Es el líder del proyecto y se encarga de asegurar que se sigan las prácticas SCRUM. También ayuda a resolver impedimentos.

Product Owner: Es el responsable del producto y define las funcionalidades que deben ser desarrolladas. Prioriza el trabajo en el Product Backlog.

Equipo de Desarrollo: Es el grupo de profesionales que lleva a cabo el trabajo técnico para desarrollar el producto.

🗓️ 5.3. Ceremonias de SCRUM
Planificación del Sprint: Reunión donde el equipo selecciona las tareas del Product Backlog para el próximo sprint.

Revisión del Sprint: Al final del sprint, el equipo demuestra el trabajo completado al Product Owner y otros interesados.

Retrospectiva del Sprint: El equipo reflexiona sobre el sprint anterior y decide cómo mejorar en el próximo.

🏁 5.4. Sprint
Definición: Es un ciclo de trabajo con una duración fija (generalmente de 1 a 4 semanas). Durante el sprint, el equipo trabaja en las tareas seleccionadas para entregar un incremento usable del producto.

Ejemplo: Un equipo de desarrollo trabaja en un sprint de 2 semanas para implementar nuevas funcionalidades en una aplicación web.

🖥️ 6. Arquitectura Cliente-Servidor, Spring Boot y Angular
🌐 6.1. Arquitectura Cliente-Servidor
Definición: Es un modelo de diseño de software donde dos componentes interactúan: el cliente (frontend) y el servidor (backend). El cliente solicita servicios y el servidor los proporciona.

Ejemplo: Un navegador web (cliente) solicita una página web a un servidor, que responde con los datos necesarios.

🍃 6.2. Spring Boot
Definición: Es un framework de Java que simplifica el desarrollo de aplicaciones basadas en Spring. Proporciona una configuración automática y permite crear aplicaciones listas para producción rápidamente.

Ventajas: Configuración automática, integración con otras tecnologías (como Hibernate), y facilidad para crear APIs REST.

⚙️ 6.3. Angular
Definición: Es un framework de JavaScript (TypeScript) para desarrollar aplicaciones web del lado del cliente (frontend). Permite crear aplicaciones SPA (Single Page Applications).

Ventajas: Modularidad, enlace de datos bidireccional, y facilidad para crear interfaces dinámicas.

📂 Opciones para Subir los Ejemplos
Markdown (README.md): Puedes subir este contenido directamente a un archivo README.md en GitHub.

Archivo de Texto (TXT): Puedes guardar este contenido en un archivo .txt y subirlo a GitHub.

Archivo de Documento (PDF): Puedes convertir este contenido a PDF y subirlo a GitHub.

Archivo de Código (Java, SQL, etc.): Puedes crear archivos .java, .sql, etc., con los ejemplos de código y subirlos a GitHub.

