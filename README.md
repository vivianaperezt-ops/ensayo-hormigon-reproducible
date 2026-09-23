# Ensayo de Compresión en Probetas Cilíndricas de Hormigón

Entorno computacional reproducible para el análisis, cálculo y visualización del ensayo de compresión axial en probetas cilíndricas de hormigón.

## 1. Propósito del Proyecto
Auditar y procesar los datos de laboratorio de un ensayo de compresión destructivo en probeta cilíndrica, corrigiendo omisiones de unidades, parametrizando variables geométricas y determinando la resistencia máxima ($f_{max}$).

## 2. Estructura del Repositorio
* `data/raw/`: Archivos originales intactos de laboratorio (`ensayo_hormigon.xlsx`).
* `data/processed/`: Planilla normalizada (`datos_procesados.xlsx`) con dimensiones y fórmulas explícitas.
* `figures/`: Gráfico final generado (`grafico_esfuerzo_desplazamiento.png`) con unidades en los ejes.
* `docs/`: Documentación de soporte, notas originales e informe preliminar heredado.

## 3. Parámetros y Unidades
* **Dimensiones de probeta:** Diámetro $D = 150\text{ mm}$, Altura $H = 300\text{ mm}$.
* **Área transversal ($A$):** Parametrizada como $A = \frac{\pi \cdot D^2}{4} \approx 17671.46\text{ mm}^2$.
* **Carga axial ($P$):** Expresada en kilonewtons [$\text{kN}$].
* **Desplazamiento axial ($u$):** Registrado en milímetros [$\text{mm}$].
* **Esfuerzo ($\sigma$):** Calculado en megapascales [$\text{MPa}$] ($1\text{ MPa} = 1\text{ N/mm}^2$):
  $$\sigma = \frac{P \times 1000}{A}$$

## 4. Procedimiento de Reproducción
1. Abrir `data/processed/datos_procesados.xlsx`.
2. Verificar en la celda del diámetro el valor de $150\text{ mm}$.
3. Corroborar el cálculo dinámico del área mediante la fórmula geométrica transversal.
4. Comprobar que en la columna de esfuerzo se divida la carga convertida a Newtons por el área en $\text{mm}^2$.
5. La resistencia máxima a la rotura obtenida es $f_{max} = 25.46\text{ MPa}$ para una carga de rotura de $450\text{ kN}$ y desplazamiento de $0.925\text{ mm}$.

## 5. Supuestos y Limitaciones
* Velocidad de carga uniforme y continua sin ciclos de descarga.
* No se instrumentó deformación transversal (sin estimación de módulo de Poisson).ara ensayo de compresión en probetas de hormigón.
