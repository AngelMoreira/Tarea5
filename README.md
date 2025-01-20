# Tarea5
// Clase Padre
class Vehiculo {
    // Atributos comunes
    protected String marca;
    protected String modelo;
    protected int año;

    // Constructor
    public Vehiculo(String marca, String modelo, int año) {
        this.marca = marca;
        this.modelo = modelo;
        this.año = año;
    }

    // Métodos comunes
    public void encender() {
        System.out.println("El vehículo está encendido");
    }

    public void apagar() {
        System.out.println("El vehículo está apagado");
    }
}

// Clase Hija: Auto
class Auto extends Vehiculo {
    private int numeroPuertas;

    // Constructor
    public Auto(String marca, String modelo, int año, int numeroPuertas) {
        super(marca, modelo, año);
        this.numeroPuertas = numeroPuertas;
    }

    // Método adicional
    public void abrirMaletero() {
        System.out.println("El maletero está abierto");
    }
}

// Clase Hija: Motocicleta
class Motocicleta extends Vehiculo {
    private String tipoCasco;

    // Constructor
    public Motocicleta(String marca, String modelo, int año, String tipoCasco) {
        super(marca, modelo, año);
        this.tipoCasco = tipoCasco;
    }

    // Método adicional
    public void hacerCaballito() {
        System.out.println("La motocicleta está haciendo un caballito");
    }
}

// Clase Hija: Camión
class Camion extends Vehiculo {
    private int capacidadCarga;

    // Constructor
    public Camion(String marca, String modelo, int año, int capacidadCarga) {
        super(marca, modelo, año);
        this.capacidadCarga = capacidadCarga;
    }

    // Método adicional
    public void descargar() {
        System.out.println("El camión está descargando");
    }
}

// Clase Principal (Main)
public class Main {
    public static void main(String[] args) {
        // Crear objetos de Auto
        Auto auto1 = new Auto("Toyota", "Corolla", 2020, 4);
        Auto auto2 = new Auto("Honda", "Civic", 2022, 4);

        // Crear objetos de Motocicleta
        Motocicleta moto1 = new Motocicleta("Yamaha", "R15", 2021, "Integral");
        Motocicleta moto2 = new Motocicleta("Suzuki", "GSX", 2023, "Abierto");

        // Crear objetos de Camión
        Camion camion1 = new Camion("Volvo", "FH16", 2019, 20000);
        Camion camion2 = new Camion("Scania", "R500", 2021, 25000);

        // Llamar a métodos de Auto
        System.out.println("Auto 1:");
        auto1.encender();
        auto1.abrirMaletero();
        auto1.apagar();

        System.out.println("Auto 2:");
        auto2.encender();
        auto2.abrirMaletero();
        auto2.apagar();

        // Llamar a métodos de Motocicleta
        System.out.println("Motocicleta 1:");
        moto1.encender();
        moto1.hacerCaballito();
        moto1.apagar();

        System.out.println("Motocicleta 2:");
        moto2.encender();
        moto2.hacerCaballito();
        moto2.apagar();

        // Llamar a métodos de Camión
        System.out.println("Camión 1:");
        camion1.encender();
        camion1.descargar();
        camion1.apagar();

        System.out.println("Camión 2:");
        camion2.encender();
        camion2.descargar();
        camion2.apagar();
    }
}
