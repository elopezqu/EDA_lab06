<div align="center">
<table>
    <theader>
        <tr>
            <td><img src="https://github.com/rescobedoq/pw2/blob/main/epis.png?raw=true" alt="EPIS" style="width:50%; height:auto"/></td>
            <th>
                <span style="font-weight:bold;">UNIVERSIDAD NACIONAL DE SAN AGUSTIN</span><br />
                <span style="font-weight:bold;">FACULTAD DE INGENIERÍA DE PRODUCCIÓN Y SERVICIOS</span><br />
                <span style="font-weight:bold;">ESCUELA PROFESIONAL DE INGENIERÍA DE SISTEMAS</span>
            </th>
            <td><img src="https://github.com/rescobedoq/pw2/blob/main/abet.png?raw=true" alt="ABET" style="width:50%; height:auto"/></td>
        </tr>
    </theader>
    <tbody>
        <tr><td colspan="3"><span style="font-weight:bold;">Formato</span>: Guía de Práctica de Laboratorio</td></tr>
        <tr><td><span style="font-weight:bold;">Aprobación</span>:  2022/03/01</td><td><span style="font-weight:bold;">Código</span>: GUIA-PRLD-001</td><td><span style="font-weight:bold;">Página</span>: 1</td></tr>
    </tbody>
</table>
</div>
<div align="center">
 <h3>INFORME DE LABORATORIO</h3>
</div>
<table>
 <theader>
  <tr><th colspan="6" bgcolor="red">INFORMACIÓN BÁSICA</th></tr>
 </theader>
 <tbody>
  <tr><td>ASIGNATUA:</td><td colspan="5">Estructura de Datos y Algoritmos</td></tr>
  <tr><td>TÍTULO DE LA PRACTICA:</td><td colspan="4">Árboles<td></tr>
  <tr><td>NÚMERO DE PRÁCTICA:</td><td>Practica de Laboratorio 06</td><td>AÑO LECTIVO:</td><td>2022 A</td><td>NRO. SEMESTRE:</td><td>III</td></tr>
  <tr><td>FECHA DE PRESENTACIÓN:</td><td>12-Jun-2022</td><td>HORA DE PRESENTACIÓN:</td><td colspan="3">11:30 p.m.</td></tr>
  <tr><td>INTEGRANTES:</td><td colspan="3">-Diego Ivan Pacori Anccasi<br>-Edson Joel López Quispe<br>-Oliver Alessandro Mayta Nolasco<br>-Edwin Francisco Aguilar Tancayo<br>-Jordy Emanuel Ayma Cutipa</td><td>NOTA:</td><td>...</td></tr>
  <tr><td>DOCENTE:</td><td colspan="5">Richart Smith Escobedo Quispe - rescobedoq@unsa.edu.pe</td></tr>
 </tbody>
</table>
<table>
 <theader>
  <tr><th>SOLUCIÓN Y RESULTADOS</th></tr>
 </theader>
 <tbody>
  <tr><td><strong>I. SOLUCIÓN DE EJERCICIOS/PROBLEMAS:</strong><br>
  <ul>
    <ol>
        <li>Modificar el método de obtención de valor dado una clave (5 puntos)
En el código, para la clave www.simpsons.com, invocado de la siguiente manera:</li>
        <h1>1.- Funcionamiento del metodo Get</h1>
        <img src="Pregunta1/get.PNG">
        <p>El metodo get recibe la clave y verifica si esta es nula para mandar un error, sino retorna el metodo search el cual devuelve un valor</p>
        <h1>2.- Metodo Search (Original)</h1>
        <img src="Pregunta1/searchOriginal.png">
        <p>Crea un arreglo de Entry los cuales poseen como atributo clave, valor y un nodo siguiente: a continuacion la clase Entry:</p>
        <img src="Pregunta1/Entry.png">
        <p>luego con una condicion la cual exige que la altura sea 0, de lo contrario, verificara el numero de hijos del nodo en un for y dentro de este verificara un if el cual vera si las claves son diferentes, la que le mandamos como parametro y la key del hijo siguiente "children[j+1].key" (si son diferentes = true, si son iguales = false) con el metodo less, a continuacion el metodo less y el eq(este es todo lo contrario al less)</p>
        <img src="Pregunta1/comparadores.png">
        <p>Al entrar al if, empieza una recursividad la cual implica disminuir la altura, enviarle el nodo del hijo(children[j].next) y la key a buscar</p>
        <img src="Pregunta1/else.png">
        <p>Cuando la altura llegue a ser 0 va a entrar en el if y va a buscar en los hijos para ver cual de ellos coincide con la clave y al encontrarlo, va a retornar dicho valor, pero solo 1, a pesar de que haya otra key que coincida</p>
        <img src="Pregunta1/if.png">
        <p>Y nos retornara 1 solo valor de los 2 que ingresamos:</p>
        <img src="Pregunta1/putDatos.png">
        <p>resultado</p>
        <img src="Pregunta1/result1.png">
        <h1>3.- Metodo Search (Modificado)</h1>
        <img src="Pregunta1/modificacion.PNG">
        <p>El cambio fue realizado al entrar en el if donde la condicion es el metodo eq, el cual verifica si son iguales, ya no retorna ahi, sino que lo hace fuera del for, para que pueda buscar en todo el nodo de valores, y al momento de realizar la coincidencias lo acumule en un String, y el resultado seria el siguiente:</p>
        <img src="Pregunta1/result2.png">
        <hz>
        <li>Mostrar en un diagrama de árbol gráficamente la estructura final para los datos
ingresados. (4 puntos)</li>
        <li>El método toString() del árbol, retorna lo siguiente. ¿Por qué están entre paréntesis
ciertas claves? (4 puntos)</li>
        <li>Agregar un nodo adicional (www.youtube.com, 134.24.13.78) y mostrarlo paso a
paso. (3 puntos)</li>
  </ul>

  <tr><td><strong>III. CONCLUSIONES:</strong><br>- Un AVL es un arbol binario de busqueda que satisface la condicion de estar balanceado<br>
  - La propiedad del balanceo dice que para cada nodo la diferencia de alturas entre el subarbol izquierdo y derecho es a lo sumo 1<br>
  - Esta propiedad garantiza que la altura del arbol sea de O(log n)<br>
  - En cada nodo del arbol se guarda informacion de la altura<br></td></tr>
 </tbody>
</table>
<hr>
<table>
 <theader>
  <tr><td><strong>III. RETROALIMENTACIÓN GENERAL</strong><br>
  </td><tr>
 </theader>
 <tbody>
  <tr><td>- AVL (Addelson-Velskii y Landis) Este tipo de arbol nos permite tener una estructura eficiente con respecto a su padre el BST, y trata de mantenerlo balanceado(BST)
  </td></tr>
 </tbody>
</table>
<hr>
<table>
 <theader>
  <tr><td><strong>REFERENCIAS Y BIBLIOGRAFÍA</strong></td><tr>
 </theader>
 <tbody>
  <tr><td>https://algorithmtutor.com/Data-Structures/Tree/AVL-Trees/</td></tr>
  <tr><td>https://docs.oracle.com/javase/tutorial/java/generics/types.html</td></tr>
  <tr><td>...</td></tr>
  <tr><td>...</td></tr>
  <tr><td>...</td></tr>
 </tbody>
</table>
