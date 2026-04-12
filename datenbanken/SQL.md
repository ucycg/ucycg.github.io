---
layout: default
---

# SQL Befehle für die AP1 Prüfung

## Verschiedene Varianten von SELECT

SELECT Name, Anschaffungspreis
FROM Equipemnt
WHERE Typ = 'Hardware'
ORDER BY Anschaffungspreis DESC;

oder mit LIKE

SELECT Name, Anschaffungspreis
FROM Equipemnt
WHERE Name LIKE 'M%'
ORDER BY Anschaffungspreis DESC;

## UPDATE

Update Equipment
SET
    Name = 'Patch Antenne V2',      -- hier steht der Name der Spalte die man updaten möchte!
    Anschaffungspreis = 100.0
WHERE ID = 1;

## INSERT

INSERT INTO Equipment (ID, Name, Typ, Anschaffungspreis) VALUES (1, 'MHF4 Antenne', 'Hardware', 15.50)

## DELETE

DELETE
FROM Equipement
WHERE ID = 1;

## CREATE TABLE - Data Definition Language (DDL)

Erst der Parent

CREATE TABLE Kategorie (
    KatID INTEGER PRIMARY KEY,
    Bezeichnung VARCHAR(50)
);

Dann das Child

CREATE TABLE Equipment(
    eID INT AUTO INCREMENT PRIMARY KEY,
    Name VARCHAR(100),
    Typ VARCHAR(50),
    Anschaffungspreis DECIMAL(10,2)

    FOREIGN KEY (KatID) REFERENCES Kategorie(KatID)
    ON UPDATE CASCADE
    ON DELETE RESTRICT
);
