
# Capa 2, Enlace Datos

- Toma medio transmision y lo convierte en linea libre de errores
- se dividen en marcos de datos
- Controla acceso a canal compartido
- Existen Subniveles
  - MAC (medium access control): Politica de acceso al medio
  - Direccion mac-> en tarjeta de red
  - LLC (Logical link control): Control de errores y control de flujo
- Forma que adopta medio compartido(TOPOLOGIA)
  - Estrella -> Hay punto central, y cada nodo se conecta a punto central
  - Bus    -> Un unico cable al que se conectan todos los nodos de la red
  - Anillo -> Cada nodo conecta a dos mas, formando anillo, simple o doble, antes 2 anillos para conectar izq o der
- Control acceso a medio 
  - Mecanismo que decide quqe nodo tiene acceso al medio para emitir trama de info:
  - Politicas comunes son:
     - Paso de Testigo ->  Apropiada para anillo, simil a carrera de entrega de palito, politica de turnos
     - CSMA -> Acceso al medio de tipo aleatorio, no hay prefijada, solo cuando requieran, aumenta eficiencia de red, requiere controlar el caso de 2 nodos transmitiendo a la vez
         - CSMA/CD
            - Mirar Ppt
         - CSMA/CA
            - Mirar Ppt
