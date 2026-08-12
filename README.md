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
│   ├── P2_diagrama_actividades.png
│   └── P3_maquina_estados.png
├── evidencias/
│   ├── resumen_sga.png
│   └── revision_intento_sga.png
└── evidencias_manuscritas/
    └── (fotos del desarrollo manuscrito realizado en clase)
```

La carpeta `figuras/` es necesaria para la compilación, debido a que `main.tex` utiliza las imágenes almacenadas en dicha ubicación.

La carpeta `evidencias/` contiene las capturas correspondientes al cuestionario del SGA y no interviene en la compilación del PDF práctico.

La carpeta `evidencias_manuscritas/` contiene las fotografías del desarrollo original hecho a mano durante la sesión en clase. Tampoco interviene en la compilación del PDF; se conserva como respaldo del trabajo individual realizado en el aula.

### Compilador

Utilizar:

```text
pdfLaTeX
```

### Comandos de compilación

Desde la raíz del repositorio, ejecutar:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

Ejecutar el comando una segunda vez para asegurar la correcta resolución de las referencias internas:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

El archivo generado será:

```text
main.pdf
```

Para la entrega final, el documento compilado se encuentra versionado en el repositorio con el nombre:

```text
EVALUACION_UNIDAD_IV_DIAZ.pdf
```

### Dependencias de LaTeX

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

Se recomienda utilizar una distribución actualizada de LaTeX, como TeX Live.

### Requisito adicional del sistema

El documento usa `\usepackage[spanish]{babel}`, por lo que además de los paquetes
LaTeX listados arriba, la máquina donde se compile debe tener instalado el
soporte de idioma español para TeX Live:

```bash
sudo apt-get install texlive-lang-spanish
```

Sin este paquete, la compilación falla con el error `Package babel Error:
Unknown option 'spanish'` y no se genera el PDF. Este paquete ya viene incluido
en instalaciones completas de TeX Live (`texlive-full`) y en Overleaf, por lo
que en esos entornos no se requiere ninguna acción adicional.

### Compilación en Overleaf

El documento también puede compilarse mediante Overleaf siguiendo estos pasos
(Overleaf ya incluye el soporte de idioma español, no requiere instalación
adicional):

1. Importar o subir el contenido completo del repositorio.
2. Mantener `main.tex` y la carpeta `figuras/` en sus ubicaciones originales.
3. Establecer `main.tex` como documento principal.
4. Seleccionar `pdfLaTeX` como compilador.
5. Recompilar el proyecto.

No es necesario modificar las rutas de las imágenes.
