---
title: Unidad 10
---
# Unidad 10: PyCUDA

## Contenido de la unidad

<img src="_static/images/contenidoU10_.png"/>

## Comparemos a las CPU contra las GPU

::::{grid}
:gutter: 3

:::{grid-item-card}
:class-body: text-right
:class-header: bg-light text-center
```{dropdown} CPU
- Varios núcleos, pero generalmente menos que una GPU.
- Baja latencia.
- Bueno para procesamiento en serie.
- Puede realizar un puñado de operaciones a la vez.
```
:::

:::{grid-item-card}
:class-body: text-right
:class-header: bg-light text-center
```{dropdown} GPU
- Muchos núcleos para procesamiento en paralelo.
- Alto rendimiento.
- Bueno para procesamiento en paralelo.
- Puede realizar miles de operaciones a la vez.
```
:::

::::

<div align="center">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/-P28LKWTzrI" frameborder="0" allowfullscreen></iframe>
</div>


```{tip}
- <a href="https://blogs.nvidia.com/blog/whats-the-difference-between-a-cpu-and-a-gpu/" target="_blank">Leer un blog de Nvidia comparando GPU con las CPU</a>
```

## PyCUDA

PyCUDA ofrece un acceso sencillo y pythonico a la API de computación paralela Compute Unified Device Architecture (CUDA), de Nvidia. Aunque ya existen varios envoltorios para la API de CUDA, ¿por qué elegir PyCUDA?

**Gestión automática de objetos vinculada a su ciclo de vida.** Este enfoque, simplifica significativamente la escritura de código que es correcto, libre de fugas y resistente a caídas. PyCUDA también maneja las dependencias, lo que significa que no se desvinculará de un contexto antes de liberar toda la memoria asignada en él.

**Completitud.** PyCUDA pone a tu disposición toda la potencia de la API de controladores de CUDA, si así lo deseas.

**Verificación automática de errores.** Todos los errores de CUDA se traducen automáticamente en excepciones de Python.

**Velocidad.** Dado que la capa base de PyCUDA está escrita en C++, todas las ventajas mencionadas anteriormente prácticamente no tienen coste adicional.

```{tip}
Ver el siguiente recurso:

<a href="https://www.iitk.ac.in/hpc4se/downloads/PyCUDA-AH.pdf" target="_blank">PyCUDA Tutorial</a>
```

## Usar la GPU para multiplicar y sumar elementos

```{tip}
Ver el Notebook: `PyCUDA_multiplicar_sumar_elementos.ipynb`

O acceder a el desde <a href="https://colab.research.google.com/drive/1vm8jyD1DNf3zgS_kEIUU6FpXC1J0Xjpq?usp=sharing" target="_blank">PyCUDA_multiplicar_sumar_elementos_working.ipynb</a>

```

## Usar la GPU para multiplicar matrices

```{tip}
Ver el Notebook: `PyCUDA_multiplicar_matrices.ipynb`

O acceder a el desde <a href="https://colab.research.google.com/drive/1hpG_DpJN_Uax4_1yjgFNjG-_9YJU1397?usp=sharing" target="_blank">PyCUDA_multiplicar_matrices_working.ipynb</a>

```

## Comparativa en la creación de imágenes desde textos en GPU y en CPU

```{tip}
Ver el Notebook: `Stable_Diffusion_GPU_vs_CPU.ipynb`

O acceder a el desde <a href="https://colab.research.google.com/drive/1mG2uJrREUsv6uLVUIMbg3tM7VViv9MeU?usp=sharing" target="_blank">Stable_Diffusion_GPU_vs_CPU_working.ipynb</a>

```

## Comprendamos la indexación

```{tip}
Acceder a el desde <a href="https://anuradha-15.medium.com/cuda-thread-indexing-fb9910cba084" target="_blank">https://anuradha-15.medium.com/cuda-thread-indexing-fb9910cba084</a>

```

<img src="_static/images/U10_3.jpg"/>

<img src="_static/images/U10_1.jpg"/>

<img src="_static/images/U10_2.jpg"/>
