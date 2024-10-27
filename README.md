# Proyecto de Datos Legacy del Banco XYZ

Este proyecto proporciona los datos necesarios para un desafío de migración y modernización de procesos batch, enfocado en la transformación de sistemas legacy de un banco ficticio, Banco XYZ. Los datos están organizados en archivos CSV que representan distintos informes y operaciones del sistema legacy actual.

## Estructura del Proyecto

El proyecto contiene la siguiente estructura de directorios y archivos.

### Archivos CSV

Los archivos en el directorio `data/` representan los distintos tipos de datos legacy que se utilizarán en los procesos batch:

1. **`transacciones.csv`**: Contiene información de transacciones diarias, con problemas comunes como montos negativos, datos duplicados y formatos de fecha incorrectos.

2. **`intereses.csv`**: Proporciona datos sobre cuentas bancarias y el cálculo de intereses mensuales, incluyendo registros con edades no válidas, saldos vacíos y registros duplicados.

3. **`cuentas_anuales.csv`**: Incluye el historial de operaciones anuales de las cuentas bancarias, con posibles errores como fechas mal formateadas, descripciones faltantes y montos negativos.


## Problemas Simulados en los Datos

Los datos han sido diseñados con algunos problemas típicos para simular un entorno legacy:
- **Montos negativos o cero**: Anomalías que requieren validación.
- **Formatos de fecha inconsistentes**: Algunas fechas están en un formato incorrecto (`yyyy/MM/dd` en lugar de `yyyy-MM-dd`).
- **Datos faltantes o nulos**: Algunos campos, como el saldo o la descripción de la transacción, están vacíos.
- **Registros duplicados**: Múltiples filas con los mismos datos.
- **Valores fuera de rango**: Por ejemplo, edades no realistas o tipos de transacción no válidos.

Estos problemas deberán ser gestionados mediante políticas de reintento y omisión en Spring Batch para garantizar la integridad y calidad de los datos procesados.

**¡Buena suerte con el desafío!**