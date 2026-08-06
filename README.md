# El Cruce — decisiones patrimoniales de la casa

App estática de una sola página. Toma los datos reales del presupuesto del hogar y responde qué pasa con la plata según el camino que se tome: vender, arrendar, refinanciar, reacomodar la familia o no mover nada.

## Qué hace distinto

- **No asume que vender es la solución.** Evalúa 816 combinaciones válidas de 12 palancas, cada una proyectada mes a mes durante 5 años, y entrega tres respuestas: la mejor en general, la mejor **sin vender el apartamento** y la que menos mueve a la familia.
- **Trata cada activo como es.** Un carro con crédito vigente puede tener patrimonio negativo: venderlo no entra plata, exige ponerla. Lo que se gana es la cuota.
- **Cuenta lo que cuesta vender de verdad.** Comisión inmobiliaria con IVA, derechos notariales, retención en la fuente, ganancia ocasional con la exención de 5.000 UVT del artículo 311-1, cancelación de hipoteca y certificados.
- **Pesa el costo humano.** Cada palanca tiene un costo familiar además del financiero, y se puede subir o bajar cuánto importa.

## Las palancas

Activos: vender o arrendar el apartamento, vender el carro, vender o arrendar el campo.
Familia: que la hija regrese del exterior, dejar de cubrir la renta de la abuela, irse a vivir con el hijo, que el hijo aporte, sanear las deudas del hijo.
Deudas: refinanciar lo caro en un solo crédito.
Vivienda: volver a comprar más pequeño.

## Cómo publicarla

El archivo **tiene que llamarse exactamente `index.html`** — sin paréntesis, sin espacios, sin números. Si el navegador lo descargó como `index (7).html`, renómbrelo antes de subirlo o GitHub Pages nunca lo va a encontrar.

```bash
git init
git add index.html README.md
git commit -m "El Cruce v2"
git branch -M main
git remote add origin https://github.com/USUARIO/REPO.git
git push -u origin main
```

Settings → Pages → Deploy from a branch → main / (root) → Save.
Queda en `https://USUARIO.github.io/REPO/`

> Si va a dejar las cifras reales adentro, cree el repositorio **privado**. En un repo público cualquiera puede leer el archivo. La alternativa: dejar los valores en cero, publicar, y cargar los datos reales con el botón "Cargar datos" desde el JSON local.

## Datos tributarios de referencia (2026)

- UVT: $52.374 — Resolución DIAN 000238 de 2025.
- Ganancia ocasional: 15% sobre la utilidad, para inmuebles con más de dos años de tenencia.
- Exención vivienda de habitación: 5.000 UVT ($261.870.000), condicionada a depositar el producto en cuenta AFC o destinarlo a pagar el crédito hipotecario de esa vivienda o de una nueva (art. 311-1 E.T.).
- Retención en la fuente: 1% del precio (2,5% por encima de 20.000 UVT), la practica el notario y es un anticipo del impuesto.
- Derechos notariales: ~0,54% de la escritura, se reparten entre las partes.
- Beneficencia y registro (1,67%–2%): los asume el comprador.

Nada de esto es asesoría. Antes de firmar, validar el costo fiscal soportado con un contador y el saldo de liquidación con el banco.
