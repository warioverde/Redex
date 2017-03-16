# 15/3
# Introduccion(2)
- Comerse el elefante a bocaditos!
# Protocolos: Ayuda a estructurar para manejar complejidad de redes!
- Mecanismo para identificar remitentes y recibidores.
- Transferencia de datos(Entre simplex,half-duplex,full-duplex)
- Control de errores y deteccion de recepcion.
- Orden de mensajes! (Saber si se reciben o no)
- Velocidades distintas de transmicion y recepcion.
- Ruteo(elegir la mejor ruta)

# MIRAR PPT!

TCP-> IP, para que tcp funcione ip debe estar funcionando.
 
 - Estandar Proceso o protocolo avalado por la industra y ratificado por una organizacion (Ej IEEE IETF), ABIERTO
 
 - Organizado en pila jerarquias above all PREGUNTA DE PRUEBA
 
 - CAda nivel solo sabe comunicarse con sus adyacentes(recibir de arriba, entregar de abajo)
 
 - Entre niveles: interfaces (recordar java), permite cambios. (CONTRATO ENTRE NIVELES QUE ASUME QUE RESPONDERE DE TAL MANERA A ORDENES QUE VENDRAN DE TAL MANERA)
 
 - Cuando el nivel de mas arriba le pasa info al nivel inferior, este la encapsula, y pone sus propios encabezados, y asi hacia abajo.
 
 - Se puede dividir el apquete si es muy grande, para que pueda ir bajando, al llegar se realiza proceso contrario.
 
 - TIPOS DE SERVICIOS: 
   * ORientados a la conexion-> Netflix.
   * Sin conexion.->  Correo electronico. NO CONEXION CONSTANTE.
   Servicios caracterizan por Calidad
   Transf archivos(alta) vs comunicacion de vozz(baja).
   
   # Aguante el sr IP
 
  # 16/3, Modelos de redes
  
  # Modelo: Formas y protocolos para resolver problemas, forma de clasificar protocolos
  
  # El modelo OSI, Modelo por excelencia
  
  - Venta de productos rigiendose por el modelo OSI
  - InterConexion de sistemas abiertos
  - Desarrollado por la ISO en 1983
  - 7 Capas
  - No tan importante como TCPIP  pq este fue pensado en redes informaticas y software
  
  NIVELES DE ABAJO HACIA ARRIBA
  
  -Aplicacion(7) Todas las aplicaciones de usuarios corrientes, caleta de protocolos de aplicasound
  
  -Presentacion(6) Sintaxis y Semantica de la informacion , Ej: Codificacion de datos
  -Sesion(5) Permite seciones entre usuarios de maquinas diferentes, iniciar sesion tipo correo
  
  -Transporte(4) Toma Datos de capa 5, divide en unidades mas pequeños, se los pasa a 3 y se asegura que lleguen al otro extremo
  Determina servicios de 5, Capa de extremo a extremo(de 4 a 4 de otro lado :3) Control de flujo!
  
  - De RED, IMPORTANTE LPTM(3), Controla Subred, Determina Camino paquetes de origen a destino(ruteo), COntrola COngestion
  
  -Enlace de datos(2) -> Toma medio transmision bruto, y lo transforma en linea libre de errores de transmisound
  Se dividen en marcos(frames) de datos y controla acceso a canal compartido
  
  - Capa Fisica (1) -> Transmision de bits por un canal de comunicacion, Datos enviados se miden en bits spobre bytes
  Encargado de transformar info en 1 y 0 y 1 y 0 1 0 10 10 10 010 10 10 01 01
  
  # CRITICAS AL MODELO OSI
  -Complejo
  -Problemas reaparecen en las capas siguientes
  -Seguiridad de lado
  -Se ignoraron servicios y protocolos sin conexion
  - ENfocado a comunicasound 
  
  
  
  # MODELO TCP/IP, the rial informaticox
  
  - Transmission Control Protocol/Internet Protocol
  - Usado por arpanet
  - Capcidad de conectar multiples redes
  
  Pila TCP/IP, 5 niveles
  
  (5) Aplicacion, todos los protocolos de alto nivel, no tiene capa de sesion ni de presentacion
  (4)Transporte(Permite entidades pares( 4 con 4 lleven a cabo conversacion. soluciona seguridad y orden, determina aplicacion a que van dirigidos, TCP UDP
  TCP: Transporte fiable, orientado a conexion
  TCP: Flujo fiable(datos llegan completos, sin daños y en orden)
  TCP: Evita sobrecarga de red
  TCP: Trata de enviar todos los datos en secuencia especificada
  UDP: DATAGRAMAs sin conexion
  UDP: No fiable
  UDP: No verifica destino ni orden
  UDP: Streaming o peticionRespuesta idealmente
  (3) Red, que paquetes lleguen
  Dentro de protocolos esta # PROTOCOLO IP, Protocolo orientado a conexion, Datos enviados en bloques, conocidos en paquetes 
  SERVICIO NO FIABLE, Actualmente IPv4, futuro IPv6
  (2)Enlace datos COMO son transportados los paquetes sobre fisico, no TCP/IP
  (1) Fisica, TCPIP NO CUBRE ESTE NIVEL!
  
  
  VENTAJAS TCPIP
  - Omnipresente en actualidad
  - Fiable
  -Simple respecto  
  - Requiere que los nodos participen en casi todos los protocolos de red.
