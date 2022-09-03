# Laboratorio 1 - Robótica Industrial No. 1
Para cumplir satisfactoriamente los requerimientos y tareas propuestas, se siguió el siguiente proceso:
## 1) Diseño de la herramienta
Se requería una herramienta que estuviera montada en el plato portaherramientas del robot IRB140. Esta debia sostener un marcador con el objetivo de seguir una secuencia que
anotara en un tablero las iniciales de algún nombre de los integrantes del grupo. 
### Proceso
Se observó el manual con las medidas del plato, despues se realizó la medición del marcador a usar, y finalmente se diseño la herramienta adjunta en este repositorio, dividida en dos partes, la base (base marcador.ipt) y la tapa de la herramienta (taoa.ipt). La geometría fue sencilla, lo cual facilitó su adaptación al RobotStudio.

![image](https://user-images.githubusercontent.com/112737454/188254964-bd5f101f-07b5-4d56-a55f-09272db3bbee.png)
![image](https://user-images.githubusercontent.com/112737454/188255034-605c3887-791c-4f62-ad0c-e29fcd8b9add.png)


## 2) Configuración de la herramienta en RobotStudio
Para no tener inconvenientes con importar archivos y geometrías, se creó un modelo en RobotStudio, esto a partir de cilindros y conos. Se generó la herramienta con su respectivo TCP y se añadió al robot.

![image](https://user-images.githubusercontent.com/112737454/188255135-ca8e6eff-37af-4204-a268-9a08102b1d0e.png)

### Tablero
En Inventor se creó el tablero que será la guía fundamental para el desrrollo de la superficie de trabajo. Ese modelo se importó a RobotStudio y se verificó que este se situra dentro del rango alcanzable del robot. El diseño trae las letras S y H

![image](https://user-images.githubusercontent.com/112737454/188255248-fe3c15c7-51b1-4eef-8b6a-75c61c696769.png)

## 3) Creación de objetos de trabajo en RobotStudio
Después de haber importado la geometría del tablero y ubicarlo en una posición favorable para el robot, se crea un objeto de trabajo en la sección de "Programación de trayectorias". Esta función permite unir la geometría de las letras al workspace de RobotStudio para su posterior programación en RAPID. Se establecieron 3 puntos para la creación de este objeto, los cuales eran las esquinas del tablero. Ya con este objeto se puede configurar las trayectorias.

![image](https://user-images.githubusercontent.com/112737454/188255648-b87bc589-d7ab-41a6-8827-7937dd195622.png)
![image](https://user-images.githubusercontent.com/112737454/188255934-ba33f6fc-20b0-4a70-ae06-11a2e03b3da6.png)

## 4) Generación de trayectorias
Finalmente, para la creación de trayectorias, se sigue en el bloque de funciones de "Programación de trayectorias", donde se selecciona la función de "Rutas" y se elige "Trayectoria automática". Posteriormente se elige la geometría de las letras en el tablero y se crea un algoritmo de posiciones a seguir por el robot. Finalmente estas trayectorias se reorganizan respecto al TCP de la herramienta.

![image](https://user-images.githubusercontent.com/112737454/188256082-23f2ff26-76eb-4156-a3b4-e7c2b8f03bc6.png)
![image](https://user-images.githubusercontent.com/112737454/188256409-6f764038-eef5-4adf-9f1e-65d3ba85bead.png)

## 5) Programación en RAPID
El último paso es programar y simular las trayectorias, para esto, se accede al panel de RAPID, donde podemos observar los "patch" o trayectorias generadas en la sección anteriores, Estas secuencias se tienen que unir a un main y finalmente se reproduce la secuencia.

![image](https://user-images.githubusercontent.com/112737454/188256533-d8ed5163-8227-4a16-bd73-5921fd6cff8a.png)
## 6) Resultados
El programa generado y probado en la sección anterior se exportó a un dispositivo de almacenamiento USB, y finalmente se probó en el robot IRB140 del laboratorio LabSIR. Primero ubicando el tablero respecto a la trayectoria (video 1) y después configurando el robot respecto al tablero (video 2). El resultado fue el siguiente

![image](https://user-images.githubusercontent.com/112737454/188256638-8ed185e2-7ccf-48ce-badb-e890c773401c.png)
![image](https://user-images.githubusercontent.com/112737454/188256641-3d53ebcb-1c1b-472e-9e47-2cd88282c98c.png)



