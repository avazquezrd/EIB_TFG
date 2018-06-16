# Plantilla para la memoria de un TFG
Plantilla para la creación del Trabajo de Fin de Grado siguiendo la normativa de la Escuela de Ingeniería de Bilbao (UPV/EHU) y la [guía de expresión de marca de la UPV/EHU](https://www.ehu.eus/documents/10136/3950780/GUIA_EXPRESION_UPV_es.pdf/4d538337-2577-4260-ae02-d0fed29a26b5).

> **Nota:** Se recomienda usar `XeLaTex` como compilador.

## Personalización de la portada

En el archivo `main.tex` se deben introducir los datos de la portada del TFG:
```
% ------------------------------------------------------------ %
% DATOS DEL DOCUMENTO                                          %
% ------------------------------------------------------------ %

% Título:
\newcommand{\titulo}{<Título del trabajo>}
% Curso académico:
\newcommand{\curso}{<XXXX-XXXX>}
% Carrera:
\newcommand{\carrera}{Grado en XXXXXXXX}
% Alumno/Alumna:
\newcommand{\alumno}{<apellido 1, apellido 2, nombre>}
% Dirección 1 del TFG:
\newcommand{\direccionA}{<apellido 1, apellido 2, nombre>}
% Dirección 2 del TFG (si no la hay, comentar la línea aquí y también en preamble.tex):
\newcommand{\direccionB}{<apellido 1, apellido 2, nombre>}
% Fecha:
\newcommand{\fecha}{<XXXX, día, mes, año>}
% ------------------------------------------------------------ %
```
Para modificar detalles como `Alumno/Alumna` o eliminar una de las líneas de la dirección del TFG, se debe ir a la parte inferior del archivo `preamble.tex`:
```
	\begin{tikzpicture}[remember picture, overlay]
		\node (C) at ([yshift=-6.95cm, xshift=9.7cm]current page.west) [inner sep=10pt, draw, thick, minimum width=13.34cm, minimum height=64pt, align=left, fill=white]{};
		\node (D) [right=0.2cm of C.west, anchor=west, align=left]
		{\small{\textbf{Alumno/Alumna: }\alumno}\\
			\small{\textbf{Director/Directora (1): }\direccionA}
			% Comentar la siguiente línea si sólo hay una direcicón del TFG. Eliminar también de la anterior el (1).
			\\\small{\textbf{Director/Directora (2): }\direccionB}
			};
	\end{tikzpicture}
}
```
