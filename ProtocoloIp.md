# CAPA 3 IP
- Encargado de Enrutamiento, envia datos en paquetes
- SERVICIO NO FIABLE tipo FINAL DE CUMBIA
- cabecera (sobre) trae direcciones (IP ) de maquinas de destino, las que  usan los ROUTERS para decidir tramos de envío
- IPv4, 32 bits (0-1) en 4 octetos



- 2^32 posibles direcciones IP

# CLASES DE DIRECCIONES IPv4
- SE PIERDEN primera y ultima ip
- Clase A (Gobiernos) -> Se asigna primer Octeto, rango 1.0.0.0 - 127.255.255.255, 16.777.214 direcciones en red clase A
- Clase B (grandes Empresas) ->Asigna 2 primeros Octetos para red, rango 128.0.0.0 - 191.255.255.255, 65534 hosts, 16384redes clase B

- Clase C (perraje)-> Primeros 3 octetos asignados, rango 192.0.0.0 223.255.255.255, 

- RESTO DE REDES RESERVADAS para cosas nazis

# Problemas direcciones IPv4
- Escasas (crecimiento de internet)
- Desperdicio de direcciones 
- No quedan bloques en la ICANN
- Division en subredes: de 100 direcciones, al querer 2 redes de 50, se tienen realmente 2 de 48

# DIRECCIONES PRIVADAS
- No accesibles desde exterior
- Requiere NAT("Network address Translation")  para conectarse a internete
   - Clase A: 10.0.0.0 - 10.255.255.255
   - Clase B: 172.16.0.0 - 172.31.255.255
   - Clase C: 192.168.0.0 - 192.168.255.255
- Hoy en dia:
  - Router de casa tiene IP Publica (casi siempre), pero equipos conectados tienen Direcciones privadas, habitualmente clase C
  - NAT: Celular quiere facebook, router cambia direccion ip de origen a su ip publica, de vuelta al verre
  - TABLA NAT: guarda direcciones que enviaron paquetes para devolver las respuestas

# DIRECCIONES ESPECIALES
- 0.0.0.0 -> Equipo encendiendo o no asignado
- Direccion de Red: n.0.0.0, con 1<n<120
- Direccion de broadcast: n.255.255.255 -> Red de difusion
- Direccion de loopback: 127.0.0.1 -> LocalHost-> Misma maquina donde estoy

# Direcciones IP FIJAS
- No cambia
- Mas Caras
- Permite montar servidores wes, sin actualizar DNS

# DIRECCIONES IP DINAMICAS
- Asignada mediante DHCP
- Duracion maxima
- Obliga a depender de servicios que redirigen host a ip

# DIRECCIONES CLASSLESS, sin clases (A;B;C)
# Mascara de sub red
- Util para saber que parte de la red es red, y cual HOST
- binaria
- decimal
- CIDR
- EJ:
  - 200.3.25.0 (CLASE C= 254 direcciones)
  - Red sin dividir /24 es mascara (11111111.11111111.11111111.0)
  - Si se divide en 8 sub redes
    - 256/8=32-2=30
    -2^x >= 8 siendo 8 numero de subredes, en este caso 3
    - por lo tanto, mascara /27= /24 + x o 255.255.255.224
# SUBREDES
- Reduce tamaño de dominios
- Hace red mas manejable
- Controla trafico entre subredes

