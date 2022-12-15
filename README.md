![Iotproject](https://user-images.githubusercontent.com/94047075/207590719-65581173-c96c-419a-b612-d6092f433391.png)
# Iot_project. 
Viktiga förklaringar: Syftet med kursen är att förstå hur IoT-lösningar är uppbyggda och hur de olika komponenterna knyts ihop till en helhet.
Efter kursen ska studenten ha en förståelse och kunskap om hur devices knyts till en molntjänst (provisioning), hur de administreras (decvice management) och hur grundläggande molntjänster används för att bygga en tjänst som tillhandahåller och visualiserar insamlad data.” ”Målet med kursen är att student ska kunna skapa en grundläggande arkitektur för en IoT-lösning utifrån krav som studenten själv kan ställa upp från ett hypotetiskt business case. 
Vidare jag skall Jag kunna realisera lösningen på någon befintlig molnplattform och simulera data för lösningen.
AWS IOT:
ESP32![image](https://user-images.githubusercontent.com/94047075/207983546-08c9e09c-cc5d-4d87-8d16-96555c3ed073.png)


IAAS, Infrastructure-as-a-service, eller IaaS, är ett steg bort från lokal infrastruktur. Det är en pay-as-you-go-tjänst där en tredje part förser dig med infrastrukturtjänster,
som lagring och virtualisering, när du behöver dem, via ett moln, via internet

PAAS: Platform-as-a-service (PaaS) är ytterligare ett steg längre från fullständig, lokal infrastrukturhantering. Det är där en leverantör är värd för hårdvaran och mjukvaran på sin egen infrastruktur och levererar denna plattform till användaren som en integrerad lösning, 
lösningsstack eller tjänst via en internetanslutning.

AWS: Offentliga molnleverantörer som AWS, Microsoft Azure och Google Cloud är exempel på IaaS. och PAAS.

IOT: Internet of things (IoT) som det kallas, beskriver fysiska objekt (eller grupper av sådana objekt) med sensorer, bearbetningsförmåga, 
mjukvara och annan teknik som ansluter och utbyter data med andra enheter och system över Internet eller andra kommunikationsnätverk.
![image](https://user-images.githubusercontent.com/94047075/207977406-19a3211b-f9ee-49a8-aab7-9d708b1a4c1e.png)
﻿



Install Git, Python, and the AWS IoT Device SDK for Python: Här installera jag git, python och AWs för ens computer.:This document provides instructions for
installing and configuring the AWS IoT Device SDK for Python. It includes examples demonstrating the use of the SDK

Sedan skapa jag en fil som heter mkdir cert. Sedan så kolla jag för att se att den har skapat med ls -l ~/certs. Så för jag total 0.

Git clone: git clone står eller används främst för att peka på ett befintligt repo och göra en klon eller kopia av det repet i en ny katalog, på en annan 
plats. Det ursprungliga arkivet kan placeras på det lokala filsystemet eller på fjärranslutna protokoll som stöds. Git clone-kommandot kopierar ett befintligt
Git-förråd

Nästa blir IOT endpoint: Det gör jag under, jag gjorde först installation av Ascii som såg ut så här med massa rader

Under AWS console har jag created thing och certificate. nu under policies har jag fastnat lite på hur jag ska göra färdig det. 
Det visar malfunktioned policies. Här hade jag fastnat på länge tills jag kunde göra om policy, gjorde om certifikak, gjorde download, Kopierade, kliistra i filen som heter cert:
Gjorde rename, device.pem.crt
RSA klistrade jag på cert mapp och byt namn på den., Dopte om root till Amazon
gjorde download och byt namn på public key or private key.
och byte Region till US-east.1. Den gjorde jag om där det fanns Region. byt discount ID till nummer som jag hade under min AWS profil.

Sedan kommer jag till consolen och skriver in den här kommando: cd ~/aws-iot-device-sdk-python-v2/samples
python3 pubsub.py --topic test/topic --ca_file ~/certs/Amazon-root-CA-1.pem --cert ~/certs/device.pem.crt --key ~/certs/private.pem.key --endpoint your-iot-endpoint" för att göra Subscribe to the topic, test/topic. 

After att har gjort det så fick jag 10 recieved messages och 10 messages sent.


