Si se realiza la descarga del repositorio como .zip, los archivos dentro de la carpeta de External Libraries no se descargaran completa, debido a la configuración de git lts, se anexa una liga a drive en donde se puede encontrar la carpeta completa con todos los archivos, remplazar en la ubicación correcta.

https://drive.google.com/drive/folders/1Qpw_c-z50NlG6221SU-IFCxFxRJXP1LQ?usp=drive_link


https://drive.google.com/file/d/14APYc-izvPk7rnUJ3VNd3cjtCv1a9U6b/view?usp=drive_link

Ubicación donde se debe de remplazar la carpeta:
ExtraOrdinario/External Libraries


De igual forma si no se descargan todos los modelos se anexa la liga para poder descargar directamente la carpeta completa
https://drive.google.com/file/d/1MM-H1WGtk8vUuZrf5WIHrfhuBZF-019m/view?usp=drive_link

Ubicación donde se debe de remplazar la carpeta:
ExtraOrdinario/ExtraOrdinario/ModelsExtra



En caso de tener problemas con la configuración del proyecto, leer las siguiente sección:

Dentro de la configuración del proyecto en visual studio se debe de configurar los diccionarios que se utilizaran.





De tener algún error se debe de verificar la sección de C/C++ y en el apartado de Additional Include directories agregar los siguientes:



$(SolutionDir)External Libraries\\GLFW\\Include

$(SolutionDir)External Libraries\\GLEW\\Include

$(SolutionDir)External Libraries\\assimp\\Include

$(SolutionDir)External Libraries\\glm

$(SolutionDir)External Libraries\\SOIL2\\Include





De igual forma se debe de configurar la sección de Linker, en el apartado de Linker->General->AdditionalLibraryDirectories,  se debe de encontrar lo siguiente:



$(SolutionDir)External Libraries\\GLFW\\lib-vc2015

$(SolutionDir)External Libraries\\GLEW\\lib\\Release\\Win32

$(SolutionDir)External Libraries\\SOIL2\\lib

$(SolutionDir)External Libraries\\assimp\\lib



Y en la sección de Linker->Input->AdditionalDependencies,  se debe de encontrar lo siguiente:

glfw3.lib

opengl32.lib

glew32.lib

soil2-debug.lib

assimp-vc140-mt.lib



Es necesario configurar la plataforma de solución como x86.



cualquier duda o problema, comunicarse al correo joserapath@gmail.com





