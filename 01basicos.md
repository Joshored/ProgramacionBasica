# Básicos de programación
## ¿Qué es programar?
Programar consiste en escribir instrucciones que una computadora puede ejecutar para resolver un problema.

**Conceptos importantes**
- Programa: Conjunto de instrucciones que ejecuta una computadora.
- Lenguaje de programación: Forma de comunicarnos con la computadora mediante reglas y sintaxis específicas.
- Algoritmo: Serie de pasos para resolver un problema.
-- Pedir dos números.
-- Sumarlos.
-- Mostrar el resultado.
- Variable: Espacio en memoria donde se almacena información.
## Instalación C y Python
Para **apt**:
1. Actualizar paquetes:
```
sudo apt update
sudo apt upgrade -y
```

2. Instalar compilador c: 
```
sudo apt install build-essential -y
```

3. Verificar: 
```
gcc --version
```

4. Instalar python: 
```
sudo apt install python3 python3-pip -y
```
5. Verificar: 
```
python3 --version
pip3 --version
```

### Pruebas rápidas:
- C: En terminal
```
nano hola.c o micro hola.c
```
Una vez que abra el editor de texto simple ingresar:
```
#include <stdio.h> // biblioteca de entrada y salida estandar de c

int main() { // indica la función principal
    printf("Hola mundo\n"); // printf es impresión con formato
    return 0; // la función regresa un entero arbitrario
}
```
Después guardar, puede ser:
```
ctrl + o ó ctrl + s
```

y salir:
```
ctrl + x ó ctrl + q
```
En terminal se compila:
```
gcc hola.c -o hola
```
y después se ejecuta:
```
./hola
```
- Python: En terminal
```
nano hola.py ó micro hola.py
```
En el editor simple ingresar:
```
print("hola mundo") #print palabra reservada para imprimir
```
Después guardar, puede ser:
```
ctrl + o ó ctrl + s
```

y salir:
```
ctrl + x ó ctrl + q
```
y ejecutas: 
```
python3 hola.py
```
## Variables
Las variables permiten guardar información.

**Python**
nombre = "Juan"\
edad = 20\
altura = 1.75\
**C**
char nombre[] = "Juan";\
int edad = 20;\
float altura = 1.75;

### Tipos comunes
| Tipo | Ejemplo |
| :--- | :---: |
| Entero | 10 |
| Decimal | 3.14 |
| Texto | "Hola" |
| Booleano | True |

## Entrada y Salida de Datos
**Python**
```
nombre = input("¿Cómo te llamas? ")
print("Hola", nombre)
```

**C**
```
char nombre[50]; //variable que almacena un arreglo de caracteres

printf("¿Cómo te llamas? ");
scanf("%49s", nombre); //scan = escanea

printf("Hola %s\n", nombre);
```

## Condicionales

Permiten tomar decisiones.

**Python**

```
edad = 18

if edad >= 18:
    print("Mayor de edad")
else:
    print("Menor de edad")
```

**C**

```
if (edad >= 18) {
    printf("Mayor de edad\n");
}
else {
    printf("Menor de edad\n");
}
```

Operadores de comparación
Operador	Significado
==	Igual
!=	Diferente
>	Mayor
<	Menor
>=	Mayor o igual
<=	Menor o igual

| Operador | Significado |
| :--- | :---: |
| == | Igual |
| != | Diferente |
| > | Mayor |
| < | Menor |
| >= | Mayor o igual |
| <= | Menor o igual|

## Ciclo While

Repite instrucciones mientras una condición sea verdadera.

**Python**
```
contador = 1

while contador <= 5:
    print(contador)
    contador += 1
```

**C**
```
int contador = 1;

while (contador <= 5) {
    printf("%d\n", contador);
    contador++;
}
```

## Ciclo For

Ideal cuando conocemos cuántas veces repetir.

**Python**
```
for i in range(10):
    print(i)
```

**C**
```
for (int i = 0; i < 10; i++) {
    printf("%d\n", i);
}
```

## Funciones

Permiten reutilizar código.

**Python**
```
def sumar(a, b):
    return a + b
```

C
```
int sumar(int a, int b) {
    return a + b;
}
```

## Listas y Arreglos

Permiten almacenar varios datos.

**Python**
```
numeros = [10, 20, 30]
```

**C**
```
int numeros[3] = {10, 20, 30};
```

Recorrer elementos

**Python:**

```
for numero in numeros:
    print(numero)
```


**C:**

```
for (int i = 0; i < 3; i++) {
    printf("%d\n", numeros[i]);
}
```
## Buenas Practicas
- Usar nombres descriptivos.
- Mantener el código ordenado.
- Comentar cuando sea necesario.
- Probar constantemente.
- Leer los errores antes de pedir ayuda.

# Git 
## ¿Qué es Git?
Git es un sistema de control de versiones.

Permite:

- Guardar cambios en un proyecto.
- Volver a versiones anteriores.
- Saber quién realizó cada cambio.
- Trabajar en equipo sin sobrescribir trabajo ajeno.

## ¿Qué problema resuelve Git?

Sin Git:

1. proyecto_final.py
2. proyecto_final_v2.py
3. proyecto_final_v3.py
4. proyecto_final_ahora_si.py
5. proyecto_final_definitivo.py

Con Git:

Proyecto

└── Historial de cambios

Git registra cada modificación sin crear decenas de copias.
## Instalar Git
Instalación mediante terminal: 
```
sudo apt install git
```
Verificar instalación:
```
git --version
```

## Configuración Inicial

Configurar nombre:

```
git config --global user.name "Juan Pérez"
```


Configurar correo:

```
git config --global user.email "correo@ejemplo.com"
```


Ver configuración:

```
git config --list
```

## Clonar un Proyecto
```
git clone URL_DEL_REPOSITORIO
```

Copia un proyecto completo a tu computadora.

## Subir Cambios

Primera vez:

```
git push -u origin main
```


Después:

```
git push
```

## Descargar Cambios
```
git pull
```


Obtiene los cambios más recientes.