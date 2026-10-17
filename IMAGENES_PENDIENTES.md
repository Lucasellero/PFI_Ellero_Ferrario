# Cambios pendientes en las imágenes del informe

Lista unificada de las tres tandas de revisión EP3. Revisé cada imagen y los textos entre comillas son los que aparecen hoy en el archivo. Al reemplazar una imagen, conviene mantener el mismo nombre de archivo para no tocar el `.tex`.

El orden va de lo que más pesa en la rúbrica a lo opcional.

---

## A. Obligatorias (contradicen el texto o tienen errores visibles)

### 1. Fig. 3.6, diagrama de casos de uso
**Archivo:** `Imagenes/Diagrama_Casos_Uso_PFI.png`

- [x] Borrar el recuadro **"Banco de figuras de casos de uso"** de la izquierda, abajo de la leyenda. Es un resto de la plantilla.
- [x] Borrar las dos flechas punteadas que van del Bloque 3 a **"Autenticarse"**: la que sale de "Configurar Camaras" y la que sale de "Validar visualizacion del video". El panel local no pide autenticación, y así lo dice el texto en 3.4.1.
- [x] Cambiar el título del bloque **"Bloque 3 - Panel de Control"** por **"Bloque 3 - Panel de operación local"**.
- [x] Cambiar **"Bloque 2 - App Mobile"** por **"Bloque 2 - Aplicación móvil"**.
- [x] Agregar en el Bloque 2 dos casos de uso nuevos para el RF15, con flecha desde "Responsable a Cargo" y una flecha punteada hacia "Autenticarse":
  - **"Marcar alerta como resuelta"**
  - **"Administrar familiares"**
- [x] Agregar la flecha punteada que falta de **"Detectar Desvío"** a **"Registrar Evento"**. El texto dice que todo evento, incluido el desvío, incluye su registro.
- [x] ~~Rotular con «include» las flechas punteadas~~. Descartado: el texto de 3.4.1 ya aclara que las relaciones punteadas son dependencias include.
- [ ] Tildes y traducción:
  - "Pose Estimation" → **"Estimar pose"** ← sigue pendiente
  - "Detección de Caidas" → **"Detección de caídas"** ✓
  - "Camara IP" → **"Cámara IP"** ✓
  - "Ubicar camaras" → **"Ubicar cámaras"** ✓
  - "Configurar Camaras" → **"Configurar cámaras"** ✓
  - "Validar visualizacion del video" → **"Validar visualización del video"** ✓

### 2. Fig. 3.7, diagrama de flujo de información ✓
**Archivo:** `Imagenes/Diagrama_Flujo_Informacion.png`

- [x] Reemplazada con la versión rediseñada: alerta inmediata en la nube, línea base diaria con bifurcación en desvío y reportes, confirmación de caída con clasificador temporal y CLIP, envío de metadatos y consulta de reportes en la app.

### 3. Fig. 3.9, diagrama de arquitectura ✓
**Archivo:** `Imagenes/Diagrama_Arquitectura.png`

- [x] Reemplazada: Firebase separado en Authentication (inicio de sesión) y Cloud Messaging (alerta desde Elastic Beanstalk y push a la app), sincronización de metadatos.
- [ ] Sin resolver: el recuadro "Red Privada de la Controladora" no dice "(prevista)". El texto de 3.4.5 sí aclara que es diseño previsto.

### 4. Fig. 3.11, base de datos en la nube ✓
**Archivo:** `Imagenes/Diagrama_Base_Datos_Nube.png`

- [x] Reemplazada: `event_id` en EVENTO, relación RESIDENTE–EVENTO ("protagoniza"), `json` en lugar de `jsonb`, y cardinalidades opcionales en HOGAR–KIT y RESIDENTE–LINEA_BASE.

### 5. Fig. 2.2, síndrome post-caída ✓
**Archivo:** `Imagenes/Sindrome_Post_Caida.png`

- [x] Corregir **"Sincrome Post-caida"** a **"Síndrome post-caída"**.

### 6. Fig. 3.2 y 3.5, mockups de reportes y de día en orden ✓
**Archivos:** `Imagenes/Mockup_Mobile_Flujo2.png` y `Imagenes/Mockup_Mobile_Oscuro1.png` (modo oscuro)

El texto ya aclara lo del "despertar", pero el mockup muestra cosas que el sistema no detecta. Para esta pantalla:

- [x] **Pantalla 04, Rutina de la semana:**
  - Reemplazar **"Despertar · Hoy 7:35 · habitual 7:00–7:45"** por **"Cocina · 40 min · habitual 35–50 min"** o **"Movilidad"**, que son los indicadores reales.
  - En **"Comió · Hoy 9:10 · habitual 8:00–9:00"**, el horario cae fuera del rango pero lleva tilde verde. Cambiarlo a **8:40**.
  - Como la pestaña activa es **"Semana"**, cambiar "Hoy" por **"Promedio"** en los indicadores.
- [x] **Pantalla 04, Eventos de la semana:** reemplazar **"Rutina de sueño alterada · Se acostó 2 h más tarde"** por un evento que el sistema sí produce, por ejemplo **"Menos movimiento que lo habitual"** o **"No salió de casa"**.
- [x] **Pantalla 05:** reemplazar **"Tomó la medicación"** por **"Comió, bebió o tomó la medicación"**. La cámara no distingue la medicación por separado.
- Nota: también se actualizaron 01 (mail) y el modo oscuro (Mockup_Mobile_Oscuro1.png); se ajustaron chapter03 y chapter06 para no mencionar el "despertar".


---

## B. Recomendadas (consistencia y forma)

### 7. Fig. 3.8, diagrama de componentes ✓
**Archivo:** `Imagenes/Diagrama_componentes.png`

- [x] **"Fusion · Combina esqueleto y CLIP"** → **"Fusión · Confirma caídas y combina esqueleto con CLIP"**. El texto le asigna también la confirmación de caídas.
- [x] **"App Movil"** → **"App móvil"**.
- [x] **"Panel de operaciones local"** → **"Panel de operación local"**, como en el resto del informe.

### 8. Fig. 2.3, monitoreo con procesamiento local (marco teórico) ✓
**Archivo:** `Imagenes/Flujo_PFI.png`

Ya es bastante genérica, así que alcanza con corregir los rótulos:
- [x] **"Notificaciones PUSH en la App Mobile"** → **"Notificaciones en la aplicación móvil"**.
- [x] **"Machine Learning: construcción de línea base de comportamiento"** → **"Aprendizaje automático: construcción de la línea base de comportamiento"**.

### 9. Capturas del modelo financiero (Fig. 3.14 a 3.20), opcional

Surgió de la revisión interna (H117), no es un pedido de la cátedra. Es por consistencia con el formato de números del texto.
**Archivos:** `captura_supuestos.png`, `captura_wacc.png`, `captura_bear_flujo.png`, `captura_base_datos.png`, `captura_base_indicadores.png`, `captura_base_flujo.png`, `captura_bull_flujo.png`

- [ ] Configurar la planilla en **español (Argentina)** y volver a exportar. Hoy figura "1,360,000", "$206.61", "0.87%" y "14.7x", y debe quedar **1.360.000**, **206,61**, **0,87 %** y **14,7x**.
- [ ] Rótulos en inglés:
  - "Infraestructura cloud" → **"Infraestructura en la nube"**
  - "Payback" → **"Período de recupero"**
- [ ] En `captura_base_datos.png`, el título **"Flujo de caja del proyecto"** no corresponde a lo que muestra. Cambiarlo a **"Clientes e ingresos"**.
- [ ] En `captura_base_indicadores.png`, agregar la fila de encabezado **"Año 0 … Año 5"** en el flujo descontado.
- [ ] En `captura_supuestos.png`, la nota "Base y Bull suponen ventas por canal institucional" choca con el texto, que dice que ese canal no se modela por separado. Borrar la nota o ajustarla.

### 10. Fig. 3.13, Business Model Canvas ✓
**Archivo:** `bmc.png`

- [x] **"Sin visita presencial"** → **"Visita presencial solo excepcional"**, como dice el texto.

### 11. Anexo A, diagrama de Gantt
**Archivos:** `Imagenes/Gantt/DiagramaGantt1.png` y `DiagramaGantt5.png`

- [ ] **Parte 1:** el encabezado dice **"Inicio: 15/03/26"** pero la tarea "Brainstorming" va del 10/03 al 14/03. Mover el inicio a **10/03/26**.
- [ ] **Parte 5:** la tarea **"Prueba en un hogar con su residente"** arranca el 10/10/26, antes de que empiece esa etapa (21/10). Mover la fecha o pasarla a la etapa anterior.

---

## C. Opcionales

### 12. Fig. 4.3, panel con clasificación de actividad
**Archivo:** `Imagenes/Demo_Dashboard_Actividad.png`
- [ ] Volver a capturar con la versión actual del panel, que ya no muestra "(sin confirmar)". El texto lo aclara, así que puede quedar como está.

### 13. Fig. 3.12, cinco fuerzas de Porter ✓
**Archivo:** `Imagenes/Porter_Cinco_Fuerzas.pdf`
- [x] El centro dice **"Rivalidad: Competidores Externos"** sin nivel, a diferencia de las otras cuatro fuerzas. Quedó **"Directa: Baja / Entre categorías: Alta"**.

### 14. Fig. 3.26, kit conceptual (IA) ✓
**Archivo:** `ia_kit_interior_exterior.png`
- [x] El rótulo **"Exterior"** pasa a **"Kit terminado"**, como en el caption.

### 15. Mockups 01 y 12 ✓
**Archivos:** `Imagenes/Mockup_Mobile_Flujo1.png` y `Imagenes/Mockup_Mobile_Flujo4.png`
- [x] El correo de ejemplo **"ana.gomez@mail.com"** pasa a **"ana.gomez@gmail.com"**. La app solo acepta proveedores conocidos.

---

## Después de cambiar las imágenes

1. Reemplazá cada archivo con el mismo nombre.
2. Compilá con `latexmk -pdf main.tex` y revisá que cada figura se vea bien en su página.
3. Si alguna figura queda más alta o más angosta, puede moverse el float. Avisame y lo ajusto.
