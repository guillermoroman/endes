# Diagramas de clases a partir de código

### Ejercicio 1
Observa el código que se muestra a continuación y crea un diagrama de clases que lo respresente:

```java
import java.util.ArrayList;
import java.util.List;

class Vehiculo {
    private String matricula;
    private String modelo;

    public Vehiculo(String matricula, String modelo) {
        this.matricula = matricula;
        this.modelo = modelo;
    }

    public String getMatricula() {
        return matricula;
    }

    public String getModelo() {
        return modelo;
    }
}

class Flota {
    private String nombre;
    private List<Vehiculo> vehiculos;

    public Flota(String nombre) {
        this.nombre = nombre;
        this.vehiculos = new ArrayList<>();
    }

    public void agregarVehiculo(Vehiculo vehiculo) {
        vehiculos.add(vehiculo);
    }

    public List<Vehiculo> getVehiculos() {
        return vehiculos;
    }
}

public class Main {
    public static void main(String[] args) {
        Flota flota = new Flota("Flota Comercial");
        Vehiculo v1 = new Vehiculo("1234ABC", "Toyota Corolla");
        Vehiculo v2 = new Vehiculo("5678DEF", "Ford Focus");

        flota.agregarVehiculo(v1);
        flota.agregarVehiculo(v2);

        System.out.println("Flota creada con " + flota.getVehiculos().size() + " vehículos.");
    }
}
```

### Ejercicio 2
Observa el código que se muestra a continuación y crea un diagrama de clases que lo respresente:

```java
import java.util.ArrayList;
import java.util.List;

class Libro {
    private String titulo;
    private String autor;

    public Libro(String titulo, String autor) {
        this.titulo = titulo;
        this.autor = autor;
    }

    public String getTitulo() {
        return titulo;
    }

    public String getAutor() {
        return autor;
    }
}

class Editorial {
    private String nombre;
    private List<Libro> libros;

    public Editorial(String nombre) {
        this.nombre = nombre;
        this.libros = new ArrayList<>();
    }

    public void publicarLibro(String titulo, String autor) {
        libros.add(new Libro(titulo, autor)); // Se crea dentro de Editorial (composición)
    }

    public List<Libro> getLibros() {
        return libros;
    }
}

public class Main {
    public static void main(String[] args) {
        Editorial editorial = new Editorial("Penguin Books");
        editorial.publicarLibro("1984", "George Orwell");
        editorial.publicarLibro("Cien años de soledad", "Gabriel García Márquez");

        System.out.println("Editorial " + editorial.getLibros().size() + " libros publicados.");
    }
}
```


### Ejercicio 3
Observa el código que se muestra a continuación y crea un diagrama de clases que lo respresente:

```java
import java.util.ArrayList;
import java.util.List;

class Paciente {
    private String nombre;

    public Paciente(String nombre) {
        this.nombre = nombre;
    }

    public String getNombre() {
        return nombre;
    }
}

class Medico {
    private String nombre;
    private List<Paciente> pacientes;

    public Medico(String nombre) {
        this.nombre = nombre;
        this.pacientes = new ArrayList<>();
    }

    public void agregarPaciente(Paciente paciente) {
        pacientes.add(paciente);
    }

    public List<Paciente> getPacientes() {
        return pacientes;
    }

    public String getNombre() {
        return nombre;
    }
}

public class Main {
    public static void main(String[] args) {
        Medico medico1 = new Medico("Dr. Rodríguez");
        Paciente paciente1 = new Paciente("Juan Pérez");
        Paciente paciente2 = new Paciente("María López");

        medico1.agregarPaciente(paciente1);
        medico1.agregarPaciente(paciente2);

        System.out.println(medico1.getNombre() + " atiende a " + medico1.getPacientes().size() + " pacientes.");
    }
}
```




