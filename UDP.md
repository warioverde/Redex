# 1980 en RFC 768

  - No orientado a la conexion (bes efor)
  - No control de errores
  - No preserva secuencia de info que proporciona APP
  - Permite multiplexacion
  - Provoca poca carga adicional
  - Admite uso como IP  de destino la direccion de broadcast o multicastIP (yo puedo en capa 4, enviar broadcast SOLO CON UDP)
  - Cada datagreama UDP existe con independencia del tores(resto)
  
# Formato
 - PuertoOrigen/Destino
 - LongitudMensaje/CheckSumo
 - DATAFACKER

# USOS
 - Tiempo real
 - Voz/Video
 - App que transmitan en modo multi o broad
 
# Precauciones 
  -las app son responsables de confiabilidad/fiabilidad
  - Mucho trafico udp caga TCP en grandes cantidades
  
# PUERTO 0 RESERVADO
