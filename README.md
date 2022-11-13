# Práctica 2 

Hecha por María Calvo Torres, Pedro Bereilh y Gonzalo Valdez Casis

## Como ejecutar el programa
Debemos tener instalado Apache Ant para comprobar si lo tenemos usar el comando:

````
ant -version 
`````

Para ejecutar la clase Main.java usar el comando:

````
ant run_main
````

> **_NOTA:_**  Ejecutar desde dentro de la carpeta java-algorithms-implementation.

Resultado tras ejecutar el comando anterior ir de v1 a v10:

![](Resultado.png)

## Grafo donde se genera el camino 
- Queremos ir de v1 a v10 y usamos el algoritmo A*

![](GrafoAEstrella.PNG)

## Preguntas sobre la práctica

**¿Qué variable representa la lista ABIERTA?**
- La variable openSet en la línea 44 de la clase Astar.java

**¿Qué variable representa la función g?**
- La variable gScore en la línea 48 de la clase Astar.java, la cual rellena sus datos en la línea 91

**¿Qué variable representa la función f?**
- La variable fScore en la línea 52 de la clase Astar.java, la cual rellena sus datos en la línea 54-55

**¿Qué método habría que modificar para que la heurística representara la distancia aérea entre vértices?**
- El método heuristicCostEstimate en la línea 119 de la clase Astar.java, por el momento devuelve 1 y no utiliza un cálculo de distancias aéreas.

**¿Realiza este método reevaluación de nudos cuando se encuentra una nueva ruta a un determinado vértice? Justifique la respuesta.**
- Sí, en la línea 96 se reevalúan todos los nudos del openSet ordenando el openSet para que el siguiente nudo a expandir sea el de menor fScore, se utiliza un comparador en la línea 62 que compara los fScore y devuelve valores que son útiles para la función sort.
