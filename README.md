# Hackathon RIIAA 2021 "JusticIA para los desaparecidos"
# Modelo de reconocimiento de objetos en documentos con Azure Custom Vision

**Nombre del equipo**  
Los Sneiks

**Integrantes**
* César Balderrama
* Elaine Díaz
* Jessica Jiménez
* Jorge García
* Luis López de Rivera

## Descripión
Este repositorio demuestra un pipeline para resolver el reto #1 del Hackathon RIIAA 2021 "JusticIA para los desaparecidos".

## Pipeline
1. Obtener cada archivo
2. Remover la metadata EXIF de todas las imágenes
3. Para cada imagen
    - Si el archivo es un .pdf convertirlo a .jpg
    - Llamar al modelo de orientación de objetos de Azure Custom Vision
    - Rotar el .jpg para que esté en 0 grados (recto)
    - Obtener el ancho y largo de la imagen
    - Llamar al modelo de reconocimiento de objetos de Azure Custom Vision
        - Recibir los resultados en json
        - Ignorar los resultados con probabilidad < 0.5
        - Convertir los resultados de Bounding Box a xmin, ymin, xmax, ymax
        - Regresar el resultado con el formato necesario para guardarse en csv
    - Adjuntar cada resultado a un archivo .csv
4. Guardar el archivo .csv con todos los resultados

## Cómo correr el código
Ejecutar el ipynb en Google Colab
Instalar todas las dependencias de la primera celda, y esperar a que el kernel se reinicie para continuar.

## Notas
En el .ipynb se encuentra una descripción más a fondo de cada método y cómo funciona