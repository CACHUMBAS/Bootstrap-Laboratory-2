# 📐 Conclusiones de Maquetación y Sistema Grid en Bootstrap

## 1. ¿Cómo calcula Bootstrap el ancho en porcentajes automáticos?

Bootstrap utiliza un sistema de rejilla flexible (Flexbox Grid) dividido en un total de **12 columnas**. El ancho porcentual de cualquier columna se calcula matemáticamente mediante la siguiente fórmula:

$$\text{Ancho Porcentual (\%)} = \left( \frac{\text{Número de Columnas}}{12} \right) \times 100$$

Cuando definimos las clases `col-md-9` y `col-md-3`:
* **Columna Principal (`col-md-9`):** $(9 / 12) \times 100 = \mathbf{75\%}$ del ancho disponible de la fila.
* **Barra Lateral (`col-md-3`):** $(3 / 12) \times 100 = \mathbf{25\%}$ del ancho disponible de la fila.
* **Suma Total:** $75\% + 25\% = \mathbf{100\%}$. Esto garantiza que ambas columnas compartan la misma fila de forma exacta en pantallas $\ge 768\text{px}$ (punto de ruptura `md`).

Por debajo de 768px, el modificador `-md-` deja de aplicar ancho porcentual y cada columna toma el **100%** de forma automática, apilándose verticalmente para facilitar la experiencia móvil.

---

## 2. Tabla Resumen de Equivalencias del Grid (12 Columnas)

| Clase Bootstrap | Fracción del Grid | Porcentaje Calculado en CSS (`width`) |
|---|---|---|
| `col-*-1` | $1/12$ | 8.3333% |
| `col-*-2` | $2/12$ | 16.6667% |
| `col-*-3` *(Barra Lateral)* | $3/12$ | **25.0000%** |
| `col-*-4` | $4/12$ | 33.3333% |
| `col-*-5` | $5/12$ | 41.6667% |
| `col-*-6` | $6/12$ | 50.0000% |
| `col-*-7` | $7/12$ | 58.3333% |
| `col-*-8` | $8/12$ | 66.6667% |
| `col-*-9` *(Contenido)* | $9/12$ | **75.0000%** |
| `col-*-10` | $10/12$ | 83.3333% |
| `col-*-11` | $11/12$ | 91.6667% |
| `col-*-12` | $12/12$ | 100.0000% |
