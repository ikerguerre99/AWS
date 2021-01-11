# ¿Qué hace cada línea de cron?

### ¿Qué es CRON?
Es un administrador de procesos en segundo plano usado unicamente en Linux. Comprueba si existe alguna tarea para ser ejecutada a la hora configurada del mismo sistema.

### ¿Qué es CRONTAB?
Es un archivo de texto que contiene la lista de comandos que se deben ejecutar. Comprobará la fecha y hora de todos los comandos y procesos a ejecutar y los ejecutará en segundo plano.

## 30 * * * * /home/prueba.sh 
Ejecuta cada hora a y 30 el script llamado prueba.sh.

## 30 20 * * * /home/prueba.sh
Ejecuta a las 20:30 el script llamado prueba.sh.

## 30 20 * * 1-5 /home/prueba.sh
Ejecuta a las 20:30, los dias laborales (De lunes a viernes) el script llamado prueba.sh.

## 30 20 * * 2,4 /home/prueba.sh
Ejecuta a las 20:30, todos los martes y jueves el script llamado prueba.sh.

## 30 20 10,20 * * /home/prueba.sh 
Ejecuta a las 20:30, el dia 10 y el dia 20 de todos los meses y todos los años, el script llamado prueba.sh.

## */15 * * * * /home/prueba.sh 
Ejecuta cada 15 minutos todos los dias de todos los años el script llamado prueba.sh.

## @daily /home/prueba.sh
Ejecuta diariamente al comienzo del cada dia el script llamado prueba.sh.

## @mountly /etc/backup.sh 
Ejecutaría el comando si estuviera bien escrito, pero en este caso daría un error(supongo).

## @monthly /etc/backup.sh 
Ejecuta al comienzo de cada mes el script llamado backup.sh.

## 30 20 * * Mon-Fri /etc/test.sh 
Ejecuta a las 20:30, los dias laborales (De lunes a viernes) el script llamado test.sh.

## 1 0 1-7 * * [ "$(date '+%a')" = "Fri" ] && /etc/backup.sh

Hace una comparación para que solo imprima los viernes a las 00:01, de los dias 1 al 7 de cada mes, ejecute el script backup.sh.


# Ejercicio 7
## Crontab cada 5 minutos  

