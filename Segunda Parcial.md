![alt](http://www.natacionmexico.com/portal/images/eventlist/venues/small/universidad_de_colima_1321220340.jpg)
#   UNIVERSIDAD DE COLIMA
#### Alexis Vladimir Ladino Munguia
#### INGENIERIA EN COMPUTACION INTELIGENTE
#### 3°B
#### FACULTAD DE INGENERIA MECANICA Y ELECTRICA
#### Walter Alexander Mata López
---
Aqui se podran ver mis programas de clase de la segunda parcial
---
### 2.1 Clases y atributos
    class User {//1
  String? nombre;//2
  int? edad; //3
}

void main (List<String> args) {
    User usuario1= User();//4
    print(usuario1);//5
    print(usuario1.nombre);//6
    print(usuario1.edad);//7

}
---
  Class User {
    String nombre = "Alex";
    int edad = 50;
}

void main(List<String>args) {
  User usuario1 = User ();
  print(usuario1.nombre);
  print(usuario1.edad);
}
---
 Class User {
  String nombre = "Alex";
  int edad = 50;
}

void main (List<String> args) {
  User usuario1 = User();
  User usuario2 = User();

  print(usuario1.nombre);
  print(usuario1.edad);
  print(usuario2.nombre); 
  print(usuario2.edad);
}
---
  Class User {
  String? nombre;
  int? edad;
}

void main(List<String> args){
  User usuario1= User();
  var usuario2 = User();

  usuario1.nombre = "Alex";
  usuario1.edad = 50;
  usuario2.nombre = "Jimena";
  usuario2.edad = 11;

  print(usuario1.nombre);
  print(usuario1.edad);
  print(usuario2.nombre);
  print(usuario2.edad);
}
---
### 2.2 Clases, atributos y metodos 
    Class User {
  String? nombre;
  int? edad;

  void reporte() {//1
  print("Nombre: $nombre");//2
  print("Edad : $edad años");//3
  }
}

void main(List<String> args) {
  User usuario1 = User();
  usuario1.nombre = "Alex";
  usuario1.edad = 50;

  usuario1.reporte(); //4
}
---
### 2.3 Encapsulamiento Metodos: Getter y Setter
  class User {
  String?_nombre;
  int?_edad;

  void set nombre (String nombre) {//1
  _nombre = nombre;//2
}

  String get nombre{//3
    return _nombre!;//4
}

void reporte() {
  print("Nombre: $_nombre");
  print("Edad : $_edad años");
}
}

void main(List<String> args) {
  final usuario1 = User();
  usuario1.nombre = "Alex"://5
  print(usuario1.nombre);//6
  usuario1.reporte();//
}
---
  Class User {
  String? _nombre;
  int? _edad;

  void set nombre(String nombre){
    _nombre = nombre;
  }

  String get nombre {
    return _nombre!;
  }

  void set edad(int edad) {
    _edad = edad;
  }

  int get edad {
    return_edad!;
  }

  void reporte() {
    print("Nombre: $_nombre");
    print("Edad : $_edad años");
  }
}

void main(List<String> args) {
  final usuario1 = User();
  usuario1.nombre = "Alex";
  usuario1.edad = 50;
  print(usuario1.nombre);
  print(usuario1.edad);
  usuario1.reporte();
}
---
### 2.4 Usando metodo Arrow
  Class User {
  String? _nombre;
  int? _edad;

  void set nombre(String nombre) =>_nombre!;
  void set edad(int edad) => _edad = edad;

  String get nombre => _nombre!;
  int get edad => _edad!;

  void reporte() {
    print("Nombre: $_nombre");
    print("Edad : $_edad años");
  }
}
void main(List<String> args) {
  final usuario1 = User();
  usuario1.nombre = "Alex";
  usuario1.edad = 50;
  print(usuario1.nombre);
  print(usuario1.edad);
  usuario1.reporte();
}
---
### 2.5 Constructores: Equivalencia de setters y getters
  Class User {
  String? _nombre; //1
  int? _edad;

  User(String nombre, int edad) { //2
    this._nombre = nombre;
    this._edad = edad;
  }

  String? get nombre => _nombre; //3
  int? get edad => _edad;
}

void main(List<String> args){
  final usuario1 = User("Alex", 50); //4
  print(usuario1.nombre);
  print(usuario1.edad);
}
---
### 2.6 Version corta de constructores(short hand)
  class User {
  String_nombre; //1
  int _edad;

  User(this.nombre, this.edad);//2

  String get nombre => _nombre;//3
  int get edad => _edad;
}

void main(List<String> args) {
  final usuario1 = User("Alex", 50);//4
  print(usuario1.nombre);
  print(usuario1.edad);
}
---
### 2.7 Varios Constructores en una Clases
  Class User {
  String? nombre;
  int? edad;

  User.nombre(this.nombre);//1
  User.edad(this.edad);//2

  String? get getNombre => nombre;
  int? get getEdad => edad;
}

void main(List<String> args) {
  final usuario1 = User.nombre("Alex");//3
  final usuario2 = User.edad("Alex");//4

  print(usuario1.getNombre);
  print(usuario1.getEdad);

  print(usuario2.getEdad);
  print(usuario2.getNombre);
}
---
### 2.8 Herencia y Polimorfismo
  Class Estudiante {
  String nombre = "";
  int edad = 0;

  void mostrarDatos() {
    print("Nombre: $nombre");
    print("Edad : $edad");
  }
}

class Profesor {
  String nombre ="";
  int edad = 0;

  void mostrarDatos(){
    print("Nombre: $nombre");
    print("Edad: $edad");
  }
}

class Directivo {
  String nombre = "";
  int edad = 0;

  void mostrarDatos() {
    print("Nombre: $nombre");
    print("Edad: $edad");
  }
}

void main(List<String> args) {
  final estudiante1 = Estudiante();
  estudiante1.nombre = "Hugo";
  estudiante1.edad = 15;
  estudiante1.mostrarDatos();

  final profesor1 = Profesor();
  profesor1.nombre = "Paco";
  profesor1.edad = 16;
  profesor1.mostrarDatos();
  final directivo1 = Directivo();
  directivo1.nombre = "Luis";
  directivo1.edad = 17;
  directivo1.mostrarDatos();
}
---
### 2.9 Sobreescritura de metodos (Overriding)
  Class User {
  String nombre = "";
  int edad = 0;

  void mostrarDatos() {
    print("Nombre: $nombre");
    print("Edad: $edad");
  }
}

class Estudiante extends User {
  @override
  void mostrar Datos() {
    print("Estudiante: $nombre");
    print("Edad: $edad");
  }
}
class Profesor extends User {}

class Directivo extends User {}

void main(List<String> args) {
  final estudiante1 = Estudiante()
  estudiante1.nombre = "Hugo";
  estudiante1.edad = 15;
  estudiante1.mostrarDatos();

  final profesor1 = Profesor();
  profesor1.nombre = "Paco"
  profesor1.edad = 16;
  profesor1.mostrarDatos();
}
---
### 2.10 Ejecucion de metodos de la superclase
  Class User {
  String nombre = "";
  int edad =0;
  User(this.nombre, this.edad);

  void mostrar Datos() {
    print("Nombre: $nombre");
    print("Edad: $edad");
  }
}

Class Estudiante extends User {
  Estudiante(String nombre, int edad) : super(nombre, edad);

  @override
  void mostrarDatos(){
    print("Estudiante");
    super.mostrarDatos();
  }
}

class Profesor extends User {
  Profesor(String nombre, int edad): super(nombre, edad);

  @override
  void mostrarDatos(){
    print("Profesor");
    super.mostrarDatos();
  }
}

class Directivo extends User {
  Directivo(String nombre, int edad) : super(nombre, edad);

  @override
  void mostrarDatos() {
    print("Directivo");
    super.mostrarDatos();
  }
}

void main(List<String> args) {
  final estudiante1 = Estudiante("Hugo", 15);
  estudiante1.mostrarDatos();

  final profesor1 = Profesor("Paco", 16);
  profesor1.mostrarDatos();
  final directivo1 = Directivo("Luis", 17);
  directivo1.mostrarDatos();
}
---
### 2.11 Clases astractas con constructores
  abstract class User {
  String? nombre;
  int? edad;

  User(this.nombre, this.edad);
  void mostrarDatos();
}

class Estudiante extends User {
  Estudiante(String nombre, int edad) : super(nombre, edad);
  void mostrarDatos(){
    print("Estudiante");
    print("Nombre: $nombre");
    print("Edad: $edad");
  }
}

void main(List<String> args) {
  //final estudiante1 = User();
  final estudiante1 = Estudiante("Alex", 50);
  estudiante1.mostrarDatos();
}
---
### 2.12 Interfaces
  class User {
  String? nombre;
  int? edad;

  void mostrarDatos() {}
}

class Estudiante implements User {
  String? nombre;
  int? edad;

  void mostrarDatos() {
    print("Estudiante");
    print("Nombre: $nombre");
    print("Edad: $edad");
  }
}

void main(List<String> args) {
  //final estudiante1 = User();
  final estudiante1 = Estudiante();
  estudiante1.nombre = "Alex";
  estudiante1.edad = 50;
  estudiante1.mostrarDatos();
}
---
### 2.13 Atributos y Metodos de Clases
  void main (List<String> args) {
  final usuario1 = User(); 
  final usuario2 = User();
  print(usuario1.maxUsers);
  print(usuario2.maxUsers);
}

class User {
  int maxUsers = 10; //propiedad de instancia
}
  
  
  
