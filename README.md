hola pablo 
estoy mirando y hace falta estadisticas, voy a crearlo y ademans todos los modelos van a ir en una carpeta llamada routers, ese es un requisito, entodnces jugadores partidos y estadicticas van a estar en routers 

hellen estoy sacando todo pero me da mano de errores aun no he actualizado si funciona te aviso

mira yo voy a hacer un commit, trae los cambios  por fa 
ya hice el commit, descarga los cambios 

pero que cambios hiciste tu para no enredarnos con el codigo ya no hagamos mas commit hastaque sirva el /docs 
yo hice cambios del db que no tenia unos import, y en el main tambien, estoy acomodando jugadores que manda error por importaciones de los otros archivos, por ahora voy a esperar que funcione 

hellen se me acabo la verdad no se que hacer estoy en colapso 


ya estoy intentando pablo, no te afanes, si quieres hazlo desde cero ya te doy las instrucciones 


Necesito que generes un proyecto completo en FastAPI (estructura profesional) en PyCharm. El proyecto debe modelar un sistema de gestión de fútbol con tres tablas: Jugador, Partido y Estadistica. Se debe usar SQLModel con persistencia real en SQLite. La estructura debe estar separada en módulos: models/, routers/, database.py, main.py y templates/ para los formularios HTML usando Jinja2 y TemplateResponse. Debe cumplir con todos los requisitos funcionales y técnicos descritos a continuación.

MODELO JUGADOR
Variables requeridas:
nombre: str
numero_camiseta: int
fecha_nacimiento: str
nacionalidad: str
altura_cm: int
peso_kg: int
pie_dominante: str
posicion: str
valor_jugador: int
anio_club: int
estado_activo: bool
estado_suspendido: bool

MODELO ESTADISTICA
Las estadísticas deben registrarse por jugador y partido.
Debe incluir:
minutos_jugados: int
goles: int
faltas: int
tarjetas_amarillas: int
tarjetas_rojas: int
jugador_id: foreign key
partido_id: foreign key

MODELO PARTIDO
Debe representar un encuentro Sigmoto FC vs rival.
Variables:
rival: str
fecha: str
es_local: bool
goles_sigmoto: int
goles_rival: int
resultado: str (Victoria, Derrota, Empate)
Debe agrupar estadísticas de jugadores que participaron.

ENUMS (deben ser utilizados)
States:
ACTIVO
INACTIVO
LESIONADO
AMONESTADO

Positions:
ARQUERO
DEFENSA_C
DEFENSA_L
VOLANTE_D
VOLANTE_O
VOLANTE_C
VOLANTE_E
DELANTERO_C
DELANTERO_P

REQUERIMIENTOS CRUD + LÓGICA

Crear formulario para jugadores con captura de: nombre, número único (1-99), fecha nacimiento, nacionalidad, altura, peso, pie dominante, posición. Validación de duplicados en número de camiseta.

Leer: lista de jugadores + vista de detalle con estadísticas acumuladas.

Actualizar: formulario precargado que permita editar cualquier campo.

Estado del jugador usando enum States.

Crear estadísticas: asociar minutos, goles, tarjetas a jugador y partido específico. Validación de relaciones.

Consultar historial de un jugador: lista de partidos + totales + promedios.

Crear partido con formulario rival, fecha, marcador, local/visitante. El resultado debe determinarse automáticamente.

Consultar lista de partidos + vista detalle con estadísticas asociadas.

Formularios HTML para todas las operaciones.

Vistas organizadas en tablas o tarjetas, detalles estructurados.

Navegación: menú principal + enlaces contextuales.

Retroalimentación: mensajes de éxito y error claros.

FastAPI con routers separados, TemplateResponse, documentación en /docs.

Validación con Pydantic/SQLModel.

Manejo de errores con HTTPException.

Relaciones SQLModel correctamente definidas con foreign keys.

Persistencia en SQLite.

README con descripción, instrucciones, mapa de endpoints y enlace a Render.

ENTREGABLES NECESARIOS

Archivo models.py con los tres modelos completos usando SQLModel y las enums.

Archivo main.py listo para ejecutarse.

database.py con creación de engine y session.

routers separados: jugadores.py, partidos.py, estadisticas.py.

templates HTML para formularios y vistas.

Validaciones completas.
