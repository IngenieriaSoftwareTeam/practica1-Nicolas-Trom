[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11763535&assignment_repo_type=AssignmentRepo)
# Práctica 1

*:warning: Importante:* escribir nombre y número de estudiante en la línea siguiente:  
- Nombre: Nicolas Trombotti 
- Número de estudiante: 267736


Una vez creado el repositorio GitHub, debe clonarlo para trabajar localmente. Debe instalar previamente: Git, Visual Studio Code y haber realizado la autenticación en GitHub.
- Copiar la <url> del repositorio usando el botón **(<> Code) / Local**.
- Abrir la terminal de comandos.
    - `git clone <url>`
    - `cd <directorio>` 

## Parte A

Dada la siguiente imagen de un grafo de depedencias entre ramas de un repositorio git se pide:

- Escribir en orden cronologico los comandos git que se utilizaron para poder realizar el grafo de la imagen.

![Image](https://i.ibb.co/KrdCt5s/grafo.png)

*Aclaraciones:*
- La cronología se lee de izquierda a derecha.
- El número en los nodos representa la cronología de los commits.
- Cada nodo es un commit.
*Recomendación: usar como mensaje de commit el número del nodo, ejemplo: 'Commit 1'.*
- Hay cuatro ramas con su nombre correspondiente:
  - main
  - feature1
  - feature2
  - fix1

**Escribir la secuencia de comandos en un issue GitHub con el nombre "Parte A", no es necesario ejecutar los comandos.**

## Parte B

Usted es el encargado de implementar dos nuevas funcionalidades en un proyecto. Es una Calculadora que permite ralizar las operaciones básicas como la suma, resta, multiplicación y división.
Las nuevas funcionalidades se documentan en el archivo Markdown `doc/features.md`. El código de la calculadora se encuentra `src/calculator.js`. 

Los cambios se deben codificar en el repositorio local y posteriormente hacer push al repositorio remoto GitHub. Cada feature se debe codificar en una rama independiente. Todas las ramas deben quedar en el repositorio remoto al finalizar.

1. Especificación de funcionalidades de la calculadora
   - Modificar el archivo `doc/features.md` agregando un título 'Funcionalidades de la calculadora' y una lista con cuatro ítems de texto: 'suma', 'resta', 'multiplicación' y 'división'.
   - Realizar commit del cambio en la rama 'main'
   - Realizar push de la rama 'main' al repositorio remoto

2. Feature 'multiply'
    - A partir de 'main' crear una nueva rama 'multiply' y moverse a dicha rama para agregar la feature.
    - Completar en el archivo `src/calculator.js` la funcionalidad multiply:
    ```javascript 
    function multiply(a, b) {
      return a * b;
    }
    ```
   - Agregar en el archivo `doc/implemented_features.md` la funcionalidad: 'Multiplicación'.
   - Realizar commit del cambio en la rama
   - Realizar push de la rama 'multiply' al remoto

3. Feature 'divide'
   - Moverse a la rama 'main'
   - A partir de 'main' crear una nueva rama 'divide' y moversa a dicha rama para agregar la feature.
   - Completar en el archivo `src/calculator.js` la funcionalidad divide:
    ```javascript 
    function divide(a, b) {
      if (b === 0) {
        throw new Error('Cannot divide by zero');
      }
      return a / b;
    }
    ```
   - Agregar en el archivo `doc/implemented_features.md` la funcionalidad: 'División'.
   - Realizar commit del cambio en la rama.
   - Realizar push de las rama 'divide' al remoto.

4. Merge de features
   - Moverse a la rama 'main'
   - Realizar merge de la rama 'multiply' a 'main'
   - Realizar merge de la rama 'divide' a 'main'
   - Realizar push de la rama 'main' al remoto

5. Tag e historial
   - Agregar un tag 'v1.0' al último commit de 'main'
   - Obtener un historial de los cambios realizados (opciones --oneline --graph)
   - Capturar la pantalla de la consola que muestra el historial 

**subir la captura de pantalla en un issue en GitHub con el nombre "Parte B"**
