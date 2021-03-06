# 2022_drag__flex_reduction


## Organización
Los Datos csv están en las carpetas Dshape...
Dentro de la misma, hay archivos cuyo nombre es la frecuencia del ventilador a la que corresponden. Dicha frecuencia se relaciona con la velocidad del túnel, de acuerdo a una tabla indicada en analisis_flapflex.ipynb
En cada archivo, hay 7 columnas, de tiempo, fuerzas y momentos del sensor:

|tiempo|fx|fy|fz|mx|my|mz|
|---|---|---|---|---|---|---|

Dentro del directorio se encuentran archivos "ref" que sirven para fijar la referencia a la medida de fuerza. 
En analisis_flapflex.ipynb se utilizan las etiquetas de tiempo que corresponden a cada medida para asegurar consistencia.
Si hiciera falta, el comando:

    git ls-files | xargs -I{} bash -c 'touch "{}" --date=@$(git log -n1 --pretty=format:%ct -- "{}")'
    
recupera los tiempos correspondientes de creación.

## Figuras

Se generan figuras de la media temporal de $C_D$ de la figura de referencia "Dshape_ref_tape" en función del número de Reynolds.

Y también figuras de $C:D$ para cada uno de los 3 espesores de Mylar ensayados.

## Datos del perfil de velocidades en el túnel de vientos.

Relevamos para una serie de alturas el perfil de velocidades y se ilustra en analisis_flapflex.ipynb

