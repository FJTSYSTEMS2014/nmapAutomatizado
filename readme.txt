
Instalar: 
git clone https://github.com/FJTSYSTEMS2014/nmapAutomatizado.git
cd nmapAutomatizado
chmod +x ./nmapAutomatizado.sh
sudo apt install -y $(cat requerimientos.txt)


ejecutar: 
 ./nmapAutomatizado.sh 
uso:
 ./nmapAutomatizado.sh --host 192.168.0.1  --type All     
 ./nmapAutomatizado.sh --host 192.168.0.1 -t Basic
./nmapAutomatizado.sh --host  192.168.0.1 -t network -s ./ruta_al_ejecutable_de_Nmap_que_se_utilizará_para_el_escaneo/nmap
ideal CTF
./nmapAutomatizado.sh --host plataformaHackTheBox.htb -t Recon -d 8.8.8.8

La extensión ".htb" es comúnmente utilizada por la plataforma Hack The Box (HTB)


info:
/nmapAutomatizado.sh                             

Usage: nmapAutomatizado.sh -H/--host <TARGET-IP> -t/--type <TYPE>
Optional: [-r/--remote <REMOTE MODE>] [-d/--dns <DNS SERVER>] [-o/--output <OUTPUT DIRECTORY>] [-s/--static-nmap <STATIC NMAP PATH>]              
                                                                         
Scan Types:                                                              
        Network : Shows all live hosts in the host's network (~15 seconds)                                                                        
        Port    : Shows all open ports (~15 seconds)                     
        Script  : Runs a script scan on found ports (~5 minutes)         
        Full    : Runs a full range port scan, then runs a script scan on new ports (~5-10 minutes)
        UDP     : Runs a UDP scan "requires sudo" (~5 minutes)           
        Vulns   : Runs CVE scan and nmap Vulns scan on all found ports (~5-15 minutes)                                                            
        Recon   : Suggests recon commands, then prompts to automatically run them
        All     : Runs all the scans (~20-30 minutes)


info español:

El archivo "nmapAutomatizado.sh" es un script automatizado que utiliza la herramienta de escaneo de red Nmap para realizar diversas tareas de escaneo en una red o en un host específico. El script tiene varias opciones de uso que permiten realizar diferentes tipos de escaneos y análisis de seguridad en un objetivo determinado. Aquí tienes una explicación de las opciones y los tipos de escaneo disponibles:

Opciones Obligatorias:

-H o --host <TARGET-IP>: Debes especificar la dirección IP del objetivo que deseas analizar.
-t o --type <TYPE>: Debes especificar el tipo de escaneo que deseas realizar, eligiendo uno de los tipos disponibles (se explicarán a continuación).
Opciones Opcionales:

-r o --remote <REMOTE MODE>: Esta opción permite especificar si deseas realizar el escaneo de forma remota. Puede tener valores como "true" o "false".
-d o --dns <DNS SERVER>: Permite especificar un servidor DNS personalizado para el escaneo.
-o o --output <OUTPUT DIRECTORY>: Puedes especificar un directorio de salida para guardar los resultados del escaneo.
-s o --static-nmap <STATIC NMAP PATH>: Permite especificar una ruta personalizada para la instalación estática de Nmap.
Tipos de Escaneo Disponibles:

Network: Este tipo de escaneo muestra todos los hosts vivos en la red del objetivo y suele tardar unos 15 segundos en completarse.
Port: Escanea todos los puertos abiertos en el host y también toma alrededor de 15 segundos.
Script: Ejecuta un escaneo de scripts en los puertos encontrados y generalmente lleva unos 5 minutos.
Full: Realiza un escaneo completo de todos los puertos disponibles y luego ejecuta un escaneo de scripts en los nuevos puertos encontrados. Puede tomar entre 5 y 10 minutos.
UDP: Realiza un escaneo UDP, pero generalmente requiere permisos de superusuario (sudo) y demora aproximadamente 5 minutos.
Vulns: Realiza un escaneo de CVE (Common Vulnerabilities and Exposures) y un escaneo de vulnerabilidades de Nmap en todos los puertos encontrados, que generalmente toma de 5 a 15 minutos.
Recon: Sugiere comandos de reconocimiento y luego pregunta si deseas ejecutarlos automáticamente.
All: Ejecuta todos los tipos de escaneo disponibles, lo que generalmente lleva de 20 a 30 minutos.

En resumen, el script "nmapAutomatizado.sh" te permite realizar una variedad de escaneos de red y análisis de seguridad en un objetivo, desde escaneos simples de puertos hasta escaneos exhaustivos de vulnerabilidades. Puedes personalizar las opciones según tus necesidades y objetivos de seguridad.
