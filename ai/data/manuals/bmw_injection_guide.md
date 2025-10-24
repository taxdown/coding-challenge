# Guía de Inyección BMW (multimodelo)

> Aplica a plataformas BMW con **inyección electrónica** (ej.: R1200/R1250 bóxer, F800/F900 paralelos, S1000, K1600). Enfoque por **marca/sistema** (BMS-K, BMS-X, Bosch/Siemens), no por modelo concreto.

## Seguridad y requisitos
- Desconecta batería al manipular conectores de inyectores/rail.
- Aliviar presión del combustible antes de desconectar la línea (lleva ~3.5–4.0 bar).
- No fumes ni trabajes cerca de fuentes de ignición.

## Arquitectura típica
- **ECU (BMS-K/BMS-X/Bosch ME):** controla inyección/encendido, CAN-bus.
- **Sensores clave:** TPS, MAP, IAT, ECT, Lambda (narrowband/UEGO).
- **Actuadores:** inyectores EV14/EV6, bomba sumergida, regulador integrado.
- **Presión nominal rail:** 3.5–4.0 bar (según familia).

## Procedimientos comunes

### 1) Comprobación de presión y estanqueidad
1. Conecta manómetro en línea de servicio (si disponible) o en serie con adaptador.
2. Contacto ON: bombeo primario 2–3 s, debe subir a **3.5–4.0 bar** rápidamente.
3. Caída de presión en 5 min: ≤ 0.5 bar. Si cae más, revisar válvula de retención, regulador o inyectores que gotean.

### 2) Test de inyectores (flujo y estanqueidad)
- Extrae rail con inyectores sujetos, conecta recipientes graduados.
- Activa test de **“Injector Output/Leak test”** con herramienta (ISTA/D, Motoscan, GS-911).
- Desviación aceptable entre cilindros: ≤ 5 % de volumen a ciclo fijo.
- Sustituye toricas si hay “spray irregular” o goteo.

**Par de apriete rail/inyección (orientativo):**
- Tornillos rail a colector M6: **9–10 N·m**.
- Inyector a rail (clip): enclavamiento completo; sin par específico (ver manual de la plataforma).

### 3) Adaptaciones y aprendizaje
- Tras limpieza de cuerpos/tps, realiza **reset de adaptaciones**:
  - Con herramienta: “Reset adaptations” de ECU.
  - Manual básico: contacto ON, abre gas a tope 2× 10 s, contacto OFF (en algunas BMS funciona solo para TPS).
- Con motor a 80–100 °C, dejar ralenti 5–10 min para realimentación lambda y re-aprendizaje.

### 4) Diagnóstico de mezcla
- **Códigos lambda** frecuentes: mezcla pobre/rica (P0171/P0174).
- Revisa:
  - Tomas de aire en manguitos post-MAF/TMAP (falsos a ralentí).
  - Presión rail dentro de especificación bajo carga.
  - Estado del filtro (interno en bomba en algunas series).
  - Señal TPS lineal y coherente (sin saltos).
- En lazo cerrado, oscilación de lambda: 0.1–0.9 V (narrowband) a ~1–2 Hz. Si no oscila, comprobar sensor y fugas de escape.

## Mantenimiento preventivo
- Filtro de combustible: según plataforma, cada 40–60 000 km (si externo) o junto con módulo de bomba (si integrado).
- Limpieza de cuerpos de mariposa: spray específico, sin inundar eje.
- Verificación de PCV y respiraderos del cárter.

## Señales y valores guía
- **TPS:** 0.5–0.7 V en cerrado, ~4.2–4.5 V a WOT (lineal; verificar en live data).
- **IAT/ECT:** coherentes con ambiente y temperatura; deltas anómalos indican sensor fuera de rango.
- **RPM de arranque:** > 250 rpm; si menor, revisar batería/arranque.
- **Tensión de carga:** 13.8–14.5 V a 3 000–5 000 rpm.

## Fallos típicos y corrección
- Arranque en caliente difícil:
  - Verificar caída de presión rail (válvula retención).
  - Chequear vapor lock en climas muy cálidos; aislar línea cerca de culata.
- Tirones a 3 000–4 000 rpm:
  - Adaptaciones fuera de rango; reset + aprendizaje.
  - Fugas en toma entre MAF/TMAP y cuerpo.
- Código mezcla pobre banco 1:
  - Revisa escape por fugas antes de sonda (lectura falsa).
  - Comprobar inyectores parcialmente obstruidos (ultrasonidos + kit juntas).

## Par de apriete y conexiones (orientativos BMW)
- Abrazaderas goma admisión: **6–7 N·m**.
- Cuerpo de mariposa al colector: **9–10 N·m**.
- Sensor MAP/TMAP M5: **4–5 N·m**.
- Borne batería: **5 N·m**.

## Buenas prácticas
- Siempre sustituye **toricas** de inyectores al reinstalar (lubrica con una gota de aceite limpio).
- No inviertas conectores de inyectores (marca cilindro).
- Tras cualquier intervención, realiza prueba de fugas y aprendizaje en caliente.

## Notas por familias (referencia rápida)
- **R1200/R1250 bóxer:** sensibilidad a tomas de aire en tubos de equilibrado; sincronización electrónica mediante flujos.
- **F800/F900:** TPS y paso a paso integrados; revisar drift del TPS tras limpiar cuerpos.
- **K1600:** rail largo con 6 inyectores; atención a uniformidad de flujo.
- **S1000:** alto caudal; presión estable bajo carga crítica en pista.

> Esta guía es deliberadamente **multimodelo BMW** para forzar recuperación por **marca/sistema** (inyección) y no por modelo concreto.
