# Plantilla y Paquete LaTeX - IESIBAI (No Oficial)

<div align="center">

# 📦 `iesibai-template.sty`
**Plantilla Institucional y Paquete de Estilo LaTeX para IESIBAI** /  
**Identidad Visual y Formato Académico Estandarizado**

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/thebiotechscientist/iesibai-latex-template)
[![LaTeX](https://img.shields.io/badge/LaTeX-XeLaTeX%20%7C%20LuaLaTeX-4A154B?logo=latex&logoColor=white)](https://www.tug.org/xetex/)
[![CTAN](https://img.shields.io/badge/CTAN-iesibai--template-green.svg)](https://ctan.org/pkg/iesibai)
[![License](https://img.shields.io/badge/License-LPPL%20v1.3c-teal.svg)](https://www.latex-project.org/lppl.txt)
[![Author](https://img.shields.io/badge/author-TheBiotechScientist-181717?logo=github&logoColor=white)](https://github.com/thebiotechscientist)

*Macros, estilos tipográficos, configuración de portadas automatizadas y paletas cromáticas institucionales para el Instituto de Estudios Superiores de la Red Iberoamericana de Academias de Investigación (IESIBAI).*

</div>

---

## Descripción
Paquete no oficial de estilo en LaTeX para la redacción de documentos académicos del IES IBAI, configurado con soporte para **XeLaTeX** e identidades visuales institucionales. El paquete `iesibai-template` proporciona macros, configuración de formato y elementos de portada para la generación de documentos académicos e institucionales ajustados a los requisitos del IESIBAI.

## Contenido del paquete
- `iesibai-template.sty`: Archivo de estilo principal.
- `iesibai-doc.pdf`: Documentación oficial compilada.
- `iesibai-doc.tex`: Código fuente de la documentación.
- `ejemplo.tex`: Documento de ejemplo mínimo.
- `ejemplo.pdf`: Documento de ejemplo mínimo compilado.
- `README.md`: Readme con esta información.
- `LICENSE`: Licencia del paquete.
- `assets/`: Recursos gráficos predeterminados (logos y fondos).

## Requisitos previos
- Distribución TeX (TeX Live, MiKTeX o MacTeX).
- Compilador **XeLaTeX**.
- Procesador de bibliografía **Biber**.
- Opcional *Zotero* para la gestión de referencias.
- Tener isntalado en el sistema las fuentes Arial, Helvetica y Noto Sans

## Uso rápido
1. Clona este repositorio o descarga el archivo `iesibai-template.sty`.
2. Coloca `iesibai-template.sty` en la misma carpeta que tu archivo principal (trabajo, tesis, etc) `.tex`.
3. En el preámbulo de tu documento, incluye:
   ```latex
   \documentclass[12pt, letterpaper]{article}
   \usepackage{iesibai-template}
   % ...
   % demás código de paquetes y preámbulo
   % ...
   ```
## Instalación desde CTAN
- Desde el instalador/gestor de paquetes de su distribución instalada (MikTeX, TeXLive, MacTeX, etc.)
- Desde el repositorio de *CTAN*, buscar el paquete `iesibai-template.sty` y descargar.
- Seguir las instruciones para descarga y correcta isntalación de un paquete desde CTAN.

## Características
1. Incluye un fondo de portada predefinido.
2. Campos de datos opcionales para la portada.
3. Formato predefinido de portada, tabla de contenidos, capítulos y secciones acorde a los colores del instituto IESIBAI
4. Incluye logos de la institución en formatos `.jpeg`, `.png` y `.svg`.

## Ejemplo

```latex
\documentclass[12pt,letterpaper]{report}
\usepackage{iesibai-template}

% --- EJEMPLOS DE USO OPCIONALES ---
% 1. Para cambiar solo algunos valores de la portada, descomenta esto:
\iesibaisetup{
    logo={assets/logo_iesibai.png},
    fondo={assets/fondo_portada_redes_2.jpeg},
    institucion={Instituto de Estudios\\ Superiores de la\\ Red Iberoamericana de\\ Academias de Investigación},
    campus={Campus Virtual Hidalgo},
    programa={Maestría en Educación},
    materia={Tecnología e Innovación I},
    subtitulo={Un subtítulo interesante},
    trabajo={Nombre del Producto de Investigación},
    alumno={Nombre del Alumno},
    profesor={Dr. TheBiotechScientist},
    ubicacion={San Luis Potosí, México},
    fecha={Septiembre, 2026}
}

% Para los enlaces de la tabla de contenidos, figuras, tablas, links
\usepackage{csquotes}
\usepackage{hyperref}
\hypersetup{
%   plainpages=false,
%   pdfpagelabels=true,
  colorlinks=true,
  linkcolor=iesblueprimary,
  urlcolor=iesaccent,
  citecolor=iesblueprimary,
  pdftitle={Proyecto de Investigación},
  pdfauthor={Autor del PDF generedo},
  pdfsubject={Nombre de la nateria},
  pdfkeywords={Educación, Metodología, IESIBAI}
}

% 2. Si para algún trabajo no deseas que se genere la portada, descomenta esto:
% \sinportadaiesibai

\begin{document}

\tableofcontents

\chapter{Título del Primer capítulo}

\section{Primera sección del capítulo 1}
Texto de la primera sección

\subsection{Sub-sección de la sección 1}
Texto de la primera sub-sección



\chapter{Título del Segundo capítulo}

\section{Primera sección del capitulo 2}
Texto de la sección 1

\subsection{Una sub-sección}
Texto de la sub-sección 1 

\chapter{Tercer capítulo}
Y seguimos con un nuevo capítulo y secciones.

\end{document}
```