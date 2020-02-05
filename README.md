# ciudades_bosque
Aplicación para coordinar la reforestación de ciudades

## Introducción

El reforestar ciudades es algo sencillo, y cada día más personas buscan alguna forma de participar en revertir los niveles actuales de CO2 y su efecto en el cambio climático.

Esta aplicación funciona como una forma de coordinar el proceso de:

- Recolectar semillas de bosques y parques urbanos
- Germinarlos de forma casera y en pequeños espacios
- Encontrar espacios aptos para sembrar árboles y arbustos
- Conectar con voluntarios para sembrar las plántulas
- Seguir la historia, eficacia y calcular el CO2 reducido por la comunidad

## Diseño

Para simplificar la construcción de la aplicación, vamos a utilizar Node-Red con base de datos SQL, y a futuro formas automatizadas para correr el contenido de forma sencilla.

### CRUD

El diseño de la base de datos se basa en la necesidad de manejar colecciones de:

|Objeto|Descripción|Propiedades|
|------|-----------|-----------|
|Vivero|Voluntarios administran mini-viveros para producir plántulas|Dirección, Contacto, Plántulas|
|Especie|Queremos saber un poco sobre la especie a plantar, espacio que requiere, asegurarnos que sea nativa, su estado de vulnerabilidad, atractivos, etc|Enlaces a iNaturalist, Inbio, ACG; diámetro de raíces|
|Plántulas disponibles|Cuando germinan las semillas o pegan las estacas, esperamos a que la planta tenga cierta altura para ofrecerlas al proyecto, esperando ser recogidas y plantadas por voluntarios|Especie, cantidad|
|Semillas disponibles|Caminando por el bosque encontraremos semillas aptas para reproducir especies|Especie en iNaturalist, cantidad de semillas disponibles, fecha de recolección, Observación en iNaturalist del padre|
|Sitios para plantar|Caminando por la ciudad o usando Mapillary, buscamos jardines de ascera, espacios degradados, observamos y medimos el diámetro del espacio; para tener en cuenta el tamaño de árbol apto para plantar y conservar nuestra ciudad del efecto de las raices|Diámetro, link a mapillary|
|Cultivo|Cuando plantamos la especie es un gran logro, pero queremos celebrarlo con darle seguimiento a si murió por falta de agua o abuso humano, o si se convierte en algo majestuoso; así como calcular cuanto CO2 ha sido absorvido por los esfuersos del proyecto y sus voluntarios|Especie, historico de observacionesd deiNaturalist|

### Recomendaciones para Plantar

- Utilice un rótulo que cuente e invite a los vecinos del espacio plantado sobre su esfuerzo y el palito que viene. Use solo materiales degradables en cuestión de meses
- Una vez establecido el árbol, coloque una placa permanente para identificar la especie y ofrecer información sobre los beneficios y estado de conservación de la especie

También:

- En área de mucho tránsito, utilice estacas de madera y desechables, para brindarle soporte a la plántula mientras se desarolla. Use técnicas y materiales apropiados para amarrar, sin afectar al árbol maduro
- Para especies en peligro de extinsión se recomienda protección adicional con estructuras de madera o metal
