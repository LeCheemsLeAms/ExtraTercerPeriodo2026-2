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





