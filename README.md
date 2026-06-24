# Salguero_Danny_AlgEstDatos_U1
Ejercicio de una pila enlazada, una cola enlazada y una lista enlazada vinculadas por medio de main y con interfaz grafica de usuario por medio de Tkinter.
# Gestor de Turnos CarUPS
## Algoritmos y Estructuras de Datos – Unidad 1
### Autor
Danny Salguero
---
# Descripción
Este proyecto implementa un sistema de gestión de turnos para un taller automotriz (CarUPS) utilizando las tres estructuras lineales estudiadas en la Unidad 1 de Algoritmos y Estructuras de Datos:
- Pila enlazada (LIFO)
- Cola enlazada (FIFO)
- Lista simplemente enlazada

Cada estructura fue implementada manualmente mediante nodos enlazados, sin utilizar estructuras propias de Python como listas para representar la estructura interna.
Además del programa de consola solicitado, el proyecto incorpora una interfaz gráfica desarrollada con Tkinter para facilitar la manipulación de clientes y la visualización de las pruebas de las estructuras.
---
# Estructura del proyecto
```
Proyecto
│
├── main.py
├── datos_prueba.py
├── Ejercicio_pila_enlazada.py
├── Ejercicio_de_cola_enlazada.py
├── Ejercicio_de_lista_enlazada.py
├── Ejercicio_de_ventana_de_integracion.py
└── README.md
```
---
# Requisitos
- Python 3.10 o superior
No es necesario instalar librerías externas, ya que únicamente se utilizan módulos estándar de Python:
- tkinter
- tkinter.ttk
- tkinter.messagebox
---
# Podemos ejecutar el programa de las siguientes formas:
## Primera Opción: Programa de consola
Ejecutar:
```bash
python main.py
```
Se ejecutarán automáticamente las pruebas de:
- Pila enlazada
- Cola enlazada
- Lista enlazada
---
## Segunda Opción: Interfaz gráfica
Ejecutar:
```bash
python Ejercicio_de_ventana_de_integracion.py
```
Desde la interfaz es posible:
- Registrar turnos
- Deshacer acciones
- Encolar clientes
- Atender clientes
- Insertar clientes
- Buscar clientes por nombre
- Buscar clientes por cédula
- Eliminar clientes
- Mostrar todos los clientes
- Vaciar la lista
- Cargar datos de prueba
---
# Descripción de las estructuras

## 1. Pila enlazada (LIFO)

La pila implementa el principio **Last In First Out**, donde el último elemento ingresado es el primero en salir.

En este proyecto se utiliza para registrar el historial de acciones realizadas por el operador.
En primer lugar, debemos explicar el principio, Last In First Out, que se puede traducir como el último en llegar o ingresar es el primero en salir. Entonces como una pila funciona por medio del mecanismo LIFO, y que además se suele tener en cuenta que una pila puede funcionar como:
 Un conjunto de objetos superpuestos verticalmente en la vida real… … se cuenta con un conjunto de elementos donde el primero que se adquiere siempre es el último en ubicarse en una pila y donde siempre se ubica uno nuevo en el tope -cima- de la pila(Pérez Castaño, 2016, p. 161)
Al implementar la pila enlazada es frecuente usar algunas de sus operaciones que son: push()  o apilar que agrega, empuja o ubica  un elemento en la cima de la pila enlazada, si en cambio queremos sacar, deshacer o desapilar el elemento  ubicado en la cima de la pila usamos pop(), otras operaciones que podemos usar para mostrar o devolver el elemento que esta en la cima mediante peek() o pop(), aclaro que estas operación no remueve el elemento solo nos da a conocer que elemento se encuentra en la cima. Además, se debe prevenir o justificar de alguna manera que hacer si la pila queda vacía, que es cuando se produce un desbordamiento o underflow, la operación que verifica esta ocurrencia de vaciado es isEmpty, que en caso de existir una pila emerge el error IndexError. También puede ocurrir que excedamos la capacidad de almacenamiento en la memoria al momento de sobre apilar desmesuradamente hasta que se agote la memoria este error se conoce como overflow.

### Operaciones principales
- push()
- pop()
- peek()
- recorrer()
---
## 2. Cola enlazada (FIFO)
La cola implementa el principio **First In First Out**, donde el primer cliente que llega es el primero en ser atendido.
Se implementó mediante referencias al frente y al final de la cola para que las operaciones principales tengan complejidad constante.
Iniciaremos explicando el principio First In First Out, que se entiende como el primero en entrar es el primero en salir. Ahora una cola puede entender como:
 Un conjunto de objetos que se ubican uno a continuación del otro y donde el orden de acceso a estos es lineal, es decir, se encuentran ordenados por orden de llegada o según el tiempo que han permanecido encolados, siendo el primer objeto que más tiempo ha pasado en la cola.(Pérez Castaño, 2016, p. 165)
Ahora algunas de las operaciones que podemos realizar con las colas son: “enqueue (encolar), que inserta un elemento al final; dequeue (desencolar), que retira el elemento del frente; y front, que consulta el primer elemento sin retirarlo”(Universidad Politécnica Salesiana, 2026a). Al igual que en las pilas también se comprueba el vaciado de la cola. Existen algunas otras variantes de las colas como la cola circular o la cola de prioridad.

### Operaciones principales
- enqueue()
- dequeue()
- recorrer()
---
## 3. Lista simplemente enlazada
Este tipo de estructura de datos, resuelve el problema del costo de contigüidad de los arreglos, realizando una renuncia a la contigüidad, “sus elementos viven dispersos en la memoria, unidos por referencias. La pieza básica es el nodo, un pequeño contenedor con dos partes: el dato que almacena y una referencia (enlace o puntero) al siguiente nodo”(Universidad Politécnica Salesiana, 2026b). Es decir, una lista enlazada, se puede definir de la siguiente forma:
Un conjunto de nodos que se conectan de manera lineal por medio de referencias (los enlaces son las referencias) y donde cada nodo contiene no solo referencias a su antecesor y al próximo nodo en la lista, sino que también almacena cualquier valor que se le defina(Pérez Castaño, 2016, p. 174)
Entre algunas de las operaciones que podemos realizar en una lista enlazada inserciones, eliminaciones en tiempo constante, como insertar al inicio, insertar al final, eliminar nodos sea de inicio, final o también permite realizar la operación recorrer() y con ello realizar inserciones o eliminaciones a lo largo de la lista enlazada. También se puede verificar el vaciado donde como consecuencia finalmente quedara None. Existen variantes a las listas enlazadas como las listas ordenadas.

La lista enlazada almacena los clientes registrados.
Cada nodo contiene:
- Cédula
- Nombres
- Apellidos
- Referencia al siguiente nodo
Permite:
- insertar al inicio
- insertar al final
- eliminar clientes
- buscar por cédula
- buscar por nombre
- mostrar todos los clientes
- vaciar la lista
---
# Tabla de complejidades

| Estructura | Operación | Complejidad | Justificación |
|------------|-----------|-------------|---------------|
| Pila | push | O(1) | Inserta un nodo en la cima. |
| Pila | pop | O(1) | Elimina el nodo de la cima. |
| Pila | peek | O(1) | Consulta el elemento superior. |
| Pila | recorrer | O(n) | Recorre todos los nodos. |
| Cola | enqueue | O(1) | Inserta al final utilizando la referencia tail. |
| Cola | dequeue | O(1) | Elimina desde el frente utilizando la referencia head. |
| Cola | recorrer | O(n) | Recorre todos los nodos. |
| Lista | insertar_al_inicio | O(1) | Inserta directamente en la cabeza. |
| Lista | insertar_al_final | O(n) | Recorre la lista hasta el último nodo. |
| Lista | buscar_por_cedula | O(n) | Puede recorrer toda la lista. |
| Lista | buscar_por_nombre | O(n) | Puede recorrer toda la lista. |
| Lista | eliminar | O(n) | Debe localizar el nodo antes de eliminarlo. |
| Lista | recorrer | O(n) | Recorre toda la lista. |
| Lista | vaciar | O(1) | Asigna la cabeza a None. |
---
# Casos de prueba
El proyecto incluye casos de prueba mediante:
- main.py
- datos_prueba.py
- 
Además, la interfaz gráfica permite cargar automáticamente dichos datos para verificar el funcionamiento de las tres estructuras.
---

# Conclusión

Este proyecto demuestra la implementación manual de las estructuras de datos fundamentales mecionadas mediante nodos enlazados. Sin embargo algo que se debe tener en cuenta el contexto o caracteristicas de lo que queremos implementar si quiero eliminar o insertar solo desde el frente, desde la cabeza o final o tail o si queremos realizar inserciones eliminaciones a lo largo del conjunto de elementos podemos usar una lista enlazada. También dedemos tener en cuenta el vaciado o underflow y la sobrecarga lllamado overflow.
[main.py](https://github.com/user-attachments/files/29313823/main.py)
[Ejercicio_pila_enlazada.py](https://github.com/user-attachments/files/29313822/Ejercicio_pila_enlazada.py)
[Ejercicio_de_ventana_de_integracion.py](https://github.com/user-attachments/files/29313821/Ejercicio_de_ventana_de_integracion.py)
[Ejercicio_de_lista_enlazada.py](https://github.com/user-attachments/files/29313820/Ejercicio_de_lista_enlazada.py)
[Ejercicio_de_cola_enlazada.py](https://github.com/user-attachments/files/29313819/Ejercicio_de_cola_enlazada.py)
[datos_prueba.py](https://github.com/user-attachments/files/29313818/datos_prueba.py)

