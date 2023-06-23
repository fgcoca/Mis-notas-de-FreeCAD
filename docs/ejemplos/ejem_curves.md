# <FONT COLOR=#8B008B>Curves</font>
Fundamentalmente se muestran ejemplos en los que intervienen elementos del banco de trabajo externo 'Curves' que se puede instalar desde el 'Administrador de complementos' de FreeCAD.

## <FONT COLOR=#007575>**Diseño de una pala**</font>
El desarrollo del ejemplo explica el funcionamiento de la herramienta *Barrido en 2 railes* del banco de trabajo 'Curves' y que aparece o bien en el menú Curves o en el icono siguiente de la barra de herramientas.

<center>

![Barrido en 2 railes](../img/9-curvas/9_3/iconos/sw2r.png)

</center>

Se trata de crear el perfil de una pala basándonos en el video de [MangoJelly Solutions for FreeCAD](https://www.youtube.com/@MangoJellySolutions/featured) titulado [Learn FreeCAD Curves Workbench [01] Sweep Along 2 Rails, Join Curve, Nurbs surfaces Practical Guide](https://www.youtube.com/watch?v=8JO3kU3Lg-U), que además nos va a servir para ver el uso de algunas otras herramientas.

Utilizaremos el banco de trabajo PartDesign para tener disponibles herramientas del mismo como la simetria y el plano de referencia.

Comenzamos por crear un boceto sobre el plano XY para formar los laterales de la pala similar al que vemos en la Figura siguiente.

<center>

![Boceto de los laterales de la pala](../img/ejemplos/curves/pala/pala_1.png)  

*Boceto de los laterales de la pala*

</center>

Para que resulte mas claro y sencillo el diseño vamos a cambiar el color de las líneas del boceto y el tamaño de los puntos de los vértices de las líneas, esto último hará mas fácil seleccionarlos posteriormente. En la animación de la siguiente vemos como hacerlo.

<center>

![Cambios en la visualización del boceto de los laterales de la pala](../img/ejemplos/curves/pala/pala_2.gif) 

*Cambios en la visualización del boceto de los laterales de la pala*

</center>

El paso siguiente va a consistir en crear la forma de la parte posterior de la pala mediante una B-spline. Esto lo vamos a hacer en un nuevo boceto creado sobre el plano XZ perpendicular al XY y tomando como referencia los puntos situados sobre el eje X de las curvas anteriores, es decir, creamos una proyección auxiliar de los mismo en el nuevo boceto utilizando la herramienta 'Geometria externa'. En la Figura siguiente vemos el proceso.

<center>

![Creación de B-spline para la parte trasera de la pala](../img/ejemplos/curves/pala/pala_3.gif) 

*Creación de B-spline para la parte trasera de la pala*

</center>

Ahora vamos a crear una simetria de esta B-spline respecto al eje Z que, como ya hemos visto, quedará aparentemente bien colocada pero en realidad los puntos finales no están unidos a los puntos que necesitamos. Unas vez establecida la restricción de coincidencia de los puntos anteriores unimos en una sola ambas splines. Para unir ambas líneas nos dirigimos al banco de trabajo 'Curves', seleccionamos ambas curvas y hacemos clic en el icono 'joinCurves', tal y como podemos observar en la animación siguiente.

<center>

![Simetría de la B-spline, restricción y unión de ambas curvas](../img/ejemplos/curves/pala/pala_4.gif)  

*Simetría de la B-spline, restricción y unión de ambas curvas*

</center>

***

> **<FONT COLOR=#008C00>- Consejo:</font>**
<center>
![](../img/bocadillos/b11.png)
</center>

***

Para crear la parte delantera de la pala vamos a necesitar de un plano auxiliar paralelo al plano XZ pero situado en los puntos finales de las primeras líneas. La creación del plano la vemos en la animación siguiente.

<center>

![Plano de referencia paralelo a Z que pasa por un punto](../img/ejemplos/curves/pala/pala_5.gif)

*Plano de referencia paralelo a Z que pasa por un punto*

</center>

Sobre este plano de referencia creamos un arco de círculo que tenga como puntos inicial y final los finales de las curvas laterales de la pala y le damos la curvatura deseada. Debemos obtener algo similar a lo que vemos en la figura siguiente.

<center>

![Perfil de pala completado](../img/ejemplos/curves/pala/pala_6.png)  

*Perfil de pala completado*

</center>

Nos dirigimos al banco de trabajo Part y vamos a crear una 'Superficie reglada' entre las dos líneas curvas laterales. La situación será la que vemos en la Figura siguiente.

<center>

![Superficie reglada entre alambres](../img/ejemplos/curves/pala/pala_7.png)  

*Superficie reglada entre alambres*

</center>

El siguiente paso es crear el barrido en dos railes y para ello procedemos como vemos en la animación de la Figura siguiente. Observamos como se crea una nube de puntos que sigue el contorno de la pala según las curvas creadas.

<center>

![Creamos el barrido en dos railes](../img/ejemplos/curves/pala/pala_8.gif) 

*Creamos el barrido en dos railes*

</center>

En la animación siguiente vemos algunos de los valores de los datos del nuevo objeto creado y como están definidos esos puntos como vectores.

<center>

![Datos de la nube de puntos](../img/ejemplos/curves/pala/pala_9.gif)  

*Datos de la nube de puntos*

</center>

Para crear la superficie de referencia de la pala vamos a utilizar la herramienta 'Aproximar' para lo que manteniendo seleccionado el objeto Sweep_2_rails en el árbol de objetos hacemos clic en el icono de la herramienta y veremos como aparece la superficie curva que se adapta a nuestros perfiles de diseño y que podemos ver en la Figura siguiente.

<center>

![Superficie curva de la pala](../img/ejemplos/curves/pala/pala_10.png)  

*Superficie curva de la pala*

</center>

Podemos dar un determinado grosor a la pala mediante la herramienta extruir del banco de trabajo Part, pero vamos a hacerlo utilizando la herramienta Offset o desplazamiento, tal y como vemos a continuación.

<center>

![Dando espesor a la superficie curva de la pala](../img/ejemplos/curves/pala/pala_11.gif)  

*Dando espesor a la superficie curva de la pala*

</center>

En este momento es conveniente ocultar la superficie generadora ya que no lo hace de forma automática y nos puede originar alguna confusión.

Para finalizar la pala tenemos que añadir un punto de conexión con el mango. Desde el banco de trabajo Part creamos un tubo de longitud 100mm con radio exterior 20mm e interior 12mm. Posicionamos el tubo para que esté colocado en su lugar y lo unimos a la superficie curva, teniendo así la pala final que vemos en la Figura siguiente.

<center>

![Pala](../img/ejemplos/curves/pala/pala_13.png)  

*Figura 9.3.21. Pala*

</center>

En el enlace siguiente tenemos el Archivo fuente de FreeCAD:

* [Enlace para descarga del archivo fuente de FreeCAD](../img/designs/9/pala.FCStd)

## <FONT COLOR=#007575>**Diseño de un tubo sencillo**</font>
El desarrollo del ejemplo introduce el funcionamiento de las herramientas *PipeShell* del banco de trabajo 'Curves' y que aparece o bien en el menú Curves o en los iconos siguiente de la barra de herramientas.

<center>

![Perfil para tuberia](../img/9-curvas/9_3/iconos/Curves_PipeshellProfile.svg) ![Barrido para tuberia](../img/9-curvas/9_3/iconos/Curves_Pipeshell.svg)

</center>

Vamos a comenzar por crear un tubo sencillo que va a recorrer una trayectoria fijada por una B-spline. Comenzamos seleccionando el banco de trabajo Sketcher y vamos a dibujar un círculo en un boceto creado en el plano XY y una B-spline creada sobre el plano XZ. El boceto del círculo puede contener otros objetos. En la Figura siguiente vemos la situación incial.

<center>

![Bocetos iniciales para crear un tubo sencillo](../img/ejemplos/curves/tubo_simple/tubo_1.png)  

*Bocetos iniciales para crear un tubo sencillo*

</center>

El siguiente paso es convertir el círculo en un perfil, que lo hacemos seleccionando el círculo y desde Curves hacemos clic en el icono Perfil y veremos como el boceto original se oculta y aparece el objeto Profile (Perfil) en color azul sin que aparezca el resto del boceto. Además, como vemos en la animación siguiente los cambios en los objetos utilizados del boceto inicial se reflejan en el Profile creado. Se pueden crear varios objetos Profile para realizar un barrido.

<center>

![Creación del objeto Profile](../img/ejemplos/curves/tubo_simple/tubo_2.gif)  

*Creación del objeto Profile*

</center>

Realizamos el barrido haciendo la selección de objetos en el siguiente orden: primero seleccionamos el Profile desde el arbol de objetos y después el boceto de la trayectoria desde la ventana gráfica mientras mantenemos pulsada la tecla Ctrl, para finalizar hacemos clic en el icono de barrido y se nos crean una serie de objetos siguiendo la trayectoria. En la animación siguiente vemos como hacer esto, como modificar el número de objetos creado y finalmente como crear el tubo.

<center>

![Creación del tubo](../img/ejemplos/curves/tubo_simple/tubo_3.gif)  

*Creación del tubo*

</center>
Ahora podemos realizar cambios tanto en el boceto origen del Profile como en el del barrido y quedarán reflejados en el tubo final, tal y como se observa en la animación siguiente.

<center>

![Modificaciones en el tubo](../img/ejemplos/curves/tubo_simple/tubo_4.gif)  

*Modificaciones en el tubo*

</center>

Si en lugar de un tubo queremos crear un sólido lo único que tenemos que hacer es poner a 'True' la propiedad 'Solid' del objeto PipeShell.

A la superficie creada en forma tubular le podemos dar un espesor con la herramienta Ofsset del menú Part.

Un primer potencial de estas herramientas es que el boceto inicial puede ser un B-spline de la que podemos realizar un barrido. En la animación siguiente vemos como funciona lo dicho.

<center>

![Barrido de un boceto con B-spline](../img/ejemplos/curves/tubo_simple/tubo_5.gif)  

*Barrido de un boceto con B-spline*

</center>

En el enlace siguiente tenemos el Archivo fuente de FreeCAD:

* [Enlace para descarga del archivo fuente de FreeCAD](../img/designs/9/tubo_simple.FCStd)

## <FONT COLOR=#007575>**Diseño de una máscara facial**</font>
El desarrollo del ejemplo introduce el funcionamiento de la herramienta *Discretizar curvas/superficies* del banco de trabajo 'Curves' y que aparece o bien en el menú Curves o en el icono siguiente de la barra de herramientas.

<center>

![Discretizar](../img/9-curvas/9_3/iconos/Curves_Discretize.svg)

</center>

### <FONT COLOR=#AA0000>Discretizar e interpolar</font>

Vamos a comenzar por crear un par de curvas desde el banco de trabajo Sketcher en un nuevo documento. La primera la creamos sobre el plano XY utilizando la herramiento B-spline para obtener algo similar a lo que vemos en la Figura siguiente.

<center>

![Boceto de curva con B-spline sobre plano XY](../img/ejemplos/curves/mascara/m_1.png) 

*Boceto de curva con B-spline sobre plano XY*

</center>

La segunda curva la podemos crear a partir de la primera rotandola o creando otra en el plano XZ que es como lo vamos a hacer para obtener una curva similar a la de la Figura siguiente que es un poco diferente a la primera.

<center>

![Boceto de curva con B-spline sobre plano XZ](../img/ejemplos/curves/mascara/m_2.png) 

*Boceto de curva con B-spline sobre plano XZ*

</center>

El siguiente paso va a ser crear un desplazamiento negativo en el eje Y de la nueva curva de 60mm y vamos a rotar la primera curva 50º respecto al eje X. En la animación siguiente vemos como hacer estas tareas.

<center>

![Reposicionando los bocetos](../img/ejemplos/curves/mascara/m_3.gif) 

*Reposicionando los bocetos*

</center>

La idea va a ser crear una superficie entre estas dos curvas. Pero antes de acometer la tarea vamos a utilizar la herramienta discretizar sobre las curvas comenzando por la primera de ellas que sabemos que va a ser un flanco o arista. Al utilizar la herramienta rompemos la curva en un determinado número de puntos. En la animación siguiente vemos el uso y como configurar para ver mas claramente esos puntos ocultando el boceto generador. En la misma también vemos como modificar el número de puntos y como hacerlos de mayor tamaño.

<center>

![Discretización de la primera curva](../img/ejemplos/curves/mascara/m_4.gif)  

*Discretización de la primera curva*

</center>

El algoritmo matemático de cálculo de los puntos se puede cambiar en la propiedad 'Algorithm' de la discretización realizada siendo las opciones posibles las siguientes:

* **Number:** Establecemos el número de puntos de la discretización.
* **QuasiNumber:** Establecemos el número de puntos. Establezcamos que un número perfecto es un entero positivo que es igual a la suma de sus divisores propios (que no sean el propio número) positivos (es amigo de si mismo). Por ejemplo 6 es perfecto porque sus divisores 1, 2 y 3 suman 6. Los siguientes números prefectos son 28, 496 y 8128. Un número cuasi perfecto es el que al sumar todos sus divisores menos el mismo nos da como resultado un número que es una unidad menor que el propio número. Por ejemplo, los divisores de 8 son 1, 2 y 4 que sumados dan 7, uno menos que 8. Finalmente un número es cuasi perfecto si la suma de sus divisores propios es uno mas que el propio número. Hasta el momento no se ha encontrado ninguno de estos números.
* **Distance:** La propiedad 'Number' cambia a 'Distance' para establecer la distancia entre los puntos. Según sea menor la distancia entre puntos se colocarán mayor número de los mismos. Cuando cambiamos de algoritmo se conservan las configuraciones de cada tipo.
* **Deflection:** Establece el número de puntos según el valor de la desviación establecido, proporcionando una secuencia de puntos de acuerdo con el grado de desviación de la curva original. En el foro de FreeCAD [Deviation and Angular deflection](https://forum.freecad.org/viewtopic.php?style=4&p=389881#p389881) hay mas información al respecto.
* **QuasiDeflection:** Similar a 'Deflection'.
* **Angular-Curvature:** Crea una secuencia de puntos con los parámetros Angular (Angular), Curvature (Curvatura) y Mínimum (Mínimo).

Dejamos finalmente la primera curva discretizada a 20 puntos y discretizamos la segunda a 10 puntos, aumentando también el tamaño de los mismos, y tendremos la situación que vemos en la Figura siguiente.

<center>

![Las dos curvas discretizadas](../img/ejemplos/curves/mascara/m_5.png)  

*Las dos curvas discretizadas*

</center>

La siguiente tarea que vamos a realizar es interpolar puntos y para ello procedemos a seleccionar los puntos en el siguiente orden: marcamos tres puntos sobre la primera curva realizando la selección de izqueirda a derecha y posteriormente seleccionamos otros tres de derecha a izquierda en la segunda curva. El orden de selección establece la trayectoria de la interpolación. En la animación siguiente vemos el proceso y el resultado.

<center>

![Interpolación](../img/ejemplos/curves/mascara/m_6.gif)  

*Interpolación*

</center>

Creamos otra interpolación como la de la animación siguiente.

<center>

![Interpolación](../img/ejemplos/curves/mascara/m_7.gif)  

*Interpolación*

</center>

Ahora nos movemos al banco de trabajo Part y seleccionamos ambas interpolaciones manteniendo la tecla Ctrl pulsada para crear una superficie reglada como la que vemos en la Figura siguiente.

<center>

![Superficie reglada entre las interpolaciones](../img/ejemplos/curves/mascara/m_8.png)  

*Superficie reglada entre las interpolaciones*

</center>

### <FONT COLOR=#AA0000>Máscara facial</font>
Comenzamos por crear, sobre el plano XY, los seis bocetos que vemos en la Figura siguiente para que mantengan la forma aproximada que vemos. Los números asociados a los ejes que aparecen en la figura son las posiciones establecidas para los bocetos.

<center>

![Bocetos iniciales máscara facial](../img/ejemplos/curves/mascara/m_9.png) 

*Bocetos iniciales máscara facial*

</center>

Ahora procedemos a discretizarlos a 15 puntos todos ellos y lo podemos hacer de una sola vez teniendo seleccionados todos los bocetos, tal y como vemos en la animación siguiente.

<center>

![Discretización y número de puntos](../img/ejemplos/curves/mascara/m_10.gif)  

*Discretización y número de puntos*

</center>

**Es MUY IMPORTANTE que todos los bocetos tengsan el mismo número de puntos o la superficie de aproximación a los mismos no va a tener éxito.**

Si ocultamos los bocetos vemos una nube de puntos que es la que nos va a permitir crear una aproximación, pero para hacerlo necesitamos que todos los puntos sean un único objeto, lo que conseguimos facilmente creando un grupo y moviendo todos los objetos discretizados al mismo. En la animación siguiente se observa este proceso.

<center>

![Ocultar bocetos, mover las discretizaciones a un grupo y crear la aproximación](../img/ejemplos/curves/mascara/m_11.gif)  

*Ocultar bocetos, mover las discretizaciones a un grupo y crear la aproximación*

</center>

Por ahora podemos dejar visibles los bocetos para que nos ayude a seguir el perfil de la superficie.

El siguiente paso es dirigirnos al banco de trabajo Part y crear un offset de la superficie para tener una primera versión de la máscara en 3D.

Ahora nos dirigimos la banco de trabajo Part y creamos dos elipsoides desde 'Crear primitivas...'. Las posicionamos en el lugar deseado para crear el orificio de los ojos, creamos una unión entre ambas alipsoides y posteriormente una operación de corte entre el objeto ofsett y la unión de las elipsoides. El resultado final, que es muy mejorable, lo vemos en la Figura siguiente.

<center>

![Máscara final](../img/ejemplos/curves/mascara/m_12.png)  

*Máscara final*

</center>

En el enlace siguiente tenemos el Archivo fuente de FreeCAD:

* [Enlace para descarga del archivo fuente de FreeCAD](../img/designs/9/mascara.FCStd)

## <FONT COLOR=#007575>**Combinación de superficies**</font>
Vamos a comenzar por un conjunto de 6 bocetos con una disposición similar a la de la figura siguiente.

<center>

![Boceto de partida](../img/ejemplos/curves/combina/c1.png)  

*Boceto de partida*

</center>

### <FONT COLOR=#AA0000>Primeros pasos</font>
Nos movemos a Part y creamos superficies regladas entre aristas para cada boceto de forma que cada uno de ellos se convierta en una superficie plana. En la animación siguiente vemos el final de este proceso y la ocultación de los bocetos originales.

<center>

![Creación de superficies regladas](../img/ejemplos/curves/combina/c2.gif) 

*Creación de superficies regladas*

</center>

Ahora nos movemos a Curves y vamos a crear superficies que se combinen con las anteriores utilizando la herramietna BlendSurface. En la animación siguiente vemos como se realiza el proceso entre algunas de ellas.

<center>

![Creación de superficies combinadas entre las regladas](../img/ejemplos/curves/combina/c3.gif) 

*Creación de superficies combinadas entre las regladas*

</center>

### <FONT COLOR=#AA0000>Propiedades de BlendSurface</font>
Antes de continuar vamos a ver algunas propiedades de la superficies combinadas y como afectan al resultado final.

* **Continuity:** establece mediante un número entero la continuidad entre la cara y la arista. En la animación siguiente observamos como se puede establecer la continuidad a 0 o ninguna y como al aumentar uno de los valores aumenta el grado de continuidad de la curva con la arista que le corresponde.

<center>

![Propiedad Continuity](../img/ejemplos/curves/combina/c4.gif)  

*Propiedad Continuity*

</center>

Con esta propiedad podemos adaptar significativamente la curva a nuestras necesidades. También observamos que a partir de un determinado valor los incrementos ya no afectan al resultado, dependiendo esto se la curva concreta.

* **Scale:** valores de la escala para cada arista en función del tipo de escalado y el número de muestras que establezcamos. Si ponemos a cero el número de muestras el resultado es el mismo que poner ambos valores de continuidad a cero. Las opciones de autoescalado son minimizar la curvatura, establecer el número de polos y manual.

El siguiente paso lo vamos a dar desde el banco de trabajo Surface por lo que nos movemos al mismo y procedemos a rellenar el hueco central utilizando la herramienta Infill (relleno). En la siguiente animación vemos el proceso.

<center>

![Infill del banco de trabajo Surface](../img/ejemplos/curves/combina/c5.gif) 

*Infill del banco de trabajo Surface*

</center>

En el enlace siguiente tenemos el Archivo fuente de FreeCAD:

* [Enlace para descarga del archivo fuente de FreeCAD](../img/designs/9/combinar.FCStd)

### <FONT COLOR=#AA0000>Herramientas extraer caras y textura de cebra</font>
En un ejemplo similar partimos de una serie de cubos distribuidos según vemos en la figura siguiente. En estos se ha marcado una cara de cada cubo para extraerla mediante la herramienta 'Extraer subforma' de la barra de herramientas 'Miscelanea' del banco de trabajo 'Curves'.

<center>

![Distribución de cubos](../img/ejemplos/curves/combina/c6.png)  

*Distribución de cubos*

</center>

Para marcar las caras de un color se utiliza la herramienta 'Color por cara' de Part.

Una vez extraidas las caras se les ha vuelto a dar color para establecer la correspondencia con su cubo y el resultado lo vemos en la figura siguiente que es una situación equivalente a la de las superficies regladas.

<center>

![Caras extraidas de los cubos](../img/ejemplos/curves/combina/c7.png)  

*Caras extraidas de los cubos*

</center>

El paso siguiente es crear y configurar las superficies combinadas. En el ejemplo resuelto que se da más adelante podemos consultar las configuraciones establecidad para cada una de ellas. En la figura siguiente vemos el resultado al finalizar esta tarea.

<center>

![Caras extraidas de los cubos y superficies combinadas](../img/ejemplos/curves/combina/c8.png)  

*Caras extraidas de los cubos y superficies combinadas*

</center>

En esta ocasión antes de hacer un relleno desde Surface vamos a crea una superficie combinada pero esta vez entre dos de las superficies creadas anteriormente. En la animación siguiente vemos el proceso completo para obtener una curiosa forma curvada.

<center>

![Superficie combinada creada entre superficies combinadas](../img/ejemplos/curves/combina/c9.gif) 

*Superficie combinada creada entre superficies combinadas*

</center>

A continuación creamos dos rellenos desde el Surface y los configuramos para obtener la figura final que vemos en la animación siguiente.

<center>

![Objeto final obtenido](../img/ejemplos/curves/combina/c10.gif)  

*Objeto final obtenido*

</center>

En el enlace siguiente tenemos el Archivo fuente de FreeCAD:

* [Enlace para descarga del archivo fuente de FreeCAD](../img/designs/9/combinar1.FCStd)

A continuación vemos una animación en la que se utiliza la herramienta 'Textura de cebra' que nos permite apreciar las diferentes curvaturas de las partes de la pieza final.

<center>

![Uso de textura de cebra](../img/ejemplos/curves/combina/c11.gif)  

*Uso de textura de cebra*

</center>

## <FONT COLOR=#007575>**Diseño de una botella de detergente líquido**</font>
Lo haremos siguiendo el tutorial de Mariana Badea [Make a Bottle Part Design Curves](https://www.youtube.com/watch?v=Gmu3y9XtXpU&t=182s) y aprenderemos el manejo de la herramienta Isocurva.

### <FONT COLOR=#AA0000>Inicio</font>
El proceso comienza por crear cuatro planos paralelos al plano XY a las siguientes distancias: 55, 105, 140 y 170mm que vamos a etiquetar indicando esas distancias en el eje Z. En la figura siguiente tenemos el aspecto final de estos planos y se ha destacado la etiqueta del último creado.

<center>

![Creación de planos paralelos al plano XY](../img/ejemplos/curves/botella_detergente/b1.png)  

*Creación de planos paralelos al plano XY*

</center>

Por el momento podemos ocultar los planos y ejes de referencia así como los planos creados. Comenzamos por crear el boceto de la figura siguiente sobre el plano de referencia XY.

<center>

![Creación de boceto en el plano XY](../img/ejemplos/curves/botella_detergente/b2.png)  

*Creación de boceto en el plano XY*

</center>

Mostramos el plano con z=55 y sobre el mismo creamos un boceto similar al anterior con la única diferencia en su cota entre centros que ahora será de 35mm, tal y como se aprecia en la figura siguiente.

<center>

![Creación de boceto en el plano z=55](../img/ejemplos/curves/botella_detergente/b3.png)  

*Creación de boceto en el plano z=55*

</center>

Repetimos el proceso en el plano con Z=105 y creamos el boceto de la figura siguiente, que es exactamente igual que el anterior.

<center>

![Creación de boceto en el plano z=105](../img/ejemplos/curves/botella_detergente/b4.png)  

*Creación de boceto en el plano z=105*

</center>

Continuamos creando el boceto de la figura siguiente sobre el plano situado en z=140.

<center>

![Creación de boceto en el plano z=140](../img/ejemplos/curves/botella_detergente/b5.png)  

*Creación de boceto en el plano z=140*

</center>

Ahora creamos el boceto de la imagen siguiente en el plazo z=170.

<center>

![Creación de boceto en el plano z=170](../img/ejemplos/curves/botella_detergente/b6.png) 

*Creación de boceto en el plano z=170*

</center>

Vamos a proceder a crear una proyección aditiva de la forma que vemos en la animación siguiente.

<center>

![Creación de proyección aditiva](../img/ejemplos/curves/botella_detergente/b7.gif)  

*Creación de proyección aditiva*

</center>

Seleccionamos el plano superior del objeto creado para crear un boceto centrado en el origen consistente en un círculo de radio 12mm, cerramos la tarea y extruimos 18mm, teniendo el aspecto que vemos en la figura siguiente.

<center>

![Creación de la boca de la botella, paso 1](../img/ejemplos/curves/botella_detergente/b8.png) 

*Creación de la boca de la botella, paso 1*

</center>

Sobre el mismo plano que el boceto anterior vamos a crear otro boceto que será un círculo de radio 15mm. Lo que pretendemos es crear una anilla alrededor del cilindro anterior separada del plano sobre el que se ha creado el boceto, por lo que debemos desactivar la propiedad 'Map Mode' y después elevar en z el boceto hasta la altura requerida, en este caso será 173mm. Una vez realizadas las tareas anteriores extruimos el boceto 1,5mm y tendremos el aspecto que vemos al final de la animación siguiente.

<center>

![Creación de la boca de la botella, paso 2](../img/ejemplos/curves/botella_detergente/b9.gif) 

*Creación de la boca de la botella, paso 2*

</center>

El estado actual del diseño lo vemos en la figura siguiente.

<center>

![Botella sólida inicial finalizada](../img/ejemplos/curves/botella_detergente/b9b.png)  

*Botella sólida inicial finalizada*

</center>

### <FONT COLOR=#AA0000>Zona de agarre lateral</font>
Comenzamos por crear un plano paralelo al XY desplazado en el eje Z 80 mm y hacemos visibles los planos a 55, 105 y 140 mm. Mediante la herramienta 'Slice apart' del banco de trabajo Part vamos a crear diferentes secciones de la botella para llegar a obtener lo que vemos en la animación siguiente.

<center>

![Aplicación de la herramienta 'Slice apart'](../img/ejemplos/curves/botella_detergente/b10.gif) 

*Aplicación de la herramienta 'Slice apart'*

</center>

Ahora creamos un alambre a partir de las aristas creadas por el corte del plano z=80mm, tal y como vemos en la animación siguiente, donde utilizamos la herramienta 'Generador de forma' de Part.

<center>

![Creación de alambre en z=80](../img/ejemplos/curves/botella_detergente/b11.gif)  

*Creación de alambre en z=80*

</center>

Algunos de los elementos de los grupos 'Explode Slice' ya no son necesarios por lo que los vamos a eliminar tal y como vemos en la animación siguiente, donde podemos ver como la sección intermedia desaparece aunque permanece el elemento alambre en su posición.

<center>

![Eliminación de elementos](../img/ejemplos/curves/botella_detergente/b11.gif)  

*Eliminación de elementos*

</center>

El paso siguiente va a consistir en crear una Isocurva a partir de la superficie curva del Slice central. En la animación siguiente vemos como hacerlo además de ver la configuración de la Isocurva (aplicamos 8 divisiones verticales) y como crear dos nuevos alambres a partir de dos de estas divisiones.

<center>

![Creación de Isocurva y nuevos alambres](../img/ejemplos/curves/botella_detergente/b12.gif)  

*Creación de Isocurva y nuevos alambres*

</center>

Procedemos a ocultar la isocurva y a crear nuevos elementos Slice a partir de los alambres. En la animación siguiente vemos el proceso de creación y se destaca el trozo final de alambre que nos queda.

<center>

![Creación de elementos Slice a partir de alambres](../img/ejemplos/curves/botella_detergente/b13.gif) 

*Creación de elementos Slice a partir de alambres*

</center>

Ocultamos el Slice que no nos interesa y creamos un nuevo alambre con los trozos nuevos y siguiendo todo el contorno de la botella como vemos en la animación siguiente.

<center>

![Creación de un nuevo alambre](../img/ejemplos/curves/botella_detergente/b14.gif)  

*Creación de un nuevo alambre*

</center>

Todos los elementos Exploded Slice creados así como los alambres anteriores ya no van a sernos de utilidad por lo que podemos proceder a eliminarlos para simplificar el árbol de objetos.

Ahora vamos a crear una serie de planos que nos permitan colocar los bocetos que definirán el perfil del rebaje que realizaremos en la botella para facilitar el agarre de la misma.

* El primer plano lo vamos a colocar normal al alambre creado y lo situaremos en el vértice final del mismo, tal y como se aprecia en la animación siguiente.

<center>

![Primer plano de referencia](../img/ejemplos/curves/botella_detergente/b15.gif)  

*Primer plano de referencia*

</center>

* El segundo plano lo colocaremos de forma similar al anterior pero en el otro extremo del alambre, tal y como vemos en la animación siguiente.

<center>

![Segundo plano de referencia](../img/ejemplos/curves/botella_detergente/b16.gif)  

*Segundo plano de referencia*

</center>

* El tercer plano de referencia lo colocamos en uno de los trozos de alambre de la parte curva opuesta y de forma similar a los anteriores, tal y como se puede apreciar en la animación siguiente.

<center>

![Tercer plano de referencia](../img/ejemplos/curves/botella_detergente/b17.gif)  

*Tercer plano de referencia*

</center>

Seleccionamos el tercer plano que hemos creado y sobre el mismo dibujamos el boceto que vemos en la figura siguiente. Hemos puesto el Estilo de dibujo en modelo de alambres y la imagen se toma sobre una vista frontal del boceto.

<center>

![Boceto sobre el tercer plano de referencia](../img/ejemplos/curves/botella_detergente/b18.png) 

*Boceto sobre el tercer plano de referencia*

</center>

Sobre el primer y el segundo plano dibujamos un boceto que sea igual en ambos y como el que vemos en la figura siguiente.

<center>

![Boceto sobre el primer y segundo plano de referencia](../img/ejemplos/curves/botella_detergente/b19.png) 

*Boceto sobre el primer y segundo plano de referencia*

</center>

En la versión con la que se ha realizado el ejercicio presenta continuos errores de conexión en los planos de referencia que tendremos que ir arreglando con las opciones de conexionado que nos deja pero siempre trabajando sobre el mismo alambre, es decir, ocultando las copias que se van creando o mejor aún, aliminando las copias que se crean. Al final debemos tener un boceto en cada plano en una situación como la que vemos en la figura siguiente, donde podemos ver el árbol de objetos en el estado que tiene en este momento del diseño.

<center>

![Vista con los tres bocetos creados](../img/ejemplos/curves/botella_detergente/b20.png) 

*Vista con los tres bocetos creados*

</center>

El siguiente paso va a consistir en crear un vaciado mediante la herramienta 'Tubo sustractivo' que nos permita definir la zona que estamos trabajando. Para ello iniciamos la herramienta con una arista del boceto del primer plano seleccionada para que se nos muestre la ventana de 'Parámetros del tubo' donde indicaremos que el recorrido del barrido se hará según marca el alambre y añadiendo los dos bocetos restantes para realizar una 'Transformación de la sección' de tipo Multisección. En la animación siguiente vemos el proceso completo y el resultado que se obtiene.

<center>

![Creación de la zona de agarre](../img/ejemplos/curves/botella_detergente/b21.gif)  

*Creación de la zona de agarre*

</center>

### <FONT COLOR=#AA0000>Sistema antigoteo</font>
A estas alturas del diseño la situación actual es que las divisiones horizontales han desaparecido, seguramente porque se han eliminado, pero no importa demasiado porque es bastante fácil recuperar el estado que teniamos al princicipio. En la figura siguiente vemos como la cara curva de la izquierda ya es un sola (la destacada en rojo) y no tiene divisiones horizontales (las destacadas en verde).

<center>

![Superficie sin divisiones horizontales](../img/ejemplos/curves/botella_detergente/b22.png) 

*Superficie sin divisiones horizontales*

</center>

Vamos a proceder a crear de nuevo las divisiones perdidas y para ello desde el menú Part vamos a crear planos utilizando la herramienta 'Crear primitivas' que vamos a situar a la misma altura que tenian los de partida, es decir cuatro planos paralelos al plano XY a las siguientes distancias: 55, 105, 140 y 170mm. En la animación siguiente vemos como crear estos planos.

<center>

![Creación de nuevos planos para dividir en vertical el objeto 3D](../img/ejemplos/curves/botella_detergente/b23.gif) 

*Creación de nuevos planos para dividir en vertical el objeto 3D*

</center>

El siguiente paso es crear las divisiones utilizando la herramienta Slice del menú pieza, tal y como observamos en la animación siguiente, dejando preparado de nuevo el objeto 3D para continuar con nuestro diseño.

<center>

![Creación de las divisiones con Slice](../img/ejemplos/curves/botella_detergente/b24.gif)  

*Creación de las divisiones con Slice*

</center>

Ahora vamos a diseñar sobre la superficies curvas que vemos destacadas en la figura siguiente, que convertiremos en Isocurvas.

<center>

![Superficies a convertir en Isocurvas](../img/ejemplos/curves/botella_detergente/b25.png)  

*Superficies a convertir en Isocurvas*

</center>

Creamos las Isocurvas en ambas superficies y las configuramos con 7 divisiones verticales. Posteriormente nos dirigimos al banco de trabajo Part desde donde creamos los alambres que vemos en la animación siguiente. En horizontal corresponde con las divisiones 4, 6, 8 y 10 y las verticales las que quedan a izquierda y derecha de la central.

<center>

![Creación de los alambres](../img/ejemplos/curves/botella_detergente/b26.gif)  

*Creación de los alambres*

</center>

Seguidamente vemos en la animación como crear cortes entre los alambres anteriores eliminando los que no nos interesan para quedarnos solamente con los trozos que vamos a utilizar. Se muestran solamente las dos últimas instancias dado que el método de creación es el mismo para las dos superiores.

<center>

![Creación de cortes en los alambres](../img/ejemplos/curves/botella_detergente/b27.gif) 

*Creación de cortes en los alambres*

</center>

A partir de los trozos obtenidos volvemos a crear alambres de cada uno de ellos y procedemos a eliminar todos los Slices y las Isocurvas que ya no nos sirven para nada. En la animación siguiente vemos el proceso y como se eliminan los elementos que aún permanecen tras el primer borrado.

<center>

![Creación de alambres y eliminación de operaciones](../img/ejemplos/curves/botella_detergente/b28.gif) 

*Creación de alambres y eliminación de operaciones*

</center>

Seleccionando cada alambre creamos un plano de referencia desde Partdesign que sea normal a la arista y que esté atado al punto final del alambre. Sobre este plano dibujamos un círculo de radio 3mm con el que creamos un vaciado mediante la herramienta 'Tubo sustractivo'. En la animación siguiente vemos el proceso seguido para el alambre superior. El resto de vaciados se han obtenido siguiendo exactamente el mismo procedimiento.

<center>

![Vaciados antigoteo a parti de alamabres](../img/ejemplos/curves/botella_detergente/b29.gif) 

*Vaciados antigoteo a parti de alamabres*

</center>

En la figura siguiente vemos el estado actual de la botella, que por ahora sigue siendo sólida.

<center>

![Botella sólida final sin remates](../img/ejemplos/curves/botella_detergente/b30.png) 

*Botella sólida final sin remates*

</center>

### <FONT COLOR=#AA0000>Creación del recipiente</font>
El siguiente paso que vamos a dar es vaciar la botella por dentro para así crear el recipiente. Comenzamos por crear tres planos paralelos al plano de referencia XY y colocados a una distancia de 6, 105 y 167mm del mismo en Z. En la figura siguiente vemos los tres planos creados.

<center>

![Planos para crear el vaciado interno](../img/ejemplos/curves/botella_detergente/b31.png)  

*Planos para crear el vaciado interno*

</center>

Sobre el primer y segundo planos creamos el boceto que vemos en la figura siguiente.

<center>

![Boceto sobre el primer y segundo planos para crear el vaciado interno](../img/ejemplos/curves/botella_detergente/b32.png) 

*Boceto sobre el primer y segundo planos para crear el vaciado interno*

</center>

Sobre el tercero de los planos creamos el boceto de la figura siguiente.

<center>

![Boceto sobre el tercer plano para crear el vaciado interno](../img/ejemplos/curves/botella_detergente/b33.png) 

*Boceto sobre el tercer plano para crear el vaciado interno*

</center>

En la figura siguiente vemos los bocetos creados mostrados sobre en modelo de alambres como estilo de dibujo para poder verlos.

<center>

![Bocetos para crear el vaciado interno](../img/ejemplos/curves/botella_detergente/b34.png) 

*Bocetos para crear el vaciado interno*

</center>

El siguiente paso es crear una 'Proyección sustractiva' utilizando como perfil los tres bocetos creados. El proceso a seguir lo vemos en la animación siguiente.

<center>

![Proyección sustractiva para crear el vaciado interno](../img/ejemplos/curves/botella_detergente/b35.gif) 

*Proyección sustractivas para crear el vaciado interno*

</center>

Lógicamente el vaciado se crea en el volumen comprendido entre el primer plano y el tercer plano. Para vaciar la boca vamos a crear el bocedto de la figura siguiente sobre el plano situado a 167mm, que coincide con la parte superior del vaciado anterior.

<center>

![Boceto para crear el vaciado de la boca](../img/ejemplos/curves/botella_detergente/b36.png) 

*Boceto para crear el vaciado de la boca*

</center>

Creamos un vaciado invertido a través de todos y ocultamos todos los elementos anteriores y obtenemos la botella. Las operaciones finales van a consistir en aplicar operaciones de redondedo a diferentes aristas para obtener un mejor resultado.

En el enlace siguiente tenemos el Archivo fuente de FreeCAD:

* [Enlace para descarga del archivo fuente de FreeCAD](../img/designs/9/botella.FCStd)

En la figura siguiente vemos el aspecto final que se ha dado al diseño.

<center>

![Botella final](../img/ejemplos/curves/botella_detergente/b37.png)

*Botella final*

</center>
