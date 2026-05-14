# Simulación TP2 - Competencia de Locales de Comida Rápida

Este repositorio contiene el notebook `simulacion_tp2.ipynb` del Trabajo Práctico 2 de Operativa. El notebook simula decisiones estratégicas para un local de comida rápida en un patio de comidas, comparando opciones de:

- Publicidad
- Calidad
- Empleados en sector de pedidos
- Lugares de espera
- Empleados en preparación

## Contexto del problema

El modelo está basado en el trabajo práctico donde cada grupo administra un local de comida rápida en un shopping. En la primera ronda, la demanda depende de publicidad y calidad, pero no de imagen. El objetivo es maximizar el beneficio neto teniendo en cuenta los costos de publicidad, calidad, empleados y espera.

## Cómo funciona la simulación

El notebook realiza lo siguiente:

1. Define los parámetros del juego, incluyendo costos, capacidad de empleados y el lambda asociado a la posición de demanda.
2. Crea posibles combinaciones de decisiones de nuestro local.
3. Simula escenarios donde los demás grupos eligen decisiones de forma aleatoria.
4. Calcula la posición de nuestro local en el ranking de demanda usando un "factor de demanda".
5. Estima el beneficio neto para cada combinación considerando:
   - ingresos por clientes atendidos
   - costos de publicidad
   - costos de empleados en atención y preparación
   - costos de lugares de espera

## Qué representa cada opción

- **Publicidad:** mayor inversión aumenta el costo fijo por hora pero mejora el ranking de demanda.
- **Calidad:** mayor calidad reduce el margen bruto por ticket, pero también mejora el ranking de demanda.
- **Empleados en pedidos:** determinan la capacidad de atención en la toma de pedidos. Más empleados reducen la saturación del primer sector.
- **Lugares de espera:** permiten que más clientes permanezcan en cola en el sector de pedidos; cada lugar aumenta el costo por hora.
- **Empleados en preparación:** determinan la velocidad del segundo sector, donde se prepara el pedido.

## Cómo interpretar los resultados

- El notebook devuelve una combinación recomendada y un beneficio promedio estimado.
- El análisis muestra si conviene gastar más en calidad o en personal, y cuánto margen hay entre diferentes estrategias.
- La simulación usa Monte Carlo: se repite el cálculo muchas veces para obtener un promedio y una desviación estándar.

## Uso

1. Abrir `simulacion_tp2.ipynb` en Jupyter Notebook / JupyterLab.
2. Ejecutar las celdas en orden.
3. Leer la sección de resultados y el gráfico final.
4. Si quieres explorar otras hipótesis, ajusta las combinaciones y vuelve a ejecutar.

## Recomendaciones para tus compañeros

- Trabajen en ramas separadas cuando hagan cambios grandes.
- No modifiquen el notebook sin probar todas las celdas.
- Añadan notas o comentarios en el notebook para explicar qué decidieron cambiar y por qué.

## Objetivo

Encontrar la mejor situación operativa para maximizar el beneficio en la primera ronda, teniendo en cuenta que el ranking de imagen no se utiliza en la ronda inicial.
