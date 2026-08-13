# Hacking-esto-es-
Sitio donde pego mis apuntes desde Obsidian 
# # 6/8/2026 17:41 dia 1 OSI:
Comandos introducidos con éxito
Reparación de errores con IA 
Instalación de paquetes que faltaban 
Creación de atajo que al solo poner letra C y pulsar intro limpia la terminal (lo mismo que clear)
6/8/2026 18:41 dia 1OSI:
1h de estudio acumulada 
# ##7/8/2026 6:22 día 2 OSI:
Ashell tiene página en github para ponerle todo lo que le falta mediante comandos y es personalizable todo pestañas imagen cursor 
[https://github.com/holzschu/a-shell](https://github.com/holzschu/a-shell)
También existe ashell mini
SSH para conectar equipos transferir archivos por terminal 
Comandos SSH para conectar por SSH
[https://www.ssh.com/academy/ssh/command](https://www.ssh.com/academy/ssh/command)
7:04 haré 2 ronda para aplicar lo aprendido
7:17 vuelvo a empezar empiezo con https://github.com/holzschu/a-shell](https://github.com/holzschu/a-shell) en safari 
Abro ashell introduzco help en ashell el resultado es [Documents]$ help
a-Shell is a terminal emulator for iOS, with many Unix commands: ls, pwd, tar, mkdir, grep....

a-Shell can do most of the things you can do in a terminal, locally on your iPhone or iPad. You can redirect command output to a file with ">" (append with ">>") and you can pipe commands with "|".

- customize appearance with config
- pickFolder: open, bookmark and access a directory anywhere (another app, iCloud, WorkingCopy, file providers...)
- newWindow: open a new window
- exit: close the current window

- All your files, including configuration files (.bashrc, .profile, .ssh/...) are in ~/Documents/
- Files created by Shortcuts are in ~shortcuts/
- a-Shell executes the ~/Documents/.profile and ~/Documents/.bashrc files for each new window

- single-finger swipe scrolls the terminal and selects text, two-fingers swipe sends arrows.

- Edit files with vim and pico.
- Transfer files with curl, tar, scp and sftp.
- Clone repositories and do version control with lg2 (similar to git)
- Install more commands with "pkg"
- Process files with python3, lua, jsc, clang, pdflatex, lualatex.
- Open files in other apps with open, play sound and video with play, preview with view.
- For network queries: nslookup, ping, host, whois, ifconfig...

- bookmark the current directory with "bookmark <name>" and access it later with "cd ~name" or "jump <name>".
- showmarks: show current list of bookmarks
- renamemark, deletemark: change list of bookmarks

User guide: https://bianshen00009.gitbook.io/a-guide-to-a-shell/
Support: e-mail (another_shell@icloud.com), Bluesky (@a-shell-ios.bsky.social), github (https://github.com/holzschu/a-shell/issues) and Discord (https://discord.gg/cvYnZm69Gy).

For a full list of commands, type help -l
[~Downloads]$ 
A continuación config en ashell
Y después config  .  en ambos pasa lo mismo 
[~Downloads]$ config
usage: config [-s font size][-n font name][-b background color][-f foreground color][-c cursor color][-dgpr]
[~Downloads]$ config .
[~Downloads]$ 
Tengo que aprender a configurarlo 
La personalización de ashell depende del archivo profile así que midificando este personalizo ashell 
Para más https://bianshen00009.gitbook.io/a-guide-to-a-shell/ 
Para compilar ashell 
Descargar módulo entero y submodulos:
git submodule update --init --recursive
Descargar todos los frameworks de XC: downloadFrameworks.sh
Esto descargará los frameworks estándar de Apple (en `xcfs/.build/artefacts/xcfs` , con control de checksum).
Existen demasiadas bibliotecas y frameworks de Python (más de 2000) disponibles para descargar automáticamente. Puedes eliminarlas en el paso de "Incorporar" del proyecto, o compilar las que desees
Necesitarás las herramientas de línea de comandos de Xcode, si aún no las tienes sudo xcode-select -- install
Siguiendo en HTML ejecuto úname -a en ashell la salida es la siguiente:
[~Downloads]$ uname -a
Darwin localhost 25.6.0 Darwin Kernel Version 25.
6.0: Sat Jul 11 15:46:45 PDT 2026; root:xnu-12377
.162.13~2/RELEASE_ARM64_T8140 iPhone17,3
[~Downloads]$ 
A continuación  introduzco el siguiente comando del HTML SSH-keygen:
[~Downloads]$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/private/var
/mobile/Containers/Data/Application/8F8B8576-BB74
-4EA9-A54E-FB51B92576DB/Documents/.ssh/id_rsa): 
7:53 sigo con ssh 
~Downloads]$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/private/var
/mobile/Containers/Data/Application/8F8B8576-BB74
-4EA9-A54E-FB51B92576DB/Documents/.ssh/id_rsa): 1
Reply is: 1.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in 1
Your public key has been saved in 1.pub
The key fingerprint is:
SHA256:Y40hjNg9MKhrmt8XdN/vtIHEwddeTYJPisWWfACuM1
c mobile@localhost
The key's randomart image is:
+---[RSA 3072]----+
|   .o     .+.+. .|
|  .o *   . .B o+.|
| .. o = . .+E=. +|
|.     .o.=.o.o...|
| .   . .S.o.o   .|
|..    .. =....   |
|o.     .    ..o  |
|o  .  .      ..o |
| .. ..       .o  |
+----[SHA256]-----+
[~Downloads]$ 
7:55 hago captura de pantalla para tener la imagen generada de ssh
8:00 añado la foto aquí 
![[IMG_4316.jpeg]]
![[Pasted image 20260807080326.jpg]]
Código dentro de fotos 
8:05 sigo y procedo a aprender el modelo OSI
[https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-osi-model/](https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-osi-model/)
Mando el HTML a Gemini para que ponga botones de copiado rápido
No hace falta al final por qué funciona bien el HTML
OSI protocolos 
| Capa | Nombre | Función Principal | Protocolos / Elementos | Enfoque en Ciberseguridad |
| :---: | :--- | :--- | :--- | :--- |
| **7** | **Aplicación** | Interfaz directa con software y usuario final. | HTTP, HTTPS, SMTP, DNS | **Ataques DDoS Capa 7** (HTTP Floods, agotamiento de recursos del servidor). |
| **6** | **Presentación** | Traducción, formato, compresión y **cifrado/descifrado**. | TLS/SSL, ASCII, Base64 | Vulnerabilidades en algoritmos de cifrado, desinteligibilidad de datos. |
| **5** | **Sesión** | Apertura, mantenimiento y cierre de sesiones de comunicación. | RPC, Sockets, SMB | Secuestro de sesión (*Session Hijacking*), ataques Replay. |
| **4** | **Transporte** | Transmisión de datos segmento a segmento (fiable o rápida). | TCP, UDP | SYN Floods, Port Scanning (escaneo de puertos TCP/UDP). |
| **3** | **Red** | Enrutamiento y direccionamiento lógico entre redes. | IP, ICMP, Routers | IP Spoofing, Ping Floods (ICMP DDoS), manipulación de tablas de rutas. |
| **2** | **Enlace de Datos** | Transferencia de tramas entre nodos de la misma red local. | Ethernet, MAC, Switches | ARP Spoofing, MAC Flooding, ataques VLAN Hopping. |
| **1** | **Física** | Transmisión física de bits brutos sobre el medio. | Cables RJ45, Fibra, Radio | Intercepción de señal (*Eavesdropping*), Jamming de Wi-Fi, corte físico. |

https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/
OSI:El modelo OSI se puede ver como un lenguaje universal para la conexión de las redes de equipos. 
Se basa en el concepto de dividir un sistema de comunicación en siete capas abstractas, cada una apilada sobre la anterior.
Para capas ver foto de capas 
 
 Ataques ddos: https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/
 Ataques a la capa de aplicación se dirigen a la capa 7:
https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/

Internet no sigue OSI
Cada capa es específica y se comunica con las otras
Internet no sigue estrictamente OSI (sigue cerca paquetes de internet)
OSI útil para resolver problemas
OSi ayuda a desglosar problema y a identificar causa
Si problema reduce 1 capa no se hace trabajo innecesario 
Informe de seguridad 
https://www.cloudflare.com/lp/security-signals-report/2026/
C7-interactúa datos usuario apps no forman parte de capa 
la capa de aplicación es responsable de los protocolos y la manipulación de datos de los que depende el software para presentar datos significativos al usuario
Protocolos de capa de app incluyen HTTP y SMTP 
C6-responsable de preparar datos para app para capa de app
Hace que datos se preparen para apps
Responsable de traducción cifrado y comprensión de datos 
c6 traduce datos en sintaxis para que receptor 
# ### 6:22  8/8/2026 día 3 OSI:
6:22 a 8:40 2:18h
Total acumuladas h: 3:18h
# #### 8:56 9/8/2026 día 4 OSI:
6:22 8:56 total día 2:34
Acumuladas    5:52
# Ver opciones de configuración visual (fuente, colores, cursor)
config

# Modificar tamaño de fuente (-s) y color de fondo (-b)
config -s 14 -b black

# Editar el archivo de perfil para persistir aliases y variables de entorno
pico ~/Documents/.profile
# o con vim:
vim ~/Documents/.profile

# Alias rápidos
alias c='clear'
alias ll='ls -la'
alias h='help'

# Mostrar mensaje de bienvenida
echo "a-Shell cargado correctamente."
# Generar clave RSA estándar de 3072 bits
ssh-keygen

# Conectarse a un servidor remoto mediante SSH
ssh usuario@direccion_ip -p 22

# Conectarse especificando una clave privada personalizada
ssh -i ~/.ssh/1 usuario@direccion_ip

🔗 Referencias y Enlaces de Interés

 a-Shell GitHub: [https://github.com/holzschu/a-shell](https://github.com/holzschu/a-shell)

 Guía de usuario a-Shell: [https://bianshen00009.gitbook.io/a-guide-to-a-shell/](https://bianshen00009.gitbook.io/a-guide-to-a-shell/)

 SSH Command Reference: [https://www.ssh.com/academy/ssh/command](https://www.ssh.com/academy/ssh/command)

 Aprender Modelo OSI (Cloudflare): [https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-osi-model/](https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-osi-model/)

 Ataques DDoS Capa 7: [https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/](https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/)

""| Capa | Nombre | Función Principal | Protocolos / Elementos | Enfoque en Ciberseguridad |
| :---: | :--- | :--- | :--- | :--- |
| **7** | **Aplicación** | Interfaz directa con software y usuario final. | HTTP, HTTPS, SMTP, DNS | **Ataques DDoS Capa 7** (HTTP Floods, agotamiento de recursos del servidor). |
| **6** | **Presentación** | Traducción, formato, compresión y **cifrado/descifrado**. | TLS/SSL, ASCII, Base64 | Vulnerabilidades en algoritmos de cifrado, desinteligibilidad de datos. |
| **5** | **Sesión** | Apertura, mantenimiento y cierre de sesiones de comunicación. | RPC, Sockets, SMB | Secuestro de sesión (*Session Hijacking*), ataques Replay. |
| **4** | **Transporte** | Transmisión de datos segmento a segmento (fiable o rápida). | TCP, UDP | SYN Floods, Port Scanning (escaneo de puertos TCP/UDP). |
| **3** | **Red** | Enrutamiento y direccionamiento lógico entre redes. | IP, ICMP, Routers | IP Spoofing, Ping Floods (ICMP DDoS), manipulación de tablas de rutas. |
| **2** | **Enlace de Datos** | Transferencia de tramas entre nodos de la misma red local. | Ethernet, MAC, Switches | ARP Spoofing, MAC Flooding, ataques VLAN Hopping. |
| **1** | **Física** | Transmisión física de bits brutos sobre el medio. | Cables RJ45, Fibra, Radio | Intercepción de señal (*Eavesdropping*), Jamming de Wi-Fi, corte físico. |

+-------------------------------------------------------------+
|  Capa 7: APLICACIÓN   --> HTTP, HTTPS, SMTP, DNS, FTP, SSH  |
+-------------------------------------------------------------+
|  Capa 6: PRESENTACIÓN --> TLS/SSL, JSON, XML, JPEG (Cifrado)|
+-------------------------------------------------------------+
|  Capa 5: SESIÓN       --> NetBIOS, RPC, Sockets             |
+-------------------------------------------------------------+
|  Capa 4: TRANSPORTE   --> TCP, UDP                          |
+-------------------------------------------------------------+
|  Capa 3: RED          --> IPv4, IPv6, ICMP, IPsec (Routers) |
+-------------------------------------------------------------+
|  Capa 2: ENLACE DATOS --> Ethernet, Wi-Fi, MAC, Switches    |
+-------------------------------------------------------------+
|  Capa 1: FÍSICA       --> Cables, Fibra, Señales de Radio  |
+-------------------------------------------------------------+
# ######8:56 10/8/2026 día 6 OSI:
2:34 día 10:13:10 h termine
Total acumuladas 
Hago copia de seguridad hacia notas
Notas no aparece en compartir así que en el PC Mac sincronizo el móvil con PC 
Creo HTML nuevo sincronizado actualizado
Y sincronizo Obsidian entre Mac y iPhone con iCloud
Buscaré cómo hacer copia de seguridad 
12:51 7/8/2026. 
16:05 todo listo para jornada siguiente atajo echo y archivo HTML en app  Documents en descargas/hack/  y en iCloud 
Todo sincronizado además ahora el HTML tiene una pestaña llamada guía de referencia donde pego todo lo que apunto en Obsidian y lo indexa y ofrece en forma de índice que al tocar se despliega con botones de copiado rápido y enlaces clicables
La pestaña estudiar tiene una checklist de 3 que cuando se completa ofrece los 3 siguientes pasos desplegables con referencias comandos webs y demás 
16:23 lo dejé en 
https://www.cloudflare.com/es-es/learning/ddos/glossary/open-systems-interconnection-model-osi/
6 Capa de presentación
Leer 1 capa 7 y pasar a Documents el HTML capa 6 apuntar todo en obsidian
Día 6 10/8/2026 17:40 empiezo a estudiar OSI:  
[Documents]$ openssl s_client -connect google.com:443
openssl: command not found
[Documents]$ openssl version
which openssl
Modifico el atajo para incluir ashell-mini
El 1 comando no funciona así que voy a la web https://www.cloudflare.com/es-es/learning/ddos/glossary/open-systems-interconnection-model-osi/ para aprender capa 7 y 6 el objetivo del día es la 6 el primero más concretamente tls SSL formatos crifrados 
Me pongo a ello 
Osi modelo conceptual creado por organizacion estandarización permite sistemas conecten estándar da estándar para conectar lenguaje universal para conexion divide sistema en 7 capas 
7 app láyer: Human-computer interaction layer, where applications can access the network services
6 presentation layer:Ensures that data is in a usable format and is
where data encryption occurs
5 sesión layer:Maintains connections and is responsible for controlling ports and sessions
4 transport layer:Transmits data using transmission protocols including TCP/UDP
3 network layer:Decides which physical path the data will take
2 data link layer:Defines the format of data on the network
1 physical layer:Transmits raw bit stream over the physical medium

7. Capa de aplicación (Application Layer):  
Capa de interacción entre el usuario y el ordenador, donde las aplicaciones pueden acceder a los servicios de red.

6.Capa de presentación (Presentation Layer):  Garantiza que los datos estén en un formato utilizable y es donde se realiza el cifrado de los datos.

5.Capa de sesión (Session Layer):  
Mantiene las conexiones y se encarga de controlar los puertos y las sesiones.

4.Capa de transporte (Transport Layer):  
Transmite los datos utilizando protocolos de transmisión, incluidos TCP/UDP.

3.Capa de red (Network Layer):  
Decide qué ruta física seguirán los datos.

2.Capa de enlace de datos (Data Link Layer):  
Define el formato de los datos en la red.

1.Capa física (Physical Layer):  
Transmite el flujo de bits sin procesar a través del medio fisico
7 → Aplicación  
6 → Presentación  
5 → Sesión  
4 → Transporte  
3 → Red  
2 → Enlace de datos  
1 → Física
7-6-5 → Aplicación, datos y sesiones  
4 → TCP/UDP  
3 → IP/routing  
2 → Ethernet/MAC  
1 → Señales/cables/Wi-Fi físico
Cada osi función comunica capas 
Los ddos a osi capas específicas https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/ 
Ataques a capa de app https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/
Ataques app capa 7 ataques capa ptrotoclo 3 y 4 
Osi desglosar  problema e identificar causa 
Problema-capa-evita trabajo
Las 7 capas:
7:app
6:presentación
5:sesión
4:transporte
3:red
2:enlace de datos
1:física 
# ###### 17:40 10/8/2026 Día 6 OSI:
Hoy 1:12h acumuladas 9:28h
# ####### 6:47 11/8/2026 día 7 OSI:
traceroute 8.8.8.8
Comand not found en Ashell mini 
Procedo a investigar cómo arreglarlo: 
ChatGPT introduzco:
traceroute 8.8.8.8
Comand not found 
Ashell mini 
Dame el comando para que cualquier comando funcione en Ashell- mini y no de problemas 
Responde:
Con comandos
Procedo a arreglarlo 
Hoy toca la capa 3 y finalizar las 7:
#######Capa 7:Aplicacion:
**********************************************
Única interactúa usuario (software) dependen de C7 para iniciar software cliente no C7  C7 protocolos manipulación datos depende datos usuario C7 incluye HTTP-(https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) SMTP-(https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) protocolo correo permite comunicaciones (https://www.cloudflare.com/learning/email-security/what-is-email/)
######Capa 6:Presentación:
********************************************
Responsable datos usar capa app los preparan consumo apps responsable de traducción cifrado y compresión
(https://www.cloudflare.com/learning/ssl/what-is-encryption/) 
Dos conectados puede usar distintos codificadores responsable traducir entrantes receptor si cifrada responsable cifrado emisor y decodificar receptor para app legible comprime datos de C7 antes enviar a C5 más velocidad/eficiencia comunicación/minimizacion datos transferidos 
#####Capa 5: Sesión:
**********************************************
Responsable apertura/cierre 2 dispositivos tiempo entre apertura/cierre-sesion garantiza abierta datos cambiando después cierra para no desaprovechar recursos sincroniza datos utilizando control 
####Capa 4: Transporte:
**********************************************
Responsable cifrada (extremo a extremo)toma sesión y divide en trozos pequeños (segmentos) responsable rearmar segmentos para construir datos para sesion responsable flujo y errores flujo-velocidad-conexión rápida control errores y garantiza recibidos  y si no solicita 
(https://www.cloudflare.com/learning/ddos/glossary/tcp-ip/)
(https://www.cloudflare.com/learning/ddos/glossary/user-datagram-protocol-udp/)
###Capa 3: Red:
**********************************************
Responsable transferencia redes si dispositivos se encuentran en red la capa no necesaria divide segmentos en unidades pequeñas paquetes(https://www.cloudflare.com/learning/network-layer/what-is-a-packet/) los junta en receptor
La capa busca la ruta para datos a destino [enrutamiento] (https://www.cloudflare.com/learning/network-layer/what-is-routing/)
Protocolos incluyen ip 
 [Protocolo control Internet (ICMP)](https://www.cloudflare.com/learning/ddos/glossary/internet-control-message-protocol-icmp/), el [Protocolo grupo Internet (IGMP)](https://www.cloudflare.com/learning/network-layer/what-is-igmp/) paquete [IPsec](https://www.cloudflare.com/learning/network-layer/what-is-/)##
 ##Capa2:Enlace datos:
 ****************************************
 Similar a 3 excepto que capa enlace facilita datos dos de red(misma) la 2 coje paquetes y divide en partes pequeñas (tramas) 
 Responsable control flujo y control errores comunicaciones red (transporte solo control flujo y errores )
# Capa 1: Física :
**********************************************
 Esquioo físico en datos (cables y conmutadores)-(https://www.cloudflare.com/learning/network-layer/what-is-a-network-switch/)
 Datos en bits 1 y 0  dispositivos estar acuerdo a convención a convención a 1 y 0 (bits) en dispositivos
 Transmisión en osi:
 Datos atravesar 7 capas en orden en emisor y receptor 
 # #######7:23 11/8/2026 día 7 OSI:
  como están sin acabar las 7 capas sigo por encima de capa 3 para acabar 
 7:53 11/8/2026 descanso
 8:31 he editado esta nota en el descanso para asegurar que refleja bien los días 1/2/3 las h de estudio y que lleva orden en todo aparte de que esté documentada 
 8:32 sigo terminando capa 6 y termino capa 7 Total acumuladas h:hasta ahora
 9:46 procedo a marcar conceptos y dias 
 dia 7 empiezo: 6:47
 Termino:1204
 Horas día 6:51
 Acumuladas 16:19h
 Falta: Terminal para Mac y iPhone sincronizada  
 # ########5:18 12/8/2026 día 8 capa red direccionamiento subnetting ICMP 
 https://www.google.com/search?client=firefox-b-m&q=capa%20red%20direccionamiento%20subnetting%20ICMP%20
 Welcome to Alpine!

You can install packages with: apk add <package>

You may change this message by editing /etc/motd.

localhost:~# traceroute 8.8.8.8
traceroute to 8.8.8.8 (8.8.8.8), 30 hops max, 46 byte packets
 1traceroute: sendto: Socket is connected
localhost:~# 
localhost:~# arp -a
arp: can't open '/proc/net/arp': No such file or directory
localhost:~# 
localhost:~# tcpdump -i any -c 10 -n
-ash: tcpdump: not found
localhost:~# 
Capa 3 Red (IP / Direccionamiento / Subnetting / ICMP)
Capa 3: 
se encarga del direccionamiento lógico y del enrutamiento de paquetes de datos a través de diferentes redes interconectadas usa protocolos ip icmp para mover dirección de origen a destino
Protocolo IP:
Dirección lógica identifica únicamente cada dispositivo en una red
IPv4 e IPv6 versiones en uso v4 32 y v6 128 (bits)
Encapsulamiento: añade info origen/destino a paquete
Direccionamiento/Subnetting:
Red/host:ip dividida entre red y equipo
Máscara de su red:que parte de ip es de red y cuál de host 
Subnetting:divide red en redes para mejorar rendimiento y seguridad 
Protocolo ICMP:
Control y errores:informa sobre ellos con mensajes 
Herramienta Ping: usa ICMP para comprobar conexión con (PC)
Herramienta Traceroute:enseña ruta de paquetes en routers
5:54 termino 1 tarea del día
localhost:~# arp -a
arp: can't open '/proc/net/arp': No such file or directory
localhost:~# 
Capa 1 Física & Capa 2 Enlace (Ethernet / Direcciones MAC / ARP)
https://www.google.com/search?client=firefox-b-m&q=Capa%201%20F%C3%ADsica%20%26%20Capa%202%20Enlace%20%28Ethernet%20%2F%20Direcciones%20MAC%20%2F%20ARP%29
Ethernet usa mac para mandar datos a red local Mac fija (estática)ip cambia (dinámica)
ARP une ip con Mac para hablar en la red 
06:03 Comienzo descanso/Termino descanso 6;07 - 4 minutos de descanso 
Ethernet/Mac: 
Ethernet:estándar que conecta (pcs)en red por cable/señañes
Mac:viene de fábrica es un código de 48 bits no cambia e identifica el equipo,es una tarjeta que identifica
Protocolo ARP:
Arp:un PC pregunta quien tiene la ip correcta a la red
Respuesta:el PC con esa ip responde con Mac 
Tabla caché: PC tardan respuestas para no preguntar qué envían
localhost:~# tcpdump -i any -c 10 -n
-ash: tcpdump: not found
localhost:~# 
https://www.google.com/search?client=firefox-b-m&q=Captura%20y%20An%C3%A1lisis%20de%20Tr%C3%A1fico%20de%20Red%20%28Wireshark%20%26%20Tcpdump
Captura y Análisis de Tráfico de Red 
Wireshark tcpdump:
Herramientas para captura/analisis de red  tcpdump es capturador en línea de comandos para servidores 
whireshark es gráfica/ avanzada y examina paquetes se usan juntos para análisis en whireshark
Uso tcpdump:
Capturar: tcpdump -i eth0
Guardar: tcpdump -i eth0 -w captura.pcap
Filtrar puertos: tcpdump -i eth0 port 80
Uso wireshark
Seleccionar: elige tarjeta res y pulsar botón
Filtros visualización: IP/HTTP …
Seguir TCP: clic en paquete y reconstruye la charla completa de sesión
6:55 hago pausa para reparar terminal
7:06 termino de arreglar terminal continuo
Total tiempo no estudiado: 15 minutos 
7:12 instalo todo a iSH para evitar fallos
localhost:~# curl -I https://example.com
HTTP/2 200 
date: Wed, 12 Aug 2026 05:14:44 GMT
content-type: text/html
server: cloudflare
last-modified: Sat, 08 Aug 2026 02:07:29 GMT
allow: GET, HEAD
accept-ranges: bytes
age: 4946
cf-cache-status: HIT
cf-ray: a29cff89dc05f771-MAD

localhost:~# 
Fundamentos OWASP Top 10 & Pentesting Web
https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=AOlV&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnt_medfkAcFtbiCaiablEO6aJQaxg%3A1786511845349&udm=50&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiCgrefq5qWAxVkygIHHUsSJrYQ2J8OegQIDhAE&biw=393&bih=651&dpr=3&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1

https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=3iQq&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnuPZ4nCUp_5sdYQYUWr7jIeSvGShw%3A1786512757600&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiSorbSrpqWAxVG7LsIHaQdF0AQ2J8OegQIDhAE&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1&udm=50&biw=393&bih=651&dpr=3
OWASP:Top 10 guía 
https://owasp.org/Top10/2021/es/
Recoge 10 riesgos críticos en apps web
Pentesting web es simular/descubrir/mitigar vulnerabilidades antes
Las graves:
organizado en frecuencia/impacto
A01:2021-acceso roto:
Usuarios van a datos/funciones fuera de permiso 
A02:2021-Falla criptográfica:
Exposición de datos por cifrado/algoritmo
A03:2021-Inyección:
Datos enviados a intérprete comandos involuntarios 
A04:2021-Diseño inseguro:
Errores/arquitectura/diseño de app que no se arreglan
A05:2021-Configuración seguridad incorrecta:
Sistemas por defecto servicios/mensajes de error con detalle
A06:2021-Componentes:
Hackeables que usan librerías/framewroks/software con fallos 
A07:2021Fallos:
identificación/autentificacion 
Permite fuerza/robo por la gestión de keys (contraseñas)
A08:2021-Fallos integridad de software/datos:
Código/datos sin ver origen
A09:2021-Fallos en registro/supervisión de seguridad:
No registrar criticos(eventos)impide detectar ataques 
A10:2021-Falsificación solicitudes servidor (SSRF):
App/web manipulada para hacer peticiones a servidores 
Metodología de Pentesting Web:
1 Reconocimiento: 
Recopila información sobre objetivo/activa
2 Escaneo y Análisis:
Saber por dónde entrar con herramientas 
3 Explotación (Gain Access):
Aprovecha vulnerabilidades
4 Post-explotación:
Mide impacto de fallo analiza datos comprometidos o escala privilegios.
5 Reporte: Crear informe para desarrollador/ejecutivo/gerencia y dice la solución
https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=3iQq&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnuPZ4nCUp_5sdYQYUWr7jIeSvGShw%3A1786512757600&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiSorbSrpqWAxVG7LsIHaQdF0AQ2J8OegQIDhAE&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1&udm=50&biw=393&bih=651&dpr=3
Herramientas pentester:
Se unan entornos/ herramientas 
Kali SO para seguridad tiene muchas herramientas 
Burp Owasp proxis para analizar/modificar/repetir HTTP (entre navegador y servidor)
Nmap escáner para abiertos/ejecucion (puertos)
Dirsearch/Gobuster para directorios/archivos en servidor
OWASP Juice Shop vulnerable para hacking segura 
8:18 12/8/2026 acabo de estudiar
Empeze a las 5:18
Total h hoy 3h
Acumuladas 19:19 h
# ########7:08 13/8/2026 dia 8 Scripting Bash & Python para Automatización Terminal
localhost:~# python3 -m http.server 8080
-ash: python3: not found
localhost:~# 
https://www.py4e.com/
Python para todos:
Materiales https://www.py4e.com/lessons
Conferencias https://www.youtube.com/watch?v=UjeNA_JtXME&list=PLlRFEj9H3Oj7Bp8-DfGpfAfDBiblRfl5p&index=1
Libro https://www.py4e.com/book.php
También en: coursera https://www.coursera.org/specializations/python
Edx https://www.edx.org/bio/charles-severance
Freecodecamp https://www.youtube.com/watch?v=8DvywoWv6fI
Certificados gratuitos para estudiantes y personal de la universidad de Míchigan 
https://online.umich.edu/series/python-for-everybody/
Si inicias sesión te unes a un mundo libre curso online con calificaciones asignaciones/foros/insignias por tus esfuerzos se toman en serio la privacidad se puede revisar política para detalles https://www.py4e.com/privacy
Todo esto se puede usar https://www.py4e.com/tsugi/cc/ IMS también herramientas IMS la clave/secreto https://www.py4e.com/tsugi/admin/key/index.php el código/diapositivas/contenido está en
https://github.com/csev/py4e puedes hacer lo que quieras con el mismo puedes traducir el sitio publicarlo (instrucciones traducción github)
https://github.com/csev/py4e/blob/master/TRANSLATION.md  la web usa Tsugi 
http://www.tsugi.org/ para aprender si quieres colaborar http://www.tsugi.org/
https://www.py4e.com/ 
python3 -m http.server 8080
Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ...
 Hardening Unix/Linux & Auditoría de Archivos de Log
 tail -f /var/log/syslog no funciona en ishell
 Con otros comandos 
localhost:~# echo "[INFO] Sistema iniciado" > prueba.log
tail -f prueba.log 
INFO] Sistema iniciado
localhost:~# python3 -m http.server 8080
Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ...
Ishell es solo en inglés
[https://www.cisecurity.org/cis-benchmarks/]
8:31 descanso 
CIS 
configuraciones para productos 
son expertos/esfuerzo/consenso mundial ayudan a sistemas contra amenazas 
Puntos de referencia https://learn.cisecurity.org/benchmarks
Nuevo? 
https://www.cisecurity.org/cis-benchmarks-overview
Benchmarks/puntos https://fast.wistia.com/embed/medias/s1abjx9h37/  
encuentra lo que buscas tecnología/subcategoria/filtar(jopcional)/CIS/accede a todo esto en la web https://www.cisecurity.org/cis-benchmarks a unos 7 mm del inicio de la web en cuadro azul
Construye kits https://www.cisecurity.org/cis-securesuite/cis-securesuite-build-kit-content
descarga referencias v2.0.0 https://learn.cisecurity.org/benchmarks 
A fondo https://www.cisecurity.org/benchmark/alibaba_cloud
Adaptar 
https://www.cisecurity.org/cis-securesuite
- Alibaba Cloud Linux 3 (2.0.0) 
- Aliyun Linux 2 (1.0.0)
https://learn.cisecurity.org/benchmarks
Adaptar seguridad https://www.cisecurity.org/cis-securesuite
Alibaba Cloud Linux
https://learn.cisecurity.org/benchmarks?_gl=1*1m0zp0f*_gcl_au*NDc3MzU0ODExLjE3ODY2MDI2NDQuLS4tLjE3ODY2MDI2NDQuMTg3MzQzOTI1My4xNzg2NjAyNjQ0LjE3ODY2MDQ2NjQ.*_ga*MjAwNTkxMTQ5OS4xNzg2NjAyNjYz*_ga_N70Z2MKMD7*czE3ODY2MDI2NjMkbzEkZzEkdDE3ODY2MDQ2NjgkajUzJGwwJGgw*_ga_3FW1B1JC98*czE3ODY2MDI2NjMkbzEkZzEkdDE3ODY2MDQ2NjgkajUzJGwwJGgw
Adaptar
https://www.cisecurity.org/cis-securesuite
Alibaba Cloud Linux
Referencias 
https://learn.cisecurity.org/benchmarks
9:11 termino estudiar 
Total h hoy 1:56 minutos
Acumuladas         21:15h a dia 8
Creado nuevo HTML
Que funciona en Mac y iPhone
Vale para todo 
Creado con Gemini
11:08 actualizados foto y nombre en RRSS
Procedo a colgar apuntes de Obsidian
