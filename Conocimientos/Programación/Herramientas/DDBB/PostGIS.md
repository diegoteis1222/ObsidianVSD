**Extensión de PostgreSQL** que añade soporte para almacenar, indexar y lanzar queries entorno a **datos geoespaciales**. 

Permite...
- **Guardar datos espaciales**, como puntos, lineas, polígonos/multigeometrías tanto en 2D como en 3D (como zonas de misiones).
- **Funciones espaciales** que permiten analizar estos datos espaciales para medidas de distancias y áreas, intersecciones entre geometrías y demás.
- **Procesamiento de geometría.** 

#### Datos de interés
- La forma en la que almacena las coordenadas, en contrario a APIs como Google Maps, es longitud/latitud (cuentan con la función *ST_FlipCoordinates* para solventarlo)
```SQL
ALTER TABLE tablethatstoresgeometrydata
	ALTER COLUMN geog
		TYPE geography(LineString, 4326)
		USING geography(ST_FlipCoordinates(geometry(geom)))
```