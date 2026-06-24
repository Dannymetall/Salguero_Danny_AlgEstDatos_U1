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

# Cómo ejecutar el programa

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

### Operaciones principales

- push()
- pop()
- peek()
- recorrer()
---
## 2. Cola enlazada (FIFO)
La cola implementa el principio **First In First Out**, donde el primer cliente que llega es el primero en ser atendido.
Se implementó mediante referencias al frente y al final de la cola para que las operaciones principales tengan complejidad constante.
### Operaciones principales
- enqueue()
- dequeue()
- recorrer()
---
## 3. Lista simplemente enlazada
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

