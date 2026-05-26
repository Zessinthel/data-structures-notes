# Estructuras de Datos — Notas de Curso

**Autor:** Jesús Antonio Chala Casanova  
**Programa:** Computer and Information Science Engineering (CISE), Ph.D.  
**Estado:** En desarrollo activo — documentación parcial

---

## Descripción

Compendio de notas de estudio del curso de *Data Structures*, redactado con énfasis en
la lógica estructural y el análisis de complejidad que subyace a cada estructura. El
objetivo no es replicar la documentación oficial de Java, sino articular *por qué* cada
estructura existe, *cuándo* elegirla y *a qué costo* algorítmico.

Las notas están escritas en español con anglicismos técnicos donde el término en inglés
es el estándar en la literatura (*hashing*, *BST*, *heap*, *in-order*, etc.). El nivel
de formalidad es alto: se incluyen definiciones recursivas, notación de conjuntos y
argumentos de complejidad asintótica.

---

## Temario completo del curso

| #  | Tema                                      | Estado         |
|----|-------------------------------------------|----------------|
| 1  | Fundamentos de Java (POO, clases, interfaces) | Pendiente  |
| 2  | Big-O Analysis                            | Pendiente      |
| 3  | ArrayLists                                | Pendiente      |
| 4  | Linked Lists                              | Pendiente      |
| 5  | Queues                                    | Pendiente      |
| 6  | Deques                                    | Pendiente      |
| 7  | Stacks                                    | Pendiente      |
| 8  | Sets                                      | Pendiente      |
| 9  | Hashing                                   | ✅ Documentado |
| 10 | Hash Tables                               | ✅ Documentado |
| 11 | Hash Maps                                 | ✅ Documentado |
| 12 | Trees                                     | ✅ Documentado |
| 13 | Binary Search Trees (BST)                 | ✅ Documentado |
| 14 | Heaps                                     | Pendiente      |
| 15 | Priority Queues                           | Pendiente      |
| 16 | Grafos                                    | Pendiente      |
| 17 | Sorting                                   | Pendiente      |

Los capítulos documentados corresponden a los temas 9–13. Los anteriores y posteriores
se irán incorporando a medida que avance el curso.

---

## Estructura del repositorio

```
.
├── main.tex                    # Documento principal
├── metadata.tex                # Título, autor, keywords, bibliografía
├── config/                     # Paquetes, márgenes, macros, estilos
├── environments/               # Entornos tcolorbox (definicion, teorema, ejemplo, etc.)
├── themes/                     # Paleta Catppuccin (claro/oscuro)
├── frontmatter/
│   ├── titlepage.tex
│   ├── preliminary.tex
│   └── preface.tex
├── chapters/
│   ├── chapter1.tex            # Hashing
│   ├── chapter2.tex            # Hash Tables y Hash Maps
│   ├── chapter3.tex            # Trees
│   └── chapter4.tex            # Binary Search Trees (BST)
├── references/
│   └── references.bib
└── figs/                       # Imágenes y figuras externas
```

---

## Compilación

El documento usa **pdflatex** con `biber` para la bibliografía.

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Si usas **latexmk**:

```bash
latexmk -pdf main.tex
```

### Dependencias principales

- `tcolorbox` (con librerías `theorems`, `breakable`, `skins`)
- `forest` — diagramas de árboles
- `algorithm2e` — pseudocódigo
- `tikz` — figuras y diagramas
- `tabularx`, `booktabs`, `colortbl` — tablas
- `catppuccinpalette` — paleta de colores
- `biblatex` + `biber` — bibliografía

> Para limpiar archivos auxiliares entre compilaciones:
> ```bash
> latexmk -c
> ```

---

## Template

Este documento usa el template `latex-catppuccin-academic` (v0.2), desarrollado por el
mismo autor. El template provee entornos semánticos (`definicion`, `teorema`, `ejemplo`,
`ejercicio`, `observacion`), un sistema de coloreado de ecuaciones, soporte para
*listings* en múltiples lenguajes y la paleta completa de Catppuccin en modo claro y oscuro.

Repositorio del template: [github.com/Zessinthel](https://github.com/Zessinthel/)

---

## Licencia

MIT — ver archivo [`LICENSE`](LICENSE)
