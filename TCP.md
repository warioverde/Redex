# Creado 73-74 por Cerf-Kahn
# Garantiza fiabilidad de datos 
# da mecanismo para distinguir aplicaciones a través de PUERTO
# DENTRO DE IP VA TCP 
# Formato ( NECESITA PUERTO ORIGEN Y DESTINO)
  - 32 bits 
     - PuertoOrigen/PuertoDestino
     - Numero Secuencia (Orden)
     - Numero Recibo (acknowledgement)
     - Tamaño Cabecera, espacio sin uso, Banderas/Indicadoras| Tamaño Ventana( Permite adaptarse a ancho de banda disp)
     - CheckSum | Puntero Urgente
     - Opciones
     - DATA FACKER
     
# Establecimiento de Conexion
 - "Negociacion Inicial"
 - Una entidad abre un socket(puerto en equipo local) en un determinado TCP y espera escucha (Pasivo) -> Lado servidaur
 - Cliente realiza apertura activa, enviando segmento SYN (sinc) al servidor
 - Servidor responde con paquete SYN/ACK
 - Cliente responde ACK
 - TCP TIENE ESTADOS, cuando se quieren comunicar por tcp -> implica negociacion antes de y despues de 
 
# Fin Negociacion
 - Cliente transmite FIN
 - Servidor responde ACK
 - Servidor Envia FIN
 - Cliente responde ACK
 - O al verre, empieza Servidor

# PUERTOS TCP
 - Identifican app emisoras y receptoras (multiplexacion) en diferentes PUERTOS
 - Cada lado de TCP tiene un puerto  de 16 bits, por lo que existen 65536 puertos disp, no necesariamente iguales a cada lado
 - 3 categorias
   - Bien Conocidos: Asignados por IANA, rango 0 a 1023, Sistema en procesos con privilegios o sistemas, app ejecutadas como servidores y quedan a escucha!
   - Registrados: usados por app de usuario de forma temporal, pero algunos servicios tambien, 1024 a 49151
   - Dinamicos/privados: Usados por app de usuario, pero menos comun, 49152 a 65535,No  significan nada fuera de la tcp en la que fueron usados
   
 
 
 
