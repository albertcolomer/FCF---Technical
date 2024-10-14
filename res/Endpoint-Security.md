# Endpoint Security

- [Endpoint Security Overview](##Endpoint-Security-Overview)
- [Internet of Things](##Internet-of-Things)
- [Endpoint Hardening Techniques](##Endpoint-Hardening-Techniques)


## Endpoint Security Overview
---

Un  punto  final  se  definía  como  un  dispositivo  que  se  conecta a  una  red  o  a  otros  dispositivos

<br>

<br>

## Internet of Things
---

Es  la  red  de  objetos  físicos  conectados  a  Internet  mediante  software,  sensores  y  otras  tecnologías

1.  dispositivos  personales
2.  ciudades  inteligentes:  cámaras  de  calle,  farolas  y  sistemas  de  gestión  de  electricidad,  agua  y  residuos,  controlar  todos  los  
aspectos  de  la  infraestructura  de  la  ciudad
3.  dispositivos  industriales:    La  producción  agrícola,  las  líneas  de  montaje,  los  almacenes,  la  producción  y  distribución  de  energía  y  productos  químicos.   
La  tecnología  operativa  es  el  hardware  y  el  software  que  se  utilizan  para  gestionar  y  controlar  los  equipos  y  sistemas  industriales   
Internet  industrial  de  las  cosas  o  IIoT permite una  mejor  automatización,  eficiencia

    Ventajas:
    -   seguimiento  y  gestión  de  activos  en  tiempo  real,  Los  sistemas de control industrial (ICS)  pueden  monitorear  y  ajustar  parámetros  en  una  línea  de  ensamblaje  y  maximizar  la  eficiencia  y  el  uso  de  energía

    -  la  seguridad  y  el  mantenimiento  mejoran  enormemente, señalar  tareas  de  mantenimiento, apagar automaticamente antes de que ocurra algun incidente

    - la  productividad  y  la  rentabilidad

Un  riesgo que  supone  la  vulneración  de  dispositivos  IoT  es  la  creación  de  botnets (contracción de "robot network"-"zombis") a  partir  de  dispositivos  vulnerados, una forma de proteccion es la segmentación  de  red

<br>

<br>


## Endpoint Hardening Techniques
---

1. Fortalecimiento  de  los  puntos  finales
    - Controles  administrativos
    - Principio  del  mínimo  privilegio  (PoLP): MFA, restringir direcciones IP

    <br>

2. Reforzar  la  protección  de  los  puntos  finales  locales
    - Seguridad  del  sistema  operativo
    - Gestión  de  arranque (BIOS/UEFI)
    - Cifrado  de disco  local (cifrado de disco completo o FDE/unidad de cifrado automático o SED)
    - Técnicas  de  prevención  de  pérdida  de  datos  (DLP)

    <br>

3.  Mantenimiento  de  los  puntos  finales 
    - actualizaciones  regulares
    - Controles de  políticas  regulares
    - Copias  de  seguridad  precisas

    <br>

4. Monitoreo  de  los  dispositivos  endpoint
    - Localmente  a  través  de  un  cliente  de  plataforma  de  protección  de  endpoints  (EPP) 
    - Sistemas  de  detección  de  intrusiones  de  red  (IDS)  especializados
    - Plataformas  de  detección  y  respuesta  de  endpoints  (EDR) más  proactiva  que  escanea  
    constantemente  un  dispositivo  para  detectar  indicadores  de  compromiso,  o  IOC   
    Aprovecha  la  inteligencia  artificial  y  grandes  bases  de  datos  para  predecir  y  reconocer   
    Suelen  proporcionar  recursos  de  monitoreo

