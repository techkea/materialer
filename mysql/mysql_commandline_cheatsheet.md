
# MySQL Kommandolinje Cheatsheet
## Forbindelse til MySQL

- **Forbind til MySQL Server:**
  ```sh
  mysql -u brugernavn -p
  ```
  - `-u brugernavn`: Angiver MySQL-brugernavnet.
  - `-p`: Beder om adgangskoden.

- **Forbind til en Specifik Database:**
  ```sh
  mysql -u brugernavn -p databasenavn
  ```

## Databaseoperationer

- **Opret en Database:**
  ```sql
  CREATE DATABASE databasenavn;
  ```

- **Slet en Database:**
  ```sql
  DROP DATABASE databasenavn;
  ```

- **Vælg en Database:**
  ```sql
  USE databasenavn;
  ```

- **Vis Alle Databaser:**
  ```sql
  SHOW DATABASES;
  ```

## Tabeloperationer

- **Opret en Tabel:**
  ```sql
  CREATE TABLE tablenavn (
      kolonne1 datatype,
      kolonne2 datatype,
      ...
  );
  ```

- **Slet en Tabel:**
  ```sql
  DROP TABLE tablenavn;
  ```

- **Beskriv en Tabel:**
  ```sql
  DESCRIBE tablenavn;
  ```

- **Vis Alle Tabeller i den Aktuelle Database:**
  ```sql
  SHOW TABLES;
  ```

## Datamanipulation

- **Indsæt Data i en Tabel:**
  ```sql
  INSERT INTO tablenavn (kolonne1, kolonne2, ...) VALUES (værdi1, værdi2, ...);
  ```

- **Opdater Data i en Tabel:**
  ```sql
  UPDATE tablenavn SET kolonne1 = værdi1, kolonne2 = værdi2, ... WHERE betingelse;
  ```

- **Slet Data fra en Tabel:**
  ```sql
  DELETE FROM tablenavn WHERE betingelse;
  ```

- **Vælg Data fra en Tabel:**
  ```sql
  SELECT kolonne1, kolonne2, ... FROM tablenavn WHERE betingelse;
  ```

## Brugeradministration

- **Opret en Ny Bruger:**
  ```sql
  CREATE USER 'brugernavn'@'host' IDENTIFIED BY 'adgangskode';
  ```

- **Giv Rettigheder til en Bruger:**
  ```sql
  GRANT rettighed ON databasenavn.tablenavn TO 'brugernavn'@'host';
  ```

- **Fjern Rettigheder fra en Bruger:**
  ```sql
  REVOKE rettighed ON databasenavn.tablenavn FROM 'brugernavn'@'host';
  ```

- **Slet en Bruger:**
  ```sql
  DROP USER 'brugernavn'@'host';
  ```

## Sikkerhedskopiering og Gendannelse

- **Sikkerhedskopier en Database:**
  ```sh
  mysqldump -u brugernavn -p databasenavn > sikkerhedskopi.sql
  ```

- **Gendan en Database:**
  ```sh
  mysql -u brugernavn -p databasenavn < sikkerhedskopi.sql
  ```

## Diverse

- **Vis Aktuel Bruger:**
  ```sql
  SELECT USER();
  ```

- **Vis Aktuel Database:**
  ```sql
  SELECT DATABASE();
  ```

- **Afslut MySQL:**
  ```sql
  EXIT;
  ```
