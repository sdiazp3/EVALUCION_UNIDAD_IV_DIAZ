## Compilación reproducible

El documento principal de la evaluación está desarrollado en LaTeX.

### Archivo principal

```text
main.tex
```

### Estructura necesaria

Para que la compilación se realice correctamente, se debe conservar la siguiente estructura:

```text
EVALUCION_UNIDAD_IV_DIAZ/
├── main.tex
├── EVALUACION_UNIDAD_IV_DIAZ.pdf
├── README.md
├── figuras/
│   ├── P1_diagrama_clases.jpeg
│   ├── P2_diagrama_actividades.jpeg
│   └── P3_maquina_estados.png
└── evidencias/
    ├── resumen_sga.png
    └── revision_intento_sga.png
```

La carpeta `figuras/` es necesaria para la compilación, debido a que
`main.tex` utiliza las imágenes almacenadas en dicha ubicación.

La carpeta `evidencias/` contiene las capturas correspondientes al
desarrollo de la evaluación y no interviene en la compilación del PDF.

### Compilador

Utilizar:

```text
pdfLaTeX
```

### Comando de compilación

Desde la raíz del repositorio ejecutar:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

Ejecutar el comando una segunda vez para asegurar la correcta resolución
de referencias internas:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

El archivo generado será:

```text
main.pdf
```

Para la entrega final, el documento compilado se encuentra versionado en
el repositorio con el nombre:

```text
EVALUACION_UNIDAD_IV_DIAZ.pdf
```

### Dependencias LaTeX

El documento requiere los siguientes paquetes:

- inputenc
- fontenc
- babel
- graphicx
- geometry
- array
- tabularx
- longtable
- float
- hyperref

Se recomienda una distribución LaTeX actualizada, como TeX Live.

### Compilación en Overleaf

También puede reproducirse mediante Overleaf:

1. Importar o subir el contenido completo del repositorio.
2. Mantener `main.tex` y la carpeta `figuras/` en sus ubicaciones originales.
3. Establecer `main.tex` como documento principal.
4. Seleccionar `pdfLaTeX` como compilador.
5. Recompilar el proyecto.

No es necesario modificar las rutas de las imágenes.
