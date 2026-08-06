# El Cruce — simulador de decisiones patrimoniales

App estática de una sola página para comparar caminos financieros de un hogar: vender o no vender activos, pagar deudas con esa plata, irse a arriendo o volver a comprar, y ver qué flujo de caja mensual queda en cada caso.

Los datos vienen de la plantilla de presupuesto de pareja (ingresos, cuentas mensuales, saldos de deuda) y quedan precargados en el archivo. Todo es editable desde la interfaz.

## Qué hace

- **Hoy**: ingresos contra salidas, el hueco mensual, deuda total y patrimonio neto.
- **La bifurcación**: diagrama de caminos, cada rama termina en el flujo mensual que quedaría.
- **Escenarios**: se prende y se apaga qué se vende, qué deudas se pagan (todas / solo las caras / ninguna) y dónde se vive después (quedarse / arriendo / comprar otra, de contado o con crédito).
- **Comparación a 5 años**: proyección mes a mes con intereses, liberación de cuotas cuando una deuda llega a cero, inflación de gastos, rendimiento del sobrante y costo de financiar los meses en rojo.
- **Datos**: tablas editables de activos, deudas, cuentas, ingresos y supuestos. Exporta e importa JSON.

## Cómo se usa

Abrir `index.html` en cualquier navegador. No necesita servidor, ni build, ni dependencias.

## Publicar en GitHub Pages

```bash
git init
git add .
git commit -m "El Cruce v1.0"
git branch -M main
git remote add origin https://github.com/USUARIO/REPO.git
git push -u origin main
```

Luego en el repositorio: **Settings → Pages → Source: Deploy from a branch → Branch: main / (root) → Save**.
Queda publicado en `https://USUARIO.github.io/REPO/`.

> El repositorio es público por defecto: si va a subir cifras reales del hogar, cree el repo como **privado** y use Pages en un plan que lo permita, o deje los valores en cero y cargue los datos reales con el botón "Cargar datos" desde el JSON local.

## Supuestos que hay que confirmar

Están marcados en fondo azul dentro de la app:

- Valor comercial del carro y del campo.
- Tasas efectivas anuales de cada deuda (van estimadas por tipo de crédito).
- Costo de vender (comisión + escrituración), rendimiento del sobrante, inflación y valorización.

No incluye impuesto de ganancia ocasional sobre la venta del inmueble, penalidades por prepago ni cambios de tasa. Antes de mover un activo, validar el efecto tributario con un contador y el saldo de liquidación con el banco.

## Estructura

```
index.html    Todo: datos, motor de simulación, interfaz y gráficos SVG
README.md
```
