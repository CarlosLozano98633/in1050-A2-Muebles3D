
## 3. Por qué con IA y por qué este modelo
El *modelo fue seleccionado* debido a que, el realizar un modelado, en blender por ejemplo de algún mueble o algo en específico, requiere de tiempo y esfuerzo innecesario, que con **Stabilityai/stable-fast-3D** puede realizar en poco tiempo.

Sin embargo, nuestro modelo no es el único, por ejemplo en **Hugging Face** teníamos varias opciones, por ejemplo:

- ***TRELLIS.2-4B***: El cual es un modelo de Microsoft, sin embargo no escogímos este modelo debido a que es demasiado pesado para correr en Google Collab, o en alguna computadora con gráfica.

A continuación presentamos una tabla comparativa entre los dos modelos.
### Stabilityai/stable-fast-3D

| **Dato** | **Respuesta** |
|:--- | --- |                           
| Identificador |[Stabilityai/stable-fast-3d](https://huggingface.co/stabilityai/stable-fast-3d) |
| Tarea | Este modelo está entrenado para generar un plano 3D desde una Imagen |
| Número de parámetros | FP32 /1B|
| Licencia |stabilityai-ai-community |
| Limitación (Model Card) |El modelo no fue entrenado para hacer representaciones fácticas o verdaderas de personas o eventos. Como tal. el uso del modelo para generar dicho contenido está fuera del alcance de las capacidades de este modelo. |

![Imagen del modelo](docs/img/ImagenST.png)


### TRELLIS.2-4B
|**Dato**|**Respuesta**|
|---|---|
|Identificador| TRELLIS.2-4B|
|Tarea| Generador de alta fidelidad de **imagen-3D** |
|Número de Parámetros| ***4B FP32***; aunque marca que en necesidad de hardware necesita una NVIDIA GPU con un mínimo de **24GB de VRAM**|
|Licencia| Este modelo es lanzado desde la licencia del MIT; el código y la base de datos son compartidas publicamente para facilitar su reproducción e investigación futura.|
|Limitación (Model Card)|- **Problemas geométricos (pequeños agujeros):** Aunque O-Voxels maneja topologías complejas, las mallas generadas pueden presentar pequeños agujeros o discontinuidades. Para solucionarlo, se proporcionan herramientas de posprocesamiento que permiten rellenarlos y obtener modelos adecuados para impresión 3D.                                                                                                             **- Modelo base sin alineación:** TRELLIS.2-4B es un modelo preentrenado que no ha sido ajustado mediante preferencias humanas ni optimizado para estilos estéticos específicos. Por ello, los resultados pueden variar según los datos de entrenamiento y es posible que se necesiten varios intentos para conseguir el resultado deseado.|

![Imagen del Modelo](docs/img/ImagenTRELLIS.png)

Finalmente se eligió el modelo Stability, debido a que necesitaba menos parámetros por lo que es mucho más flexible su uso en dispositivos con menor capacidad de renderizado.
