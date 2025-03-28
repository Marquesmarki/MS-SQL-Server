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

🔧 El **suport oficial** és proporcionat per **Microsoft**, tant per la versió local com les del núvol (*Azure SQL*).

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



4.A on es troben físicament els fitxers de dades (per defecte). Com ho has sabut?

5.El servei de SGBD escollit en quins ports escolta. Quina modificació/passos caldrien fer per canviar aquest port a un altre per exemple? Important: No realitzis els canvis. Només indica els passos que faries.

6.Incloure en la documentació un petit apartat a on s'expliqui com realitzar la connexió a la BD. Demostra que us podeu connectar al SGBD a través d’una eina de gestió de BD o  a través d’un programa.

