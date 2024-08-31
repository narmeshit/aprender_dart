# Dart

Dart es un lenguaje de programación, desarrollado por Google y presentado al público en el año 2011 en Dinamarca. Fue concebido para correr sobre una máquina virtual, lo que nos brinda la oportunidad de que los proyectos que desarrollemos puedan ejecutarse en cualquier equipo según sean nuestras necesidades. En sus inicios se consideraba como una alternativa o sustituto a JavaScript, lo que, según sus creadores, podría convertirlo en un lenguaje popular y de uso extendido en poco tiempo. Pese a esto, solo fue hasta 2017 que su utilización comenzó a incrementarse, gracias a la aparición de Flutter, un framework que permite crear aplicaciones para todos los sistemas operativos. Dart nos ofrece la posibilidad de trabajar tanto en el desarrollo frontend como en el backend, aunque las encuestas dicen que parece ser que es más empleado en frontend. Google ha utilizado este lenguaje de programación para desarrollar sus productos AdSense y AdWords.

Dart ofrece un conjunto de herramientas que logran en el usuario la utilización de estas, que son de tipo de compiladores, analizadores y de formatear. Asimismo, una gran ventaja que ofrece Dart es la ejecución del código en el momento en el que se va desarrollando. También es importante mencionar las características o conocimientos similares que comparte con JavaScript o C ++.

Dart cuenta con un amplio conjunto de bibliotecas centrales que brindan elementos esenciales para muchas tareas de programación cotidianas, como trabajar con colecciones de objetos `(dart:collection)`, realizar cálculos `(dart:math)` y codificar/decodificar datos `(dart:convert)`. Hay API adicionales disponibles en [paquetes de uso común](https://dart.dev/resources/useful-packages). El repositorio de paquetes oficial para aplicaciones Dart y Flutter [pub.dev](https://pub.dev/).

## Hello World

Cada aplicación requiere la función de nivel superior `main()`, donde comienza la ejecución. Las funciones que no devuelven un valor de forma explícita tienen el `void` tipo de retorno. Para mostrar texto en la consola, puedes usar la `print()`función de nivel superior:

```dart
void main() {
  print('Hello, World!');
}
```

## Sintaxis Básica de Dart

Incluso en código Dart de tipo seguro , puedes declarar la mayoría de las variables sin especificar explícitamente su tipo mediante var. Gracias a la inferencia de tipos, los tipos de estas variables se determinan por sus valores iniciales:

```dart
var name = 'Voyager I';
var year = 1977;
var antennaDiameter = 3.7;
var flybyObjects = ['Jupiter', 'Saturn', 'Uranus', 'Neptune'];
var image = {
  'tags': ['saturn'],
  'url': '//path/to/saturn.jpg'
};
```

- **Variables y Tipos de Datos**

En Dart, var, final y const se utilizan para declarar variables, pero tienen diferencias en cuanto a su mutabilidad y en el momento en que se determinan sus valores.

```dart
//var: Se utiliza para declarar una variable cuya asignación inicial puede cambiar durante la ejecución del programa.
var nombre = 'Jhon';
//final: Declara una variable cuyo valor no puede cambiar una vez que se le ha asignado. Es inmutable después de la inicialización.
final edad = 25;
//const: Declara una variable cuyo valor es una constante y se determina en tiempo de compilación.
const pi = 3.14;
//Tipos de datos básicos
String name = 'Voyager I';
int entero = 20;
double decimal = 100.0;
bool booleano = true;
List list = [];
var image = {
  'tags': ['saturn'],
  'url': '//path/to/saturn.jpg'
};
```

### Operadores

En Dart, los operadores son símbolos que realizan operaciones sobre una o más variables. Estos operadores están divididos en varias categorías según el tipo de operación que realizan.

- **Operadores aritméticos**

Estos operadores se utilizan para realizar operaciones matemáticas básicas.

```dart
int a = 5;
int b = 3;
//Suma(+)
int suma = a + b; // 8
//Resta(-)
int resta = a - b; // 2
//Multiplicacion(*)
int multiplicacion = a * b; // 15
//Division(/)
double division = a / b; // 1.6666666666666667
```

- **Operadores de asignación**
Estos operadores se utilizan para asignar valores a las variables.

```dart
int x = 10;
x -= 5; // 5
x += 5; // 15
x *= 5; // 50
x /= 2; // 5
```

- **Operadores de incremento y decremento**
Estos operadores se utilizan para aumentar o disminuir en 1 el valor de una variable.

```dart
int x = 10;
x++; // 11
x--; // 9
```

- **Operadores de igualdad y relacionales**
Estos operadores comparan dos valores y devuelven un valor booleano (true o false).

```dart
int a = 10;
int b = 15;

bool esIgual = (a == b); // false
bool esDiferente = (a != b); // true
bool esMayor = (a > b); // true
bool esMenor = (a < b); // false
```

- **Operadores lógicos**
Estos operadores se utilizan para combinar expresiones lógicas.

```dart
int a = 1;
int b = 2;

bool y = (a > 0 && b < 5); // true
bool o = (a < 0 || b > 0); // true
bool negacion = !(a > 0); // false
```

- **Operador ternario**
Este operador es una forma corta de la estructura condicional if-else.
`Ternario (? :)`: Retorna un valor dependiendo de una condición.

```dart
int a = 1;
int b = 2;

String resultado = (a > b) ? 'a es mayor que b' : 'a es menor que b'; // 'es menor'
```

- **Operador de nulabilidad**
`??` Devuelve el valor de la izquierda si no es nulo, de lo contrario, devuelve el valor de la derecha.
`??=` Asigna el valor de la derecha a la variable de la izquierda solo si la variable es nula.

```dart
String nombre;
String nombreReal = nombre ?? 'Desconocido';
print(nombreReal); // Desconocido

String nombre;
nombre ??= 'Jhon';
print(nombre); // Jhon
```

- **Operadores de cascada (..)**
Permiten realizar múltiples operaciones en el mismo objeto.

```dart
var lista = [1, 2, 3]
  ..add(4)
  ..remove(2)
  ..insert(1, 5);
// lista = [1, 5, 3, 4]
```

### Control de Flujo

El control de flujo en Dart te permite dirigir cómo se ejecuta el código en función de condiciones o repeticiones. Existen varias estructuras de control de flujo en Dart, incluyendo condicionales `(if, else)`, bucles `(for, while, do-while)`, y estructuras de control de flujo de selección múltiple `(switch)`.

- **Condicional if, else if, else**
Estas estructuras de control permiten ejecutar bloques de código basados en condiciones booleanas.

```dart
int edad = 18;

if (edad >= 18) {
  print('Es mayor de edad');
} else if (edad >= 13) {
  print('Es un adolescente');
} else {
  print('Es un niño');
}
// Es mayor de edad
```

- **Ciclos for, for-in, while, do-while**
Estas estructuras permiten repetir bloques de código varias veces.

```dart
for (int i = 0; i < 5; i++) {
  print(i);
}
// 0, 1, 2, 3, 4

List<String> nombres = ['Ana', 'Luis', 'Pedro'];
for (var nombre in nombres) {
  print(nombre);
}
// Ana, Luis, Pedro

int contador = 0;
while (contador < 3) {
  print(contador);
  contador++;
}
// 0, 1, 2

```

- **Estructura switch-case**
La estructura switch es una alternativa al uso de múltiples if-else. Permite evaluar una expresión y ejecutar bloques de código basados en el valor de esa expresión.

```dart
String dia = 'lunes';

switch (dia) {
    case 'lunes':
        print('Es el primer día de la semana');
        break;
    case 'viernes':
        print('Es el último día laboral');
        break;
    default:
        print('Es un día entre semana');
}
// Es el primer día de la semana

```

- **Control de flujo con break y continue**
`break:` Se utiliza para salir de un bucle o una estructura `switch`.

```dart
for (int i = 0; i < 5; i++) {
  if (i == 3) {
    break;
  }
  print(i);
}
// 0, 1, 2

for (int i = 0; i < 5; i++) {
  if (i == 3) {
    continue;
  }
  print(i);
}
// 0, 1, 2, 4

```

### Funciones

En Dart, las funciones son bloques de código que realizan una tarea específica. Se utilizan para organizar el código, hacerlo más modular y reutilizable. Una función puede recibir parámetros, realizar operaciones y devolver un resultado (o no devolver nada, lo cual se indica con el tipo `void`).

- **Función sin parámetros y sin retorno**
Una función que no recibe datos ni devuelve ningún valor.

```dart
void saludar() {
  print('Hola');
}

void main() {
  saludar(); // Llamada a la función
}
// Hola
```

- **Función con parámetros**
Las funciones pueden recibir uno o más parámetros para realizar operaciones con ellos.

```dart
void saludarConNombre(String nombre) {
  print('¡Hola, $nombre!');
}

void main() {
  saludarConNombre('Jhon'); // Llamada a la función con un parámetro
}
// ¡Hola, Jhon!
```

- **Función con retorno**
Una función puede devolver un valor utilizando la palabra clave `return`.

```dart
int sumar(int a, int b) {
  return a + b;
}

void main() {
  int resultado = sumar(5, 3); // Llamada a la función y guardado del valor retornado
  print(resultado); // 8
}
```

- **Función de flecha**
Las funciones de flecha son una forma abreviada de escribir funciones de una sola expresión. Utilizan la sintaxis => en lugar de return.

```dart
// Función regular
int sumar(int a, int b) {
  return a + b;
}

// Función de flecha equivalente
int sumarFlecha(int a, int b) => a + b;
```

- **Expresiones Lambda**
Una expresión lambda es una función anónima (sin nombre) que se puede asignar a una variable o pasar como parámetro a otra función. Estas funciones son útiles cuando se necesita una función pequeña y sin reutilización.

```dart
void main() {
  // Lambda asignada a una variable
  var multiplicar = (int x, int y) => x * y;
  print(multiplicar(3, 4)); // 12

  // Lambda pasada como parámetro a una función
  List<int> numeros = [1, 2, 3, 4];
  var cuadrados = numeros.map((num) => num * num);
  print(cuadrados); // (1, 4, 9, 16)
}
```

- **Funciones Asíncronas**
En Dart, las funciones asíncronas se declaran con la palabra clave async y se utilizan con await para esperar los resultados de funciones que devuelven un Future.

```dart
Future<String> obtenerDatos() async {
  await Future.delayed(Duration(seconds: 2)); // Simulando una operación que tarda 2 segundos
  return 'Datos obtenidos';
}

void main() async {
  print('Esperando datos...');
  String datos = await obtenerDatos(); // Espera el resultado de la función asíncrona
  print(datos); // Datos obtenidos
}
// Esperando datos...
// (Después de 2 segundos)
// Datos obtenidos

```

## Colecciones

## La Programación Orientada a Objetos (POO)

Es un paradigma de programación basado en el concepto de "objetos", que pueden contener datos en forma de campos (también conocidos como atributos) y código en forma de procedimientos (también conocidos como métodos). Dart es un lenguaje de programación orientado a objetos, y entender los conceptos básicos de la POO es fundamental para desarrollar aplicaciones en Dart de manera efectiva.

- **Clase y Creación de Objetos**
Plantillas para crear objetos. Definen atributos y métodos. Instancias de clases.

```dart
class Persona {
  String nombre;
  int edad;

  // Constructor
  Persona(this.nombre, this.edad);

  // Método
  void saludar() {
    print('Hola, mi nombre es $nombre y tengo $edad años.');
  }
}

void main() {
  // Crear una instancia (objeto) de la clase Persona
  Persona persona1 = Persona('Jhon', 25);
  persona1.saludar(); // Hola, mi nombre es Jhon y tengo 25 años.
}
```

- **Encapsulación**
Oculta detalles internos y expone solo lo necesario.

```dart
class CuentaBancaria {
  double _saldo; // Atributo privado (encapsulado)

  CuentaBancaria(this._saldo);

  // Método público para acceder al saldo
  double obtenerSaldo() {
    return _saldo;
  }

  // Método público para realizar un depósito
  void depositar(double cantidad) {
    if (cantidad > 0) {
      _saldo += cantidad;
    }
  }
}

void main() {
  CuentaBancaria cuenta = CuentaBancaria(1000);
  cuenta.depositar(500);
  print('Saldo actual: ${cuenta.obtenerSaldo()}'); // Saldo actual: 1500
}
```

- **Herencia**
Permite a una clase heredar atributos y métodos de otra clase.

```dart
class Animal {
  void hacerSonido() {
    print('El animal hace un sonido.');
  }
}

class Perro extends Animal {
  @override
  void hacerSonido() {
    print('El perro ladra.');
  }
}

void main() {
  Animal miAnimal = Animal();
  miAnimal.hacerSonido(); // El animal hace un sonido.

  Perro miPerro = Perro();
  miPerro.hacerSonido(); // El perro ladra.
}

```

- **Polimorfismo**
Permite que diferentes clases usen el mismo método de manera diferente.

```dart
class Figura {
  double area() {
    return 0;
  }
}

class Rectangulo extends Figura {
  double ancho;
  double alto;

  Rectangulo(this.ancho, this.alto);

  @override
  double area() {
    return ancho * alto;
  }
}

class Circulo extends Figura {
  double radio;

  Circulo(this.radio);

  @override
  double area() {
    return 3.14 * radio * radio;
  }
}

void main() {
  List<Figura> figuras = [
    Rectangulo(5, 10),
    Circulo(7),
  ];

  for (Figura figura in figuras) {
    print('Área: ${figura.area()}');
  }
}
// Área: 50.0
// Área: 153.86

```

- **Abstracción**
Modela conceptos abstractos y simplifica la complejidad.

```dart
abstract class Forma {
  void dibujar();
}

class Cuadrado extends Forma {
  @override
  void dibujar() {
    print('Dibujando un cuadrado.');
  }
}

class Circulo extends Forma {
  @override
  void dibujar() {
    print('Dibujando un círculo.');
  }
}

void main() {
  Forma miForma = Cuadrado();
  miForma.dibujar(); // Dibujando un cuadrado.

  miForma = Circulo();
  miForma.dibujar(); // Dibujando un círculo.
}
```

## Gestión de Errores y Excepciones

En Dart, la gestión de errores y excepciones se refiere a la captura y manejo de condiciones anormales (excepciones) que ocurren durante la ejecución de un programa. Las excepciones pueden ser lanzadas de manera explícita o generadas automáticamente por el sistema cuando ocurre un error.

```dart
void main() {
  try {
    var resultado = 10 / 0;
    print('Resultado: $resultado');
  } catch (e) {
    print('Error: $e'); // Captura y maneja la excepción
  }
}
// Resultado: Infinity
```

## Gestión de Paquetes

- **Pubspec.yaml:** Configuración del archivo pubspec.yaml para agregar dependencias a tu proyecto Dart.
- **Uso de Paquetes:** Cómo buscar, agregar y utilizar paquetes de terceros con el gestor de paquetes de Dart, pub.

## Librerías y Modulares

- **Importación de Librerías:** Uso de la palabra clave import para incluir librerías externas y separadas dentro de tu proyecto.
- **Librerías Personalizadas:** Cómo crear y organizar tu propio código en diferentes archivos y módulos.

## Testeos

El testeo en Dart es una parte crucial del desarrollo de software, ya que permite asegurar que el código funcione correctamente y que los cambios no introduzcan errores inesperados. Dart proporciona un conjunto de herramientas para realizar pruebas unitarias, de integración y de widgets. Aquí te presento los conceptos clave y ejemplos de cómo realizar pruebas en Dart.

### Herramientas de Testeo

- **package:test** Proporciona herramientas para realizar pruebas unitarias y de integración en Dart.
- **package:mockito** Facilita la creación de mocks y stubs para pruebas.
- **package:flutter_test** Utilizado para pruebas de widgets en aplicaciones Flutter.

### Ejemplos

- **Pruebas Unitarias:** Verifican que partes individuales del código, como funciones o métodos, funcionen correctamente. Son pruebas de menor nivel y se enfocan en unidades específicas de código.

```dart
// archivo: calculadora.dart
int sumar(int a, int b) {
  return a + b;
}

int restar(int a, int b) {
  return a - b;
}

// archivo: calculadora_test.dart
import 'package:test/test.dart';
import 'calculadora.dart';

void main() {
  test('Prueba de suma', () {
    expect(sumar(2, 3), equals(5));
  });

  test('Prueba de resta', () {
    expect(restar(5, 3), equals(2));
  });
}
```

- **Pruebas de Integración:** Verifican que diferentes partes del sistema trabajen juntas correctamente. Estas pruebas suelen ser más amplias que las pruebas unitarias y pueden implicar múltiples componentes o módulos.

```dart
// archivo: servicio.dart
Future<String> fetchData() async {
  return Future.delayed(Duration(seconds: 1), () => 'Datos cargados');
}

// archivo: servicio_test.dart
import 'package:test/test.dart';
import 'servicio.dart';

void main() {
  test('Prueba de integración de fetchData', () async {
    expect(await fetchData(), equals('Datos cargados'));
  });
}
```

- **Pruebas de Widgets:** En Flutter, las pruebas de widgets verifican que los widgets se comporten y se representen correctamente en la interfaz de usuario.

```dart
// archivo: contador.dart
import 'package:flutter/material.dart';

class Contador extends StatefulWidget {
  @override
  _ContadorState createState() => _ContadorState();
}

class _ContadorState extends State<Contador> {
  int _contador = 0;

  void _incrementar() {
    setState(() {
      _contador++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text('Contador')),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text('Contador: $_contador'),
            ElevatedButton(
              onPressed: _incrementar,
              child: Text('Incrementar'),
            ),
          ],
        ),
      ),
    );
  }
}

// archivo: contador_test.dart
import 'package:flutter/material.dart';
import 'package:flutter_test/flutter_test.dart';
import 'contador.dart';

void main() {
  testWidgets('Prueba de widget Contador', (WidgetTester tester) async {
    // Construye el widget Contador
    await tester.pumpWidget(MaterialApp(home: Contador()));

    // Verifica que el texto inicial del contador sea 0
    expect(find.text('Contador: 0'), findsOneWidget);

    // Toca el botón de incrementar
    await tester.tap(find.byType(ElevatedButton));
    await tester.pump();

    // Verifica que el texto del contador haya cambiado a 1
    expect(find.text('Contador: 1'), findsOneWidget);
  });
}
```

- **Mocks y Stubs:** Se utilizan para simular el comportamiento de componentes externos que no son el foco de la prueba, permitiendo que la prueba se concentre en la unidad específica.

```dart
// archivo: servicio.dart
abstract class ApiService {
  Future<String> fetchData();
}

class Cliente {
  final ApiService apiService;

  Cliente(this.apiService);

  Future<String> obtenerDatos() {
    return apiService.fetchData();
  }
}

// archivo: cliente_test.dart
import 'package:mockito/mockito.dart';
import 'package:test/test.dart';
import 'servicio.dart';

class MockApiService extends Mock implements ApiService {}

void main() {
  test('Prueba con mock', () async {
    final mockApiService = MockApiService();
    when(mockApiService.fetchData()).thenAnswer((_) async => 'Datos cargados');

    final cliente = Cliente(mockApiService);
    expect(await cliente.obtenerDatos(), equals('Datos cargados'));
  });
}
```

## Ya está listo!!! para desarrollar aplicaciones utilizando Flutter

Al dominar estos aspectos del lenguaje, ustedes se sentirán seguros y capaces de escribir código limpio y eficiente, manejar la asincronía, y aplicar principios de programación orientada a objetos y funcional. Este conocimiento les permitirá sacar el máximo provecho de Flutter, facilitando el desarrollo de interfaces de usuario fluidas y bien estructuradas.
