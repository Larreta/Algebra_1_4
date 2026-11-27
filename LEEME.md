# Álgebra 1.4 · Aula de matrices

Proyecto independiente: 25 prácticos, 40 teóricos y 11 ejercicios MATLAB de las imágenes de la sección 1.4 de Kolman y Hill. No contiene las secciones 1.1, 1.2 ni 1.3 y no modifica sus repositorios.

## EMPIEZA AQUÍ

1. Extrae **Algebra_1_4_GitHub.zip** con «Extraer todo» de Windows. No abras los archivos dentro del ZIP.
2. Abre **index.html** con Chrome o Edge. La página, las fórmulas y los laboratorios funcionan sin conexión.
3. Elige un ejercicio en la barra izquierda. Puedes buscar `20`, `T.28`, `ML.6` o una palabra del tema.
4. Lee la explicación completa o cambia a **Estudiar un paso por vez**. Los dos modos contienen la misma solución.
5. En computadora, el laboratorio está a la derecha. En una pantalla estrecha se coloca debajo para conservar el tamaño de lectura.

## Cómo funciona el laboratorio

- **Siguiente** realiza una acción: elegir una casilla, multiplicar una pareja, añadir el producto a la suma o guardar el resultado. No salta directamente a una respuesta dibujada.
- La suma comienza en cero en cada casilla. Los signos y los valores de origen permanecen visibles.
- Las casillas pendientes muestran `?`. Puedes pulsar una casilla para practicarla; consultar una cuenta no completa las otras.
- **Anterior** retrocede y retira lo guardado en ese avance. **Reiniciar** borra el recorrido del caso actual. Cada caso conserva su progreso mientras permanezcas en la página.
- Al terminar un caso, **Siguiente caso** continúa al próximo inciso. También puedes elegirlo directamente en **Inciso o caso**.
- **Operación** permite practicar una operación intermedia. Si saltas a ella, sus operandos se muestran completos para que puedas trabajar; eso no marca como calculadas las casillas de las operaciones que omitiste.
- **Reproducir** avanza automáticamente; vuelve a pulsar para pausar. Cambiar de ejercicio o caso detiene la reproducción.
- Las ayudas **Completar esta casilla/operación** actúan solo cuando las solicitas. El recorrido normal muestra todas las cuentas.
- Los teóricos se abren en **Recorrer el argumento**. Cada avance explica una parte de la demostración. Cambia a **Hacer las operaciones** para sus ilustraciones, que no sustituyen la prueba formal.
- En F₂, primero se ve la cuenta usual y después su reducción módulo 2.

## Gráficos

Los gráficos corresponden al problema: vectores, giros, recta de soluciones, evolución del mercado y entradas de potencias. Las operaciones puramente matriciales se muestran en matrices numeradas, sin un plano cartesiano artificial.

Un punto nuevo aparece cuando guardas todas las coordenadas de ese resultado. Arrastra para desplazar o girar, usa la rueda para acercar y haz doble clic para restablecer la vista. La barra del gráfico permite guardar una imagen. En las potencias puedes activar el límite como referencia, después de leer su justificación.

La comparación de una distribución con su equilibrio no representa el equilibrio como si se alcanzara en un año: su eje indica expresamente que es una verificación. Los PDF muestran figuras finales de referencia; la construcción progresiva está en la web.

## PDF, MATLAB y LaTeX

- **PDF completo 1.4**: colección con índice y marcadores.
- **PDF del ejercicio**: documento independiente del ejercicio seleccionado, incluidos todos sus incisos y ejemplos explicados.
- **Códigos MATLAB**: once archivos `.m` y auxiliares `binrand`, `binadd`, `binprod`. Extrae el paquete y selecciona esa carpeta como carpeta actual en MATLAB.
- **Fuente LaTeX**: colección editable. Para compilar, usa LuaLaTeX con las fuentes DejaVu y Latin Modern, o adapta las fuentes a tu instalación. El PDF ya viene preparado.
- **Fuentes para VS Code**: código, motor matemático, pruebas y recursos locales. No necesitas instalar Python, Node ni MATLAB para consultar la web.

La parte web de MATLAB reproduce las operaciones; no ejecuta MATLAB dentro del navegador. Los resultados se contrastaron con aritmética exacta de Python. Los `.m` se suministran para ejecutarlos en MATLAB.

## Publicar en GitHub Pages, separado del proyecto anterior

**Crea un repositorio nuevo**, por ejemplo `Algebra_1_4`. Conserva el nombre y contenido de tu repositorio anterior.

1. En GitHub, crea un repositorio público llamado `Algebra_1_4`. Puedes incluir un README inicial para crear la rama `main`.
2. Entra al repositorio nuevo. Pulsa **Add file → Upload files → choose your files**.
3. Sube **index.html** desde la carpeta extraída. En el primer cuadro de «Commit changes» escribe `Agregar sección 1.4` y pulsa el botón verde **Commit changes**. Deja seleccionada la rama `main`.
4. Repite **Add file → Upload files** para los demás archivos de la carpeta extraída, **uno por subida y por commit**. Así evitas repetir el fallo que ocurrió con la carga conjunta. Conserva todos los nombres, incluido `.nojekyll`.
5. Deben quedar juntos, en la raíz del repositorio: `index.html`, `Coleccion_1_4.pdf`, los archivos `pdfs_1_4_*.js`, `recursos_1_4.js`, `Fuentes_VSCode.zip`, `LEEME.md`, `REVISION.md`, `Guia_1_4.pdf`, `ARCHIVOS_GITHUB.txt` y `.nojekyll`. La lista exacta de esta entrega está en **ARCHIVOS_GITHUB.txt**.
6. Ve a **Settings → Pages**. En Source elige **Deploy from a branch**. En Branch selecciona **main**, carpeta **/(root)**, y pulsa **Save**.
7. Cuando GitHub termine la publicación, abre el enlace que aparezca en Pages. Si tu usuario es `Larreta` y eliges ese nombre, será `https://larreta.github.io/Algebra_1_4/`.
8. Comprueba la página y una descarga individual. Si falta una descarga, revisa que el archivo `.js` correspondiente esté en la raíz y conserve su nombre.

No subas el ZIP exterior como sustituto de la página: GitHub Pages necesita `index.html` extraído. **Fuentes_VSCode.zip sí permanece como ZIP**, porque es la descarga del código editable. No hace falta extraerlo para publicar. Esta entrega usa archivos planos; no tendrás que crear manualmente una carpeta de MATLAB en GitHub.

Todos los archivos destinados a GitHub tienen menos de 25 MiB. No se requiere Git LFS, un servidor Python ni un servicio externo para los PDF.

## Editar en VS Code

1. Extrae `Fuentes_VSCode.zip` en otra carpeta y ábrela con **Archivo → Abrir carpeta**.
2. Puedes abrir `index.html` directamente, o servirla con Live Server.
3. El contenido se genera desde `motor/practicos.py`, `motor/teoricos.py`, `motor/matlab_lecciones.py` y `motor/modelo.py`; el diseño está en `motor/diseno.css` y los controles en `motor/app.js`.
4. Para regenerar: `python -m pip install -r requirements.txt`, `npm install`, `npx playwright install chromium`, `python build.py`. Para generar todos los documentos y el paquete sigue `DESARROLLO.md`.

## Precisiones editoriales

- Las referencias a los teoremas 1.1–1.4 se contrastaron con la edición de Kolman y Hill correspondiente a los enunciados. Los datos de las imágenes que enviaste gobiernan estos ejercicios.
- T.19 conserva el enunciado impreso y explica la corrección necesaria: para A de n×m, el vector debe tener m entradas.
- ML.1(b): el menor positivo literal es 1; el primer retorno con k>1 es 5.
- ML.2(b): el índice depende de los números aleatorios; siempre es ≤4. La muestra de la web es fija y se identifica como tal.
- ML.6 usa exactamente −1/5 en la diagonal. ML.8(b) suma dos y tres copias.
- Los ejercicios 18–21 usan distribuciones columna. ML.4 usa distribuciones fila. Las dos convenciones se explican por separado.
- Las pruebas reales que dividen entre 2 o usan cuadrados no negativos no se trasladan automáticamente a F₂.
