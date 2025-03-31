# MS-SQL-Server

# Descripció de la base de dades escollida: **SQL Server**

## 1. Història i suport

**Microsoft SQL Server** és un sistema de gestió de bases de dades relacionals (SGBD-R) desenvolupat per **Microsoft**.\
Va començar a finals dels anys 80 i la primera versió (1.0) es va llançar el **1989**, en col·laboració amb **Sybase**.\
Des de llavors, Microsoft ha continuat el desenvolupament de forma independent.

Versions destacades: **2000, 2005, 2008, 2012, 2016, 2019, 2022...**

Funcionalitats destacades:

- Suport a **Big Data Clusters**
- Motor de **columnstore index**
- Integració amb **.NET**, **Azure** i **Power BI**
- Capacitats de **machine learning** i anàlisi avançada

El **suport oficial** és proporcionat per **Microsoft**, tant per la versió local com les del núvol (*Azure SQL*).

---

## 2. Casos d’ús recomanats

SQL Server és recomanat per a entorns on cal:

- Gestió de grans volums de dades relacionals
- Alta integritat i seguretat
- Integració amb l’ecosistema Microsoft

**Exemples:**

- Empreses bancàries i financeres
- Sistemes ERP i CRM
- Aplicacions web/intranets amb Windows Server
- Solucions de Business Intelligence amb SSRS i SSAS

---

## 3. Versions disponibles

| **Edició**               | **Descripció**                                                     |
| ------------------------ | ------------------------------------------------------------------ |
| `Express`                | Gratuïta i lleugera, ideal per estudi o apps petites               |
| `Developer`              | Gratuïta amb totes les funcionalitats, només per a desenvolupament |
| `Standard`               | Per a empreses petites/mitjanes, funcionalitats limitades          |
| `Enterprise`             | Completa, amb alta disponibilitat, BI i seguretat avançada         |
| `Azure SQL Database`     | Núvol (PaaS), escalable, gestió automàtica                         |
| `SQL Server on Azure VM` | Instal·lació clàssica sobre màquines virtuals Azure (IaaS)         |

---

## 4. Comparativa amb altres SGBD relacionals

| Característica     | SQL Server            | MySQL               | PostgreSQL           | Oracle DB          |
| ------------------ | --------------------- | ------------------- | -------------------- | ------------------ |
| Desenvolupador     | Microsoft             | Oracle              | Comunitat            | Oracle             |
| Llicència          | Propietària           | Codi obert (GPL)    | Codi obert           | Propietària        |
| Sistemes operatius | Windows/Linux         | Multiplataforma     | Multiplataforma      | Multiplataforma    |
| Escalabilitat      | Molt bona             | Bona                | Excel·lent           | Excel·lent         |
| Suport oficial     | Sí, Microsoft         | Sí, per Oracle      | Opcional (comercial) | Sí, Oracle         |
| Facilitat d’ús     | Excel·lent en Windows | Fàcil per a novells | Potent però complex  | Potent però costós |

---

## Webgrafia

- [Microsoft SQL Server – Pàgina oficial](https://learn.microsoft.com/sql/sql-server)
- [Comparació d’edicions de SQL Server](https://learn.microsoft.com/sql/sql-server/editions-and-components-of-sql-server)
- [Microsoft Azure – SQL Database](https://azure.microsoft.com/products/azure-sql/)
- [Wikipedia – Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server)
- [Comparativa SGBD – DB Engines](https://db-engines.com/en/system/Microsoft+SQL+Server%3BMySQL%3BOracle%3BPostgreSQL)
- [Docker Hub – SQL Server 2019](https://hub.docker.com/_/microsoft-mssql-server)

---
![image](https://github.com/user-attachments/assets/01541560-d411-48b5-905d-504ae6ea479f)

Un cop realitzada la instal·lació realitza una securització de la mateixa. Quins programa realitza aquesta tasca? Realitza una securització de la instal·lació.

![image](https://github.com/user-attachments/assets/fd0baa83-d768-4ebe-a4d6-5d0e83b2b306)

![image](https://github.com/user-attachments/assets/e23a7cc4-ad48-41bf-a462-b79ef782cd1f)
2.Quines són les instruccions per arrancar / verificar status / apagar servei de la base de dades del SBGB escollit a nivell sistema operatiu?
 
 Arrencar el servei
 
 ![image](https://github.com/user-attachments/assets/cba69150-b048-477c-919c-95dc94b6a32b)
 
 Verificar l'estat del servei
 
 ![image](https://github.com/user-attachments/assets/d5ed131a-e943-4aed-a374-56a81a46d635)
 
 Aturar el servei
 
 ![image](https://github.com/user-attachments/assets/f6537864-5f90-4e7e-ad82-41ab25efd548)

3.A on es troba i quin nom rep el fitxer de configuració del SGBD escollit?

 Primer accedir al docker amb
 ![image](https://github.com/user-attachments/assets/73351dc6-4c8c-43ef-b149-4923a89f6caf)

el fitxer es troba a:
![image](https://github.com/user-attachments/assets/168b49a0-ee15-479b-8255-7aefe714987d)

I el seu nom es:
![image](https://github.com/user-attachments/assets/be6449a4-de80-4c70-8598-2e5c27449f1f)

4.A on es troben físicament els fitxers de dades (per defecte). Com ho has sabut?

![image](https://github.com/user-attachments/assets/907c7e3f-dc7c-471f-91ad-3d0af3c27504)

Com ho has sabut?

Per la documentació oficial de SQL Server per a Linux, Microsoft indica que el directori per defecte és /var/opt/mssql/data per a les seves instàncies.

5.El servei de SGBD escollit en quins ports escolta. Quina modificació/passos caldrien fer per canviar aquest port a un altre per exemple? Important: No realitzis els canvis. Només indica els passos que faries.

![image](https://github.com/user-attachments/assets/4f33b8ff-09b9-42c8-ab8f-2e0822fbb250)
Els ports son 0.0.0.0:1433->1433/tcp

Un cop apagat editarem el fitxer mssql.conf

Primer parem el servei:
![image](https://github.com/user-attachments/assets/3e3df30f-a10a-4c95-8ff5-a026616f4d03)

I coloquem el nou port per el que escoltara
![image](https://github.com/user-attachments/assets/2ca9de83-ac4f-4353-b916-0a472d531efd)

Mapar el nou port a Docker en reiniciar el contenidor

docker run -e "ACCEPT_EULA=Y" \
           -e "MSSQL_SA_PASSWORD=ContrasenyaSegura123" \
           -p 1444:1444 \
           --name sqlserver2019 \
           -d rapidfort/microsoft-sql-server-2019-ib:latest


6.Incloure en la documentació un petit apartat a on s'expliqui com realitzar la connexió a la BD. Demostra que us podeu connectar al SGBD a través d’una eina de gestió de BD o  a través d’un programa.

Per podernos connectar a la nostre base de dades farem servir azure data studio " https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio " (hazme un elnaze resumido)

Coloquem la nostre informaccio:
![image](https://github.com/user-attachments/assets/fa73cb81-449e-4011-a798-0bfe7966c31c)

Un cop autentificat ja tenim acces a la nostre maquina virtual!
![image](https://github.com/user-attachments/assets/c7514dae-c410-4e16-959c-60d9f24dde2f)

Ja podem fer consultes
![image](https://github.com/user-attachments/assets/74cc7db1-b5ce-4e0c-8edf-d1565b226e38)











------









# MS-SQL-Server

## Documentació tècnica de la instal·lació i configuració de SQL Server 2019 amb Docker

> Aquesta documentació està orientada a tècnics informàtics i no a usuaris no experts.

---

## 1. Securització de la instal·lació

Un cop realitzada la instal·lació de SQL Server 2019 en Docker, cal aplicar una securització manual.

Quin programa realitza aquesta tasca?  
En el cas de SQL Server no hi ha una eina automàtica com en altres SGBDs. La securització s'ha de fer manualment mitjançant bones pràctiques.

**Accions realitzades:**
- Definir una contrasenya forta
- Verificar configuració de ports
- Control d’accés al contenidor

Aquí va (securitzacio-1.jpg)  
Aquí va (securitzacio-2.jpg)  
Aquí va (securitzacio-3.jpg)

---

## 2. Instruccions per gestionar el servei

**Arrencar el servei:**
```bash
docker start sqlserver
```
Aquí va (arrencar-servei.jpg)

Verificar l'estat del servei:

```bash
docker ps -a
```
Aquí va (status-servei.jpg)

Aturar el servei:

```bash
docker stop sqlserver
```
Aquí va (aturar-servei.jpg)

3. Fitxer de configuració del SGBD escollit
Per accedir al fitxer de configuració:

Accedir al contenidor:

```bash
docker exec -it sqlserver bash
```
Aquí va (accedir-docker.jpg)

Ruta del fitxer:

```bash
/var/opt/mssql/mssql.conf
```
Aquí va (ruta-config.jpg)

Nom del fitxer:

```bash
mssql.conf
```
Aquí va (nom-fitxer.jpg)

4. Ubicació dels fitxers de dades
Els fitxers de dades de SQL Server es troben a:

```bash
/var/opt/mssql/data/
```
Aquesta informació s’ha obtingut mitjançant la documentació oficial de Microsoft per SQL Server a Linux.

Aquí va (ubicacio-dades.jpg)

5. Ports i modificació
Ports per defecte:

```bash
0.0.0.0:1433->1433/tcp
```
Aquí va (port-docker.jpg)

Passos per modificar el port:

Aturar el servei:

```bash
docker stop sqlserver
```
Aquí va (stop-servei.jpg)

Editar el fitxer mssql.conf i afegir:
```bash
[network]
tcpport=1444
```
Aquí va (editar-conf-port.jpg)

Reiniciar el contenidor amb el nou port:

```bash
docker run -e "ACCEPT_EULA=Y" \
           -e "MSSQL_SA_PASSWORD=ContrasenyaSegura123" \
           -p 1444:1444 \
           --name sqlserver2019 \
           -d rapidfort/microsoft-sql-server-2019-ib:latest
```
6. Connexió a la base de dades
Per connectar-nos a SQL Server utilitzem Azure Data Studio
(Descarregar: learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio)

Informació de connexió:

Server: localhost, 127.0.0.1 o IP de la màquina

Port: 1433 o el personalitzat

Authentication: SQL Login

Login: sa

Password: la definida a la instal·lació

Aquí va (connexio-config.jpg)
Aquí va (connexio-ok.jpg)
Aquí va (consulta-sql.jpg)





