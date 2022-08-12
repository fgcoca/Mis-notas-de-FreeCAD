# <FONT COLOR=#8B008B>3.2. Plano de referencia fijado a objetos</font>
Vamos a explicar como crear planos de referencia fijados a los objetos denominados “Plano XY, Plano XZ y Plano YZ” representados en la Figura 3.2.1 que son los planos coordenados que configuran el triedro trirectángulo de cada uno de los cuadrantes. Ya hemos vistos que cuando creamos un cuerpo o body se crea un elemento denominado “Origin” que contiene los tres planos y los tres ejes de referencia del sistema de coordenadas.

<center>

![Planos de referencia](../img/PR-fijado-objetos/F3_2_1.png)  
*Figura 3.2.1. Planos de referencia*

</center>

Si hacemos clic en el icono de crear un nuevo objeto plano de referencia, se va a mostrar por defecto el nuevo plano en el plano de referencia XY y se abrirá la ventana de parámetros para seleccionar y con los modos de fijación, pero lógicamente sin tener ninguna referencia seleccionada, como vemos en la Figura 3.2.2.

<center>

![Ventana de parámetros y plano de referencia](../img/PR-fijado-objetos/F3_2_2.png)  
*Figura 3.2.2. Ventana de parámetros y plano de referencia*

</center>

Si situamos el cursor durante un par de segundos, por ejemplo, sobre la opción de “Objetos de XY” se mostrarán los tipos de fijación que estarán disponibles y que vemos en la Figura 3.2.3.

<center>

![Tipos de fijación disponibles](../img/PR-fijado-objetos/F3_2_3.png)  
*Figura 3.2.3. Tipos de fijación disponibles*

</center>

Si en esta situación cerramos la tarea haciendo clic en OK se nos mostrará una advertencia como la que vemos en la Figura 3.2.4.

<center>

![Creación de plano de referencia inamovible](../img/PR-fijado-objetos/F3_2_4.png)  
*Figura 3.2.4. Creación de plano de referencia inamovible*

</center>

Si hacemos clic en “Yes” se nos crea un plano en XY pero que estará fijado al plano XY de referencia y no podremos moverlo, como vemos en la Figura 3.2.5.

<center>

![Plano re referencia inamovible fijado al de referencia](../img/PR-fijado-objetos/F3_2_5.png)  
*Figura 3.2.5. Plano re referencia inamovible fijado al de referencia*

</center>

Vamos a repetir la operación de crear un plano de referencia pero esta vez vamos a seleccionar uno de los planos de referencia del sistema y podemos observar como el plano que se va a crear queda atado al plano de referencia seleccionado y además con valores de movimiento editables, como se observa en la Figura 3.2.6.

<center>

![Plano re referencia movible fijado al de referencia](../img/PR-fijado-objetos/F3_2_6.png)  
*Figura 3.2.6. Plano re referencia movible fijado al de referencia*

</center>

Pues bien, lo que vamos a ver a continuación es como fijar el plano de referencia a “Objetos de XY, de XZ o de YZ”. Vamos a diseñar la pieza que vemos en la figura 3.2.7 utilizando un plano de referencia para ello.

<center>

![Pieza a diseñar](../img/PR-fijado-objetos/F3_2_7.png)  
*Figura 3.2.7. Pieza a diseñar*

</center>

Realizamos un croquis sobre el plano XZ de las dimensiones que vemos en boceto y lo extruimos 30 mm para obtener algo similar a lo de la Figura de la derecha.

<center>

![Croquis inicial pieza pieza a diseñar y su extrusión](../img/PR-fijado-objetos/F3_2_8.png)  
*Figura 3.2.8. Croquis inicial pieza pieza a diseñar y su extrusión*

</center>

Para crear el saliente que falta vamos a utilizar un plano de referencia que crearemos seleccionado el plano XY de referencia y que desplazaremos 30mm en el eje Z para situarlo a la altura del rectángulo superior. Esto lo vemos en la Figura 3.2.9. Es evidente que se puede hacer creando el croquis directamente sobre la cara, pero para ver el funcionamiento de este tipo de planos resulta perfectamente válido.

<center>

![Plano de referencia fijado a XY y desplazado](../img/PR-fijado-objetos/F3_2_9.png)  
*Figura 3.2.9. Plano de referencia fijado a XY y desplazado*

</center>

Seleccionando el plano creado y hacemos clic en boceto para tener uno nuevo. Creamos y dimensionamos un cuadrado siguiendo el proceso de la animación que tenemos en la Figura 3.2.10.

<center>

![Creación del nuevo boceto](../img/PR-fijado-objetos/F3_2_10.gif)  
*Figura 3.2.10. Creación del nuevo boceto*

</center>

Simplemente queda extruirlo y tenemos finalizada la pieza con una parte creada a partir de un plano de referencia, tal y como vemos en la Figura 3.2.11.

<center>

![3_2-Pieza-1](../img/PR-fijado-objetos/F3_2_11.png)  
*Figura 3.2.11. 3_2-Pieza-1*

</center>

Es evidente que esta misma situación podemos conseguirla de otras formas incluso más sencillas, pero la ventaja que tiene hacerlo mediante un plano es que el trozo creado puede recibir tareas independiente del objeto global relativas por ejemplo a la orientación del plano. En la animación de la Figura 3.2.12 vemos como hemos rotado el plano en dos ejes y como lo hace la figura. Al final de la animación podemos observar el uso del botón actualizar para que todos los cambios efectuados se reflejen en la vista 3D.

<center>

![Rotación del plano de referencia y sus consecuencias](../img/PR-fijado-objetos/F3_2_12.gif)  
*Figura 3.2.12. Rotación del plano de referencia y sus consecuencias*

</center>

Otro aspecto importante a tener en cuenta cuando trabajamos con planos de referencia es la forma de selección y hay que saber que no es lo mismo seleccionar objetos desde la ventana 3D que desde la vista combinada. Si hacemos un clic en alguna parte de un boceto en la ventana 3D solamente seleccionamos una parte del objeto, pero en cambio si hacemos clic sobre el objeto en 'Vista combinada' el objeto se selecciona entero. Esto lo observamos en la animación de la Figura 3.2.13.

<center>

![Selección desde ventana 3D y desde vista combinada](../img/PR-fijado-objetos/F3_2_13.gif)  
*Figura 3.2.13. Selección desde ventana 3D y desde vista combinada*

</center>

Aunque si podemos hacer un clic sobre un objeto en la vista 3D y una vez seleccionado otro clic (doble clic sobre un objeto) sobre el mismo objeto y quedará seleccionado completo.

Si escogemos una arista del boceto y hacemos clic en crear plano de referencia tendremos la situación de la animación de la Figura 3.2.14.

<center>

![Creación de plano de referencia a partir de selección de arista](../img/PR-fijado-objetos/F3_2_14.gif)  
*Figura 3.2.14. Creación de plano de referencia a partir de selección de arista*

</center>

En cambio si seleccionamos el boceto entero (un objeto) y hacemos lo mismo tendremos la situación que vemos en la Figura 3.2.15.

<center>

![Creación de plano a partir de seleccionar el objeto boceto](../img/PR-fijado-objetos/F3_2_15.png)  
*Figura 3.2.15. Creación de plano a partir de seleccionar el objeto boceto*

</center>

Esto mismo ocurre cuando tenemos un sólido y seguimos los mismos procedimientos.

Cuando hemos visto los tipos de referencia las combinaciones de referencia posibles (Figura 3.2.16) eran “Cualquiera” que es lo visto hasta ahora y “Cónica” que vamos a tratar a continuación.

<center>

![Tipos de combinaciones de referencia](../img/PR-fijado-objetos/F3_2_16.png)  
*Figura 3.2.16. Tipos de combinaciones de referencia*

</center>

Recodemos que una sección cónica o simplemente cónica es la curva resultante de la intersección entre un cono y un plano y que pueden ser una de las cuatro que vemos en la Figura 3.2.17.

<center>

![Cónicas](../img/PR-fijado-objetos/F3_2_17.png)  
*Figura 3.2.17. Cónicas*

</center>

Vamos a crear por ejemplo el boceto de una elipse y un círculo y lo hacemos creando un nuevo body, como vemos en la Figura 3.2.18.

<center>

![Boceto de cónicas](../img/PR-fijado-objetos/F3_2_18.png)  
*Figura 3.2.18. Boceto de cónicas*

</center>

Vamos a ver las diferencias entre seleccionar desde la ventana 3D y desde la ventana 'Vista combinada'. Si hacemos clic en la elipse, por ejemplo, y creamos un nuevo plano de referencia la tarea que se nos abre nos muestra opciones de fijación relacionadas con curvas (Frenet, Concéntrico,...), aunque también nos muestra las opciones vistas hasta ahora de Objetos XY, XZ e YZ. En la Figura 3.2.19 se muestra lo dicho.

<center>

![Opciones de fijación a curvas](../img/PR-fijado-objetos/F3_2_19.png)  
*Figura 3.2.19. Opciones de fijación a curvas*

</center>

Esto ocurre así porque no están seleccionados todos los objetos (lo vemos en “Seleccionar”) sino solo la elipse. Si ahora hacemos la selección del boceto desde la vista combinada quedarán seleccionados todos los objetos y la ventana muestra solo los Objetos XY, XZ e YZ y la selección es del boceto completo, como vemos en la Figura 3.2.20.

<center>

![Selección de cónicas desde vista combinada](../img/PR-fijado-objetos/F3_2_20.png)  
*Figura 3.2.20. Selección de cónicas desde vista combinada*

</center>

## <FONT COLOR=#007575>**Archivos y resultados finales**</font>
En la tabla siguiente tenemos los enlaces para descargar el archivo del diseño que hemos realizado como ejemplo de la sección, otros formatos de archivo y una imagen del resultado impreso de la pieza diseñada.

<center>

| Archivos | Captura del laminador | Imagen del resultado final |
|-:-|-:-|-:-|
| <br>[Diseño](../img/designs/3/3_2-Pieza-1.FCStd)</br><br>[STL](../img/designs/3/3_2-Pieza-1.stl)</br><br>[3MF](../img/designs/3/3_2-Pieza-1.3mf)</br><br>[STEP](../img/designs/3/3_2-Pieza-1.step)</br> | ![La pieza en PrusaSlicer](../img/PR-fijado-objetos/3_2-Pieza-1.png) | ![Pieza impresa en 3D](../img/PR-fijado-objetos/3_2-Pieza-1.jpeg) |

</center>

## <FONT COLOR=#007575>**Ejercicio propuesto**</font>
A partir de los datos indicados en la Figura 3.2.21 diseñar la pieza que se propone utilizando planos fijados a objetos.

<center>

![Pieza propuesta como ejercicio](../img/PR-fijado-objetos/F3_2_21.png)  
*Figura 3.2.21. Pieza propuesta como ejercicio*

</center>
