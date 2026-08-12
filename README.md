# Evaluación Sumativa Unidad IV

Repositorio correspondiente a la Evaluación Sumativa de la Unidad IV de la asignatura Ingeniería de Requisitos.

**Estudiante:** Díaz Pontón Steven Santiago  
**Carrera:** Ingeniería de Software  
**Universidad:** Universidad Técnica Estatal de Quevedo  

## Compilación reproducible

El documento principal de la evaluación está desarrollado en LaTeX.

### Archivo principal

```text
main.tex
```

### Estructura del repositorio

Para que la compilación se realice correctamente, se debe conservar la siguiente estructura:

```text
EVALUCION_UNIDAD_IV_DIAZ/
├── main.tex
├── EVALUACION_UNIDAD_IV_DIAZ.pdf
├── README.md
├── figuras/
│   ├── Figuras.md
│   ├── P1_diagrama_clases.jpeg
│   ├── P2_diagrama_actividades.png
│   └── P3_maquina_estados.png
├── evidencias/
│   ├── evidencias.md
│   ├── resumen_sga.png
│   └── revision_intento_sga.png
└── evidencias_manuscritas/
    ├── ev_m.md
    ├── P1_P2_REALIZADO_EN_CLASE.jpeg
    ├── P3_P4_REALIZADO_EN_CLASE.jpeg
    ├── P5_P6_REALIZADO_EN_CLASE.jpeg
    ├── P7_P8_REALIZADO_EN_CLASE.jpeg
    ├── P9_P10_REALIZADO_EN_CLASE.jpeg
    └── CONTINUACION_P10.jpeg
```

La carpeta `figuras/` contiene los diagramas UML utilizados en las actividades P1, P2 y P3. Esta carpeta es necesaria para la compilación del PDF.

La carpeta `evidencias/` contiene las capturas del resumen del cuestionario y de la revisión del intento realizado en el SGA. Esta carpeta también es necesaria para la compilación del PDF.

La carpeta `evidencias_manuscritas/` contiene las fotografías del desarrollo original realizado a mano durante la sesión en clase. Esta carpeta no interviene en la compilación del PDF y se conserva como respaldo del trabajo individual.

## Compilador

El documento debe compilarse utilizando:

```text
pdfLaTeX
```

## Comandos de compilación

Desde la raíz del repositorio, ejecutar:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

Ejecutar el mismo comando una segunda vez para asegurar la correcta resolución de los enlaces y las referencias internas:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

El archivo generado será:

```text
main.pdf
```

El PDF final versionado en el repositorio se encuentra con el nombre:

```text
EVALUACION_UNIDAD_IV_DIAZ.pdf
```

## Dependencias de LaTeX

El documento requiere los siguientes paquetes:

- `inputenc`
- `fontenc`
- `babel`
- `graphicx`
- `geometry`
- `array`
- `tabularx`
- `longtable`
- `float`
- `hyperref`

Se recomienda utilizar una distribución actualizada de LaTeX, como TeX Live.

## Soporte para el idioma español

El documento utiliza:

```latex
\usepackage[spanish]{babel}
```

Por esta razón, la máquina donde se realice la compilación debe tener instalado el soporte de idioma español para TeX Live.

En Ubuntu o Debian puede instalarse mediante:

```bash
sudo apt-get install texlive-lang-spanish
```

Si este paquete no está instalado, puede producirse el siguiente error:

```text
Package babel Error: Unknown option 'spanish'
```

El soporte para español ya está incluido en instalaciones completas de TeX Live, como `texlive-full`, y en Overleaf.

## Compilación en Overleaf

El documento también puede compilarse mediante Overleaf siguiendo estos pasos:

1. Descargar o clonar el repositorio completo.
2. Crear un nuevo proyecto en Overleaf.
3. Subir `main.tex`.
4. Subir las carpetas `figuras/` y `evidencias/` conservando sus nombres y estructura.
5. Establecer `main.tex` como documento principal.
6. Seleccionar `pdfLaTeX` como compilador.
7. Presionar la opción **Recompile**.

No se deben modificar los nombres ni las rutas de las imágenes.

La carpeta `evidencias_manuscritas/` puede conservarse como respaldo, pero no es necesaria para compilar el documento.

## Repositorio

```text
https://github.com/sdiazp3/EVALUCION_UNIDAD_IV_DIAZ.git
```
