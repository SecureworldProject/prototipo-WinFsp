# prototipo-WinFsp

El archivo pasthrough.c contiene el código de la aplicación del prototipo que corre sobre la tecnología de WinFsp.

Para realizar pruebas con este prototipo se deben seguir las siguientes indicaciones:

1. Descargar WinFsp desde http://www.secfs.net/winfsp/rel/. Se debe instalar WinFsp en la ubicación predeterminada (en "Archivos de programa").
2. Descargar e instalar Microsoft Visual Studio Community 2019, se puede descargar de forma gratuita desde el sitio web de Microsoft. 

3. Instalar WinFsp, marcando la opción "Desarrollador" para asegurarse de que todos los archivos de cabecera y biblioteca necesarios se incluyan en la instalación.

4. Reemplaza el fichero WinFsp\samples\passthrough\passthrough.c con este fichero.

5. Se carga el proyecto passthrough.vcxproj en Visual Studio.  Que se puede encontrar en el directorio samples\passthrough del directorio que agrega el instalador de winsp en "Archivos de programa (x86)". 

6. Una vez cargado el proyecto se compila.

7. Luego mediante línea de comandos navegamos hacia la ubicación de passthrough-x64.exe y se ejecuta la siguiente línea de comandos:  passthrough-x64 -p C:\user -m M:

De esta forma se inicia el servicio y se mapea la unidad C:\users desde la unidad M: cuyo sistema de archivos es "pasthrough".


