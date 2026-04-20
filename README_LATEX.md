# Plantilla LaTeX para Informe de Ingeniería de Software

## Archivos incluidos

- `informe_template.tex` - Plantilla principal del documento
- `referencias.bib` - Archivo de bibliografía con ejemplos

## Cómo usar esta plantilla

### 1. Personalizar el documento

Edita `informe_template.tex` y modifica:

- **Título**: Línea 31 - Cambia el título del informe
- **Autores**: Líneas 33-36 - Agrega los nombres completos y el grupo
- **Resumen**: Líneas 48-49 - Escribe tu resumen (máx. 250 palabras)
- **Palabras clave**: Línea 53 - Lista tus palabras clave separadas por comas

### 2. Agregar contenido

- Modifica las secciones existentes según tu tema
- Agrega nuevas secciones usando `\section{Nombre de la Sección}`
- Agrega subsecciones usando `\subsection{Nombre de la Subsección}`

### 3. Agregar referencias bibliográficas

#### Editar el archivo referencias.bib

Agrega tus propias entradas bibliográficas siguiendo los ejemplos proporcionados:

```bibtex
@book{clave_unica,
    author    = {Nombre del Autor},
    title     = {Título del Libro},
    publisher = {Editorial},
    year      = {2024}
}
```

Tipos de entradas disponibles:
- `@book` - Libros
- `@article` - Artículos de revista
- `@inproceedings` - Artículos de conferencia
- `@phdthesis` - Tesis doctoral
- `@misc` - Recursos diversos
- `@online` - Recursos en línea
- `@techreport` - Reportes técnicos

#### Citar en el documento

Usa `\cite{clave_unica}` para citar una referencia:

```latex
Según Sommerville \cite{ejemplo1}, la ingeniería de software...
```

Para múltiples citas:

```latex
Diversos autores \cite{ejemplo1, ejemplo2, ejemplo3} han demostrado...
```

### 4. Agregar figuras

```latex
\begin{figure}[H]
    \centering
    \includegraphics[width=0.7\textwidth]{ruta/a/tu/imagen.png}
    \caption{Descripción de la figura}
    \label{fig:mi_figura}
\end{figure}
```

Para referenciar: `Como se observa en la Figura \ref{fig:mi_figura}...`

### 5. Agregar tablas

```latex
\begin{table}[H]
    \centering
    \caption{Descripción de la tabla}
    \label{tab:mi_tabla}
    \begin{tabular}{|l|c|r|}
        \hline
        \textbf{Columna 1} & \textbf{Columna 2} & \textbf{Columna 3} \\
        \hline
        Dato 1 & Dato 2 & Dato 3 \\
        Dato 4 & Dato 5 & Dato 6 \\
        \hline
    \end{tabular}
\end{table}
```

### 6. Compilar el documento

Debes compilar en el siguiente orden:

```bash
pdflatex informe_template.tex
bibtex informe_template
pdflatex informe_template.tex
pdflatex informe_template.tex
```

O si usas un editor LaTeX (TeXstudio, Overleaf, etc.), simplemente usa la opción de compilación con bibliografía.

## Estructura del documento

1. **Portada** - Título, autores y grupo
2. **Resumen y palabras clave**
3. **Tabla de contenidos** (opcional)
4. **Introducción** - Contexto y relevancia
5. **Contexto Histórico** - Desarrollo histórico del tema
6. **Desarrollo Técnico** - Aspectos técnicos, fórmulas, algoritmos
7. **Impacto en la CC** - Contribuciones y relevancia
8. **Conclusiones** - Síntesis y lecciones
9. **Referencias bibliográficas** - Generadas automáticamente

## Paquetes incluidos

- `babel` - Soporte para español
- `graphicx` - Inclusión de imágenes
- `amsmath` - Fórmulas matemáticas
- `cite` - Manejo de citas
- `hyperref` - Enlaces e hipervínculos
- `float` - Control de posición de figuras/tablas
- Y más...

## Consejos

- Guarda las imágenes en una carpeta separada (ej: `imagenes/`)
- Usa nombres descriptivos para las claves de las referencias
- Mantén el archivo .bib organizado por tipo de publicación
- Compila frecuentemente para detectar errores temprano
- Usa `\label` y `\ref` para referencias cruzadas automáticas

## Ejemplo de cita

En el documento:
```latex
La ingeniería de software \cite{ejemplo1} es fundamental...
```

En referencias.bib:
```bibtex
@book{ejemplo1,
    author    = {Ian Sommerville},
    title     = {Ingeniería de Software},
    publisher = {Pearson},
    year      = {2011}
}
```

Resultado: "La ingeniería de software [1] es fundamental..."
