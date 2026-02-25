# Lab 26 – Power BI: Informe básico + Seguridad a Nivel de Fila (RLS)

## Objetivo
Montar un informe sencillo en Power BI y aplicar seguridad a nivel de fila (RLS) para que cada usuario vea solo los datos que le corresponden.  
Nivel básico, orientado a entender el flujo y poder defenderlo en una entrevista.

---

## Qué he hecho en este laboratorio

1. He creado una tabla simple de ventas con la columna `Ciudad`.
2. He hecho una transformación mínima en Power Query (tipos de datos / limpieza básica).
3. He creado una visual sencilla (tabla/gráfico) para visualizar las ventas.
4. He configurado RLS con un rol que filtra por ciudad y lo he validado con “Ver como”.

---

## Concepto (muy corto)
Power BI sirve para transformar datos (Power Query), modelarlos y visualizarlos en un informe.  
RLS (Row-Level Security) añade control de acceso a nivel de dato: no solo quién entra al informe, sino qué filas puede ver.

---

## Configuración utilizada

- Tabla: `Ventas`
- Columnas: `Ciudad`, `Importe`
- Rol RLS: `RLS_Madrid`
  - Filtro: `Ventas[Ciudad] = "Madrid"`

---

## Evidencias

### 01 – Roles RLS (filtro por ciudad)
<img src="images/01-manage-roles-rls.png" width="800">

Editor de roles con el filtro aplicado para limitar los datos a la ciudad de Madrid.

---

### 02 – Validación con “Ver como” (solo Madrid)
<img src="images/02-view-as-rls-madrid.png" width="800">

Prueba del rol en Power BI Desktop mostrando que el informe queda filtrado únicamente a Madrid.

---

## Qué le diría a un cliente o en entrevista
“Power BI lo he usado a nivel básico: sé cargar datos, hacer limpieza mínima en Power Query, montar una visual simple y aplicar RLS para que cada usuario vea solo su parte del dataset. En un entorno real, los roles se asignan a usuarios o grupos en el servicio de Power BI.”
