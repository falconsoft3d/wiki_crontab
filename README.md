# Editamos el cron
```  
crontab -e
```  

# Repetimos cada 1 minutos
```  
*/1 * * * * python /home/marlon/Documentos/python/cron/write.py
```  


# Creamos el script
```  
# -*- coding: utf-8 -*-

from random import randrange

f = open('/home/marlon/Documentos/python/cron/holamundo.txt','a')
f.write('\n' + 'Hola Mundo: ' + str(randrange(1000)) )
f.close()
```  

# Reiniciamos el servicio
```  
service cron restart

```  
