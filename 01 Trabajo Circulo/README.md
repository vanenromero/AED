# AED
+ Algoritmos y Estructuras de Datos
+ Curso: K1051
+ Legajo: 2097369.
+ Apellido: Romero.
+ Nombre: Vanesa Noelia.

# *Trabajo de Círculo para promoción*

#### Objetivos
- Tipo Punto
- Tipo Circulo
- Operaciones EstánSolapados, y otra
- Main asserts
  
#### Desarrollo
- Se realiza trabajo indicado, a la hora de implementarlo se tienen en cuenta los conceptos aprendidos durante la cursada
- Comenzando se analizan las fórmulas afectadas para realizar las diferentes funciones y se utiliza como guía el trabajo número 17 de "Trabajos de AyED" 
- Se decide realizar las funciones para calcular la circunferencia, el área, la función llamada IsDentro y EstanSolapados. 
- Al buscar como llevar a cabo el trabajo, se encuentra información como por ejemplo, existe un header (Mathematical constants) que incluye el número Pi. 
  Se determina no agregar #include <numbers> debido a que lo único que utilizaríamos sería Pi, entonces se elige utilizar una variable constante con varios números luego de la coma.
  Además en el compilador que estoy utilizando, compila en C++17, el costo-beneficio de instalar otro compilador, queda en deuda si se puede resolver con una variable.
- A la hora de realizar las funciones se intenta ser claro y conciso, y que todo sea descriptivo de por si.
- Para realizar las funciones de IsDentro y EstanSolapados, se utiliza el recurso de GetDistancia (también usado en el trabajo de poligonos), se declara la función y luego se invoca en las otras dos funciones.
- Realizó los Asserts pedidos, en este caso se tuvo que utilizar la función AreNear realizada en clase hace tiempo, para poder comparar los resultados obtenidos con otro double pero que tiene menos decimales luego de la coma. 
