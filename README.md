# Hackathon RIIAA 2021 "JusticIA para los desaparecidos"
# Modelo de reconocimiento de objetos en documentos con Azure

**Nombre del equipo**  
Los Sneiks

**Integrantes**
* César Balderrama
* Elaine Díaz
* Jessica Jiménez
* Jorge García
* Luis López

## Descripión
Este repositorio demuestra un pipeline para resolver el reto #1 del Hackathon RIIAA 2021 "JusticIA para los desaparecidos.

## Pipeline
1. Obtener cada archivo
2. Limpiar todas las imágenes, removiendo la metadata Exif
3. Para cada archivo
    - Si el archivo es un .pdf convertirlo a .jpg
    - Rotar el .jpg para que esté en 0 grados
    - Llamar al modelo de reconocimiento de objetos de Azure Custom Vision
    - Recibir los resultados en json
    - Adjuntar cada resultado a un archivo .csv
4. Guardar el archivo .csv con todos los resultados

## Cómo correr el código
Ejecutar el ipynb
Librerías:
Pillow
pdf2image
poppler, instalar en ambiente según instrucciones en https://pypi.org/project/pdf2image/

https://inside-machinelearning.com/en/how-to-install-use-conda-on-google-colab/

## Notas
Acerca de los [README](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/about-readmes)

