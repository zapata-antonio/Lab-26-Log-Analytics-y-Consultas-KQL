# Lab 26: Power BI – Seguridad a Nivel de Fila (RLS)

## Objetivo
Montar un control de acceso básico para que cada persona/departamento vea **solo** la parte de datos que le corresponde (por ejemplo, por ciudad).

## Qué he montado
- Un dataset sencillo de ventas con la columna **Ciudad**.
- Dos roles de seguridad (RLS) en Power BI Desktop:
  - **RLS_Madrid** → solo puede ver registros de *Madrid*
  - **RLS_Sevilla** → solo puede ver registros de *Sevilla*
- Validación usando **“Ver como”** para comprobar que el filtro realmente limita la información.

## Pasos (resumen)
1. Crear tabla `Ventas` con columnas `Ciudad` e `Importe`.
2. Ir a **Modelado → Administrar roles** y definir los roles con filtros por ciudad.
3. Probarlo con **Modelado → Ver como**.

## Evidencias
- **Roles RLS configurados:** `01-roles-rls-madrid-sevilla.png`
- **Prueba “Ver como” (Madrid):** `02-view-as-rls-madrid.png`
- *(Opcional)* **Prueba “Ver como” (Sevilla):** `03-view-as-rls-sevilla.png`

## Para entrevista (cómo lo explico)
“Esto es un ejemplo simple de **gobierno del dato**: no solo proteges el acceso a un informe, también controlas qué filas puede ver cada usuario.
En un entorno real, esto se suele combinar con asignación de roles a **usuarios o grupos** (por ejemplo, grupos de Entra ID / Azure AD) en el servicio de Power BI.”
