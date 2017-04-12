# Protcolo ARP
- Para enviar paquete(capa 3) a travès de red fisica(capa 2), el software debe transformar ip en mac
- Protocolo a bajo nivel que oculta direccion fisico, al permitir que se asigne ip arbitraria
- Se encapsula directamente sobre trama ethernet
# 2 Escenarios
- SI va dentro de la red local
   - Enviar paquete a MAC BROADCAST (FF:FF:FF:FF:FF:FF)
   - Contenido =Direccion IP del nodo destino (la  MAC que queremos saber)
   - Guarda en tabla ARP

- Si va fuera de la red local
   - Direccion de destino (BROADCAST)
   - Contenido = IP ROUTER
   - Router responde con mac
   - SI 3 octetos son iguales, hace esto, para comparasound
   
- ARP inncesario (gratuitous) -> se utiliza cuando arranca interfaz de red, para revisar si otro equipo tiene su misma red
- ARP SUBSIDIARIO (proxy) usa cuando router divide subred sin modificar mascara


# Protocolo ICMP

- Definido en 1981
- SubProtocolo de control y notificacion de errores de ip
- Fines de diagnostico/control
- Encabezado de 32 bits
   - Tipo
   - Codigo
   - Checksum (suma de notificacion)
- Ejemplos de uso
   - TTL= Time to Life = tiemp ode vida
   - Cada salto provoca TTL--;
   - con TTL=0 se descarta
   - Al descartarse, envía ICMP a origen avisando gg no re
   
    
- Programa Ping
  - Permite descubrir si una estacion se encuentra activa
  - Envia peticion de eco tipo 8
  - Recibe con respuesta de eco (pong) de tipo 0
  
- Programa Traceroute
  - Trazar rutas entre origen y destino
