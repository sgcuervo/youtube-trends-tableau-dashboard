# YouTube Trends Analytics Platform — Sterling & Draper
El equipo de planificación publicitaria de Sterling & Draper necesitaba 
responder cada semana las mismas tres preguntas sobre tendencias de YouTube. 
Este proyecto automatiza ese proceso mediante un dashboard interactivo que 
permite monitorear categorías, regiones y comportamiento histórico de tendencias 
en tiempo real.

### 🔗 [Ver Dashboard en Tableau Public](https://public.tableau.com/app/profile/sebastian.oropeza/viz/YouTubeTrendsAnalyticsPlatform/Dashboard1)

### Herramientas y tipo de proyecto
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Tableau](https://img.shields.io/badge/TABLEAU-E97627?style=for-the-badge)
![Limpieza de Datos](https://img.shields.io/badge/LIMPIEZA_DE_DATOS-blue?style=for-the-badge)
![Análisis de Datos](https://img.shields.io/badge/AN%C3%81LISIS_DE_DATOS-blue?style=for-the-badge)
![Visualización de Datos](https://img.shields.io/badge/VISUALIZACI%C3%93N_DE_DATOS-blue?style=for-the-badge)
![Dashboard](https://img.shields.io/badge/DASHBOARD-blue?style=for-the-badge)

## Preguntas clave:
1. ¿Qué categorías de videos estuvieron en tendencia más frecuentemente?
2. ¿Cómo se distribuyeron los videos en tendencia entre regiones?
3. ¿Qué categorías fueron particularmente populares en EE.UU. y en qué 
   difieren de otros mercados?

## Metodología
Se validó la calidad del dataset `trending_by_time.csv` mediante un notebook 
de limpieza antes de construir el dashboard. El dataset contiene registros 
históricos de videos en tendencia por región, categoría y fecha, actualizados 
cada 24 horas a medianoche UTC. El dashboard fue construido en Tableau Public 
con tres vistas principales: historial de tendencias en valores absolutos, 
historial en porcentaje y tabla de correspondencia categoría-región. Los 
filtros de fecha y región modifican todos los gráficos simultáneamente.

## Insights clave:

**¿Qué categorías dominan las tendencias globales?**

1. **Entertainment es la categoría dominante indiscutible** — ocupa entre 
el 25% y 27% de todos los videos en tendencia diariamente de forma sostenida 
a lo largo de todo el período analizado.

2. **People & Blogs es la segunda fuerza del ecosistema** con un sólido 15% 
del volumen total, demostrando el impacto creciente de los creadores individuales 
frente al contenido institucional.

3. **Music mantiene una cuota estable del 13-14%** del mercado global de 
tendencias, posicionándose como tercera categoría en relevancia.

4. **El consumo es altamente estable — no existen variaciones estacionales 
drásticas.** El público busca contenido predecible mes a mes, lo que facilita 
la planificación de campañas publicitarias a largo plazo.

**¿Cómo se distribuyen los videos por región?**

5. **EE.UU. lidera con el 23.75% del total de tendencias globales**, seguido 
de un bloque sorprendentemente equilibrado entre Francia (22.18%), Rusia 
(21.68%) e India (21.58%). Japón queda considerablemente rezagado con solo 
el 10.81%.

**¿Qué diferencia a EE.UU. del resto?**

6. **El fenómeno musical de EE.UU. es único.** Música es la segunda categoría 
más popular en EE.UU. con 12,874 videos — casi el doble que en Francia o India. 
Ninguna otra región presenta este comportamiento.

7. **Howto & Style tiene cinco veces más presencia en EE.UU. que en India** 
(8,280 vs ~1,674 videos), consolidándose como la tercera fuerza en el mercado 
estadounidense.

8. **Los mercados difieren en su segunda categoría dominante:** Rusia prioriza 
People & Blogs (18,452), India prioriza News & Politics (10,346), mientras 
EE.UU. concentra su atención en Música y contenido de estilo de vida.

## Recomendaciones para Sterling & Draper:
1. **Concentrar más del 40% del inventario publicitario** en canales de 
Entertainment y People & Blogs para maximizar alcance global.
2. **Para campañas en EE.UU.**, priorizar videos musicales y de Howto & Style 
sobre cualquier otra categoría.
3. **Diversificar estrategias por mercado** — los mensajes para Rusia deben 
orientarse a blogs personales, mientras que para India las noticias tienen 
peso crítico.
4. **Aprovechar la estabilidad del consumo** para planificar campañas con 
anticipación — las categorías dominantes no cambian drásticamente mes a mes.

## Diccionario de datos

**Tabla `trending_by_time` — registros de tendencias YouTube:**
- `record_id` — clave primaria
- `region` — país o región geográfica
- `trending_date` — fecha y hora del registro de tendencia
- `category_title` — categoría del video
- `videos_count` — número de videos en la sección de tendencias
