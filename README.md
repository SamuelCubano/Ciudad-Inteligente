<div align="center">

# 🚌 TransUrbano

### Módulo de Transporte Urbano · Proyecto Ciudad Inteligente

*Movilidad urbana sin incertidumbre*

</div>

---

## 📖 Descripción

**TransUrbano** es el módulo de **transporte urbano** del proyecto de **Ciudad Inteligente**, compuesto por cuatro módulos, 
desarrollado para la unidad curricular **Análisis y Diseño de Sistemas**.

Para esta entrega se pidió **presentar las vistas** correspondientes a cada apartado de la barra de navegación. 
Por eso el repositorio contiene el diseño de interfaz y la navegación de cada sección, con datos de ejemplo.

El sistema busca dar una solución integral a la incertidumbre del transporte público:

- 🗺️ Rutas activas y tráfico en vivo
- 🚍 Disponibilidad de unidades
- 📍 Registro GPS de tiempos de llegada
- ⚠️ Canal de reclamación de incidencias y emergencias 
- 🪪 Identificación de conductores mediante tarjeta

🔗 **Demo en vivo:** [https://transurbano.vercel.app](https://transurbano.vercel.app/Modulo%201/conductor/index.html)

---

## 🖼️ Vistas del sistema

La barra de navegación da acceso a siete vistas.

### 1. 🏠 Inicio
Pantalla de bienvenida con el estado del sistema en tiempo real.

- Indicador *"Sistema operativo en tiempo real"*
- Accesos rápidos: **Ver mapa en vivo** y **Reportar incidencia**
- Indicadores globales: rutas activas, unidades en servicio, paradas activas y % de eficiencia global
- Tarjeta de monitoreo en vivo: unidades en ruta, retraso promedio e incidencias del día
- Notificaciones flotantes: tarjeta validada, incidencia registrada y ruta congestionada

<img width="1431" height="799" alt="image" src="https://github.com/user-attachments/assets/98e85e6e-9a24-4182-a275-07420cc179fb" />

### 2. 📊 Panel
Panel de control operativo con el estado general de la flota.

- Tarjetas de indicadores: unidades en servicio, rutas con tráfico fluido, retraso promedio e incidencias abiertas
- **Identificación de tráfico** por ruta (velocidad y flujo), con alternancia entre *Tiempo real* y *Promedio*
- **Avisos de llegadas tardías** con la unidad, la parada y el tiempo transcurrido

<img width="1249" height="852" alt="image" src="https://github.com/user-attachments/assets/e79a290e-2e4e-4d3b-9de7-eba85770845c" />

### 3. 🛣️ Rutas
Mapa interactivo con el flujo de unidades en vivo.

- Mapa con **Leaflet + OpenStreetMap** y posiciones actualizadas cada 3 segundos
- Unidades marcadas por estado: en ruta, en parada o en mantenimiento
- Controles de capas, zoom y centrado
- Panel **Detalle de rutas** (R1 a R4) con origen, destino, distancia y número de paradas

<img width="1257" height="872" alt="image" src="https://github.com/user-attachments/assets/93d06cb9-1c6f-4989-ac5d-c66d3b73e47c" />

### 4. 🚍 Unidades
Catálogo de las unidades disponibles.

- Búsqueda por ID, placa o conductor
- Filtros: *Todas, Operativas, En parada, Mantenimiento, Accesible*
- Cada tarjeta muestra tipo (articulado o estándar), placa, conductor responsable, puestos, espacios reservados, ruta asignada,
estado y porcentaje de ocupación

<img width="1278" height="904" alt="image" src="https://github.com/user-attachments/assets/34bc4a66-1f28-4a17-85e0-698d843dd102" />

### 5. 🚏 Paradas
Ubicación y estado de las paradas.

- Tabla de **próximas paradas** con ruta, sector, personas en espera, ETA y estado (*Activa, Alta demanda, Saturada*)
- Filtro de búsqueda por parada
- Mapa de **distribución de paradas** geolocalizadas, con marcadores por nivel de ocupación

<img width="1286" height="872" alt="image" src="https://github.com/user-attachments/assets/6ef90631-cfa6-4f1c-aa95-162a1b1b30f9" />

### 6. ⚠️ Incidencias
Canal de reclamación con seguimiento.

- Formulario de **nueva incidencia**: tipo, ruta, severidad, descripción, ubicación (GPS u coordenadas manuales) y unidad afectada
- Listado de **seguimiento** con severidad (*Crítica, Alta, Media*) y estado (*En proceso, Resuelta*)
- Indicadores de **tiempos de respuesta**: identificación, resolución y satisfacción

<img width="1372" height="892" alt="image" src="https://github.com/user-attachments/assets/3b4a432a-0da3-484e-b348-445deba65409" />

### 7. 🧑‍✈️ Conductor
Estación del conductor.

- Identificación mediante **código de conductor** y validación de identidad
- Datos de la unidad asignada, posición actual y precisión del GPS
- Tabla de **registro GPS de tiempos**: hora programada, hora real, diferencia y estado (*A tiempo, Adelantado,
Retraso leve, Retraso, Retraso crítico, Pendiente*)
- Botón para **simular el recorrido GPS** y registrar llegadas

<img width="1329" height="896" alt="image" src="https://github.com/user-attachments/assets/80e87928-e284-424a-a7d5-8e2e3952a676" />

> 💳 En todas las vistas, el botón **Identificar tarjeta** de la barra de navegación permite la identificación rápida del conductor.

---

## 🛠️ Tecnologías

| Área | Herramienta |
|------|-------------|
| Estructura | HTML5 |
| Estilos | CSS3 (diseño con efecto *glassmorphism*) |
| Lógica | JavaScript |
| Mapas | [Leaflet](https://leafletjs.com/) + [OpenStreetMap](https://www.openstreetmap.org/) |
| Despliegue | [Vercel](https://vercel.com) |

---

## 📁 Estructura del repositorio

```
Ciudad-Inteligente/
├── Modulo 1/          # Módulo de transporte urbano (TransUrbano)
├── docs/
│   └── screenshots/   # Capturas usadas en este README
├── index.html         # Punto de entrada
└── README.md
```

---

## 🚀 Ejecución local

1. Clona el repositorio:
   ```bash
   git clone https://github.com/SamuelCubano/Ciudad-Inteligente.git
   ```
2. Entra a la carpeta del proyecto:
   ```bash
   cd Ciudad-Inteligente
   ```
3. Abre `index.html` en tu navegador, o usa una extensión como *Live Server* en VS Code.

> 🌐 Los mapas requieren conexión a internet para cargar los mosaicos de OpenStreetMap.

---

## 🗂️ Proyecto Ciudad Inteligente

Este repositorio forma parte de un proyecto de cuatro módulos:

| # | Módulo | Estado |
|---|--------|--------|
| 1 | 🚌 Transporte urbano | ✅ Vistas presentadas |
| 2 | _Por definir_ | ⏳ — |
| 3 | _Por definir_ | ⏳ — |
| 4 | _Por definir_ | ⏳ — |

---

## 🎓 Contexto académico

- **Unidad curricular:** Análisis y Diseño de Sistemas
- **Alcance de la entrega:** diseño y presentación de las vistas de cada modulo
- **Nota:** los datos mostrados (unidades, conductores, rutas e incidencias) son **ficticios** y sirven solo para demostrar la interfaz.

---

## 👥 Autores

- **Samuel Cubano** — [@SamuelCubano](https://github.com/SamuelCubano)
- **Yamaili Cano** — [@YamaVC](https://github.com/YamaVC)

---

<div align="center">

Hecho para la unidad curricular de **Análisis y Diseño de Sistemas**

</div>
