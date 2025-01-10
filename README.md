
# Boogle Game

Mi primer proyecto programado un juego de Boogle en C++

Este programa es un juego interactivo de búsqueda de palabras. Los jugadores deben encontrar palabras válidas en un tablero de letras aleatorias. A medida que encuentran palabras, estas se validan y se otorgan puntos dependiendo de su longitud.

Genera un tablero de juego: Crea un tablero de 5x5 lleno de letras al azar.

Encuentra palabras:

Detecta palabras válidas automáticamente en el tablero.
Los jugadores pueden ingresar palabras manualmente para validarlas.

Asignación de puntos: Se otorgan puntos basados en la longitud de las palabras encontradas:

3-4 letras: 1 punto.
5 letras: 2 puntos.
6 letras: 3 puntos.
7 letras: 5 puntos.
8 o más letras: 11 puntos.

Los jugadores tienen un límite de 3 minutos para buscar palabras en cada ronda.

*El juego posee un diccionario en ingles y en español*

![image](https://github.com/user-attachments/assets/09468a64-934c-4e26-9cbd-735c74449410)
![image](https://github.com/user-attachments/assets/533e7f9a-4c5a-49d3-98be-b9040444fe01)


# Documentación

## Clases Incluidas

### 1. `Dictionary`
Clase que implementa un diccionario para almacenar palabras, verificar prefijos y buscar palabras en un tablero.

#### Métodos principales:
- **`addWord(string word)`**: Agrega una palabra al diccionario.
- **`isWord(string word)`**: Verifica si una palabra existe en el diccionario.
- **`isPrefix(string word)`**: Comprueba si un prefijo existe en el diccionario.
- **`wordCount()`**: Devuelve la cantidad de palabras en el diccionario.
- **`SolveBoard(char board[][5], int steps[][5], Dictionary& dict, Dictionary& wordsFound, bool printBoard)`**: Encuentra palabras en un tablero de 5x5 usando el diccionario.
- **`res(int lang)`**: Carga un tablero aleatorio y resuelve las palabras en él.

### 2. `checkword`
Clase utilizada para verificar palabras ingresadas por el usuario y manejar archivos como `output.txt` y `discard.txt`.

#### Métodos principales:
- **`CheckW(string word)`**: Verifica si una palabra está en `output.txt` y asigna una puntuación según su longitud.
- **`isDupe(string word)`**: Comprueba si una palabra ya ha sido utilizada (duplicada).
- **`GetLenght()`**: Devuelve la puntuación asignada a la palabra.
- **`GetRep()`**: Retorna si la palabra es repetida o no.

### 3. `Tempo`
Clase que implementa un temporizador para un juego con un tiempo límite.

#### Métodos principales:
- **`reloj()`**: Ejecuta un temporizador que cuenta desde 180 segundos hasta 0, con opción de reiniciar el tiempo o finalizar el juego.

### 4. `random`
Clase que genera caracteres aleatorios para llenar un tablero.

#### Métodos principales:
- **`a()`**: Llena el arreglo `strrnd` con caracteres aleatorios.
- **`rango(int, int)`**: Genera un número aleatorio dentro de un rango.

# Créditos

El algoritmo de resolución utilizado en este programa fue inspirado en el repositorio [BoggleSolver](https://github.com/joebadua/BoggleSolver) creado por [Joe Badua](https://github.com/joebadua). Fue quien creó la lógica de búsqueda de palabras en el tablero.

Este programa toma la base de ese algoritmo y lo adapta para fines específicos del juego, como la integración con un sistema de puntuación.
