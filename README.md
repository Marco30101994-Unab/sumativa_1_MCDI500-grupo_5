# Factores asociados a la duración de los permisos de uso de vía pública en San Francisco

Proyecto desarrollado por el **Grupo 5** para la asignatura **MCDI500 – Programación para la Ciencia de Datos**, del Magíster en Ciencia de Datos e Inteligencia Artificial de la Universidad Andrés Bello.

## Integrantes

- Marco Álvarez Araya ([@Marco30101994-Unab](https://github.com/Marco30101994-Unab))
- María Fassler Neumann ([@belenfassler](https://github.com/belenfassler))
- Ricardo Jaramillo Pulgar ([@RJaramilloP](https://github.com/RJaramilloP))

## Pregunta de investigación

¿Qué factores administrativos, territoriales y temporales se asocian con la duración autorizada de los permisos activos de uso de vía pública en San Francisco, considerando especialmente el tipo de permiso?

El proyecto tiene un alcance descriptivo y asociativo. Por lo tanto, sus resultados no deben interpretarse como relaciones causales.

## Datos utilizados

Los datos provienen del conjunto [Active Street-Use Permits](https://data.sf.gov/City-Infrastructure/Active-Street-Use-Permits/x8nh-xzn6/about_data), publicado por San Francisco Public Works en DataSF.

- Fecha de corte: 9 de septiembre de 2026.
- Licencia: PDDL 1.0.
- Archivo original: `data/raw/Active_Street-Use_Permits_20260909.csv`.
- Conjunto de trabajo: 6.010 registros correspondientes a 2.139 permisos.
- Unidad de observación: segmento de calle.
- Unidad de análisis definida en la Fase 3: permiso.

El archivo original se conserva sin modificaciones. Debido a que la fuente se actualiza diariamente, volver a descargarla podría producir resultados diferentes.

### Limitación

La fuente contiene solamente permisos vigentes en la fecha de corte, por lo que los permisos de mayor duración pueden quedar sobrerrepresentados. En consecuencia, los resultados describen los permisos activos al 9 de septiembre de 2026 y no la totalidad histórica de permisos otorgados.

## Desarrollo del proyecto

- **Fase 1:** definición del problema, entorno reproducible y documentación de los datos.
- **Fase 2:** limpieza, transformación, imputación, codificación y escalamiento.
- **Fase 3:** núcleo algorítmico, programación orientada a objetos, eficiencia y validación.
- **Fase 4:** análisis final, interpretación y comunicación de resultados.

## Estructura del repositorio

```text
F1/                 notebooks de la Fase 1
F2/                 notebooks de la Fase 2
F3/                 notebook de la Fase 3
F4/                 archivos de la Fase 4
data/raw/           datos originales
data/processed/     conjuntos procesados
src/                módulos reutilizables
artefactos/         objetos ajustados
docs/               metadatos, resultados y anexos
```

La carpeta `src/` contiene solamente código fuente. Los archivos serializados se almacenan en `artefactos/`.

## Instalación

### Linux o macOS

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

### Windows PowerShell

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Luego, iniciar Jupyter:

```bash
jupyter lab
```

Las versiones oficiales de las dependencias se encuentran en `requirements.txt`.

## Ejecución

Los notebooks deben ejecutarse desde la raíz del repositorio y en el siguiente orden:

1. Fase 1.
2. Fase 2.
3. `F3/S2_F3_NucleoAlgoritmico_Eficiencia_POO.ipynb`.

En cada notebook se recomienda seleccionar **Kernel → Restart Kernel and Run All Cells**. La ejecución de la Fase 3 debe finalizar sin errores y generar los conjuntos procesados, parámetros, mediciones de eficiencia, metadatos y anexos correspondientes.

## Decisiones técnicas principales

- Semilla aleatoria fijada en 42.
- Formatos de fecha declarados explícitamente.
- Partición agrupada por `permit_number`.
- Ajuste de las transformaciones solo con datos de entrenamiento.
- Un permiso por fila como unidad principal de análisis.
- Comparación reproducible de implementaciones mediante tiempo y memoria.
- Organización modular mediante clases, transformadores y un pipeline reutilizable.

## Convención de commits

- `feat`: nuevas funcionalidades.
- `fix`: correcciones.
- `data`: datos y transformaciones.
- `test`: pruebas y validaciones.
- `perf`: eficiencia y optimización.
- `docs`: documentación.
- `refactor`: reorganización del código.

Las contribuciones registradas pueden comprobarse mediante:

```bash
git shortlog -sne HEAD
```
