# Revisión de la sección 1.4

Cobertura: 25 prácticos, 40 teóricos y 11 MATLAB; 76 documentos individuales y una colección general. Enunciados transcritos de las imágenes proporcionadas. Las aclaraciones editoriales están dentro de sus ejercicios.

La revisión matemática contrasta cada entrada, cada producto parcial y cada acumulación mediante aritmética simbólica exacta. Incluye las distribuciones estacionarias, las dos raíces de normalización, las fórmulas de potencias y la clasificación de los 16 candidatos binarios. Los ejemplos se identifican como ejemplos; las pruebas formales explican las hipótesis, los pasos y la conclusión general.

Las pruebas de interfaz recorren todos los ejercicios, casos y operaciones. Además comprueban el avance por acciones, el guardado y deshecho de casillas, la transición entre casos, las ayudas explícitas, la reproducción y pausa, los temas azul/verde y el ancho móvil de 390 px. Se revisan los datos de las gráficas para que correspondan a los cálculos y no anticipen resultados.

La exportación comprueba la composición de las fórmulas de todos los documentos. Se inspeccionaron páginas de prácticos, pruebas formales, Markov y MATLAB y se comprueban límites de página y páginas vacías. El PDF general se arma a partir de los mismos PDF individuales. Los archivos de descarga empaquetados conservan exactamente sus bytes originales y se contrastan por SHA-256.

Los informes reproducibles están en la carpeta `tests` de Fuentes_VSCode.zip. Los scripts MATLAB no se ejecutaron en MATLAB durante esta revisión: su aritmética esperada se contrastó independientemente, y se entregan para ejecución en ese programa. La publicación en tu cuenta GitHub se realiza siguiendo LEEME.md; no se ha publicado automáticamente.

## Corrección de presentación LaTeX · versión 1.4.2

La integración de fuentes de la primera entrega dañaba los límites de las reglas CSS de KaTeX. Las matrices tenían sintaxis LaTeX correcta, pero las fuentes de los delimitadores no se cargaban y los corchetes quedaban pequeños. La corrección conserva las veinte reglas originales de fuentes e incluye sus archivos WOFF2 dentro de la página y de los documentos para impresión.

La nueva prueba `tests/latex_visual.cjs` carga expresamente las veinte fuentes sin conexión, comprueba las 410 matrices distintas del proyecto y mide ambos corchetes frente a la altura de sus filas: 820 delimitadores. Incluye matrices rectangulares, vectores, fracciones, radicales, expresiones simbólicas y matrices de orden 7. Esta comprobación es adicional a la validación de sintaxis de las fórmulas. Las matrices del enunciado y de las explicaciones se muestran con un tamaño mayor; se evitan las frases duplicadas dentro de un mismo paso de cálculo.

Los PDF individuales y la colección general se regeneraron después de la corrección. La revisión de documentos comprueba que las fuentes KaTeX estén efectivamente incrustadas, además de los límites de página y las páginas vacías. Se vuelven a ejecutar las pruebas de controles y descargas sobre los archivos finales de publicación.
