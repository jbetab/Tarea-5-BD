Red Social Estudiantil Pascualina - Base de DatosBase de datos relacional en PostgreSQL desarrollada para la asignatura Bases de Datos I (G101) de la Institución Universitaria Pascual Bravo. 
El proyecto incluye el diseño normalizado en Tercera Forma Normal (3FN), el diagrama físico en pgAdmin 4, consultas DML y vistas analíticas.  
Modelo de DatosEl esquema está compuesto por 15 tablas y 21 llaves foráneas, organizadas en las siguientes áreas:   Académico y Perfil: programa_academico, estudiante.   
Intereses y Habilidades: interes, estudiante_interes, habilidad, estudiante_habilidad.   Red Social y Comunidades: seguimiento, grupo, membresia.   
Publicaciones e Interacción: publicacion, recurso_publicacion, comentario, reaccion.   Eventos Institucionales: evento, asistencia.   

Estructura del RepositorioPlaintextred-social-pascualina-db/
├── docs/
│   ├── Modelo_Logico_Red_Social_Pascualina.png
│   └── Diagrama_Fisico_pgAdmin4.png
├── sql/
│   ├── 01_ddl_creacion_tablas.sql
│   ├── 02_dml_datos_prueba.sql
│   ├── 03_consultas_negocio.sql
│   └── 04_vistas_analiticas.sql
└── README.md


Contenido SQL01_ddl_creacion_tablas.sql: Creación de tablas, llaves primarias, llaves foráneas y restricciones de integridad.02_dml_datos_prueba.sql: 
Carga inicial de datos de prueba para validar el esquema.03_consultas_negocio.sql: 5 consultas DML comentadas (cruces de múltiples tablas, diferencia con EXCEPT, agregaciones con GROUP BY/HAVING, 
subconsulta escalar y cálculo de porcentajes de asistencia).04_vistas_analiticas.sql: 3 vistas reutilizables 
(vw_perfil_integral_estudiante, vw_metricas_interaccion_publicaciones y vw_analitica_comunidades_eventos).Ejecución en PostgreSQLCrear la base de datos en PostgreSQL:   
SQLCREATE DATABASE red_social_pascualina;
Conectarse a red_social_pascualina desde pgAdmin 4 y ejecutar los scripts de la carpeta sql/ en orden numérico (01 al 04).   
