# Specifikace požadavků
## Vyhlelávač dat
Verze 2  
Adam Majer 4.C  
SSPŠ  
11.10 2022  
změna: Přepsání většiny dokumentu aby se nepodoba FS.

Table of Contents
================
* 1 [Úvod](#1-úvod)
   * 1.1 [Účel](#11-účel)
   * 1.2 [Konvence Dokumentu](#12-konvence-dokumentu)
   * 1.3 [Cílová skupina](#13-cílová-skupina)
   * 1.4 [Odkazy na ostatní dokumenty](#14-odkazy-na-ostatní-dokumenty)
   * 1.5 [Kontakty](#15-kontakty)
* 2 [Celkový popis](#2-celkový-popis)
   * 2.1 [Produkt jako celek](#21-produkt-jako-celek)
   * 2.2 [Funkce](#22-funkce)
   * 2.3 [Uživatelské skupiny](#23-uživatelské-skupiny)
   * 2.4 [Provozní prostředí](#23-provozní-prostředí)
   * 2.5 [Uživatelské prostředí](#24-uživatelské-prostředí)
   * 2.6 [Omezení návrhu a implementace](#25-omezení-návrhu-a-implementace)
* 3 [Požadavky na rozhraní](#3-požadavky-na-rozhraní)
   * 3.1 [Uživatelská rozhraní](#31-uživatelská-rozhraní)
   * 3.2 [Hardwarová rozhraní](#32-hardwarová-rozhraní)
   * 3.3 [Softwarová rozhraní](#33-softwarová-rozhraní)
* 4 [Vlastnosti systému](#4-vlastnosti-systému)
   * 4.1 [Vlastnost A](#31-vlastnost-A)
   * 4.2 [Vlastnost B](#31-vlastnost-B)
   * 4.3 [Vlastnost C](#31-vlastnost-C)

## 1. Úvod 
  ### 1.1 Účel
Cílem je vytvoření programu, který bude brát data z internetu (právě ze sránky https://api.nasa.gov/). Data budou ve formě obrázků a klient je bude moc jednoduše vyhledat pomocí programu. Při připojení k internet bude program načítat nejnovější obrázky. Pokud program ztatí připojení k internetyu bude je načítat z paměti.
  ### 1.2 Konvence Dokumentu
Dokument slouží k vymězení vlastností programu, které jsou  vyžadáné zákazníkem, aby nenastaly nedorozumění mezi zákazníkem a programátorem. 
  ### 1.3 Cílová skupina
Program je tvořen pro vášnívce vesmíru, kteří se chtějí kouknout na různé obrázky, které nasa zveřejňuje. Pro lidi co mají nějaký ponětí co po programu budeou chtít, pokud člověk nebude mít alespoň tušení po čem touží při používání aplikace, pravděpodobně bude sklamán
  ### 1.4 Odkazy na ostatní dokumenty
* FS: https://github.com/MajerAdam/Srovn-vacDat/blob/main/FS.md
  ### 1.5 Kontakty
  
* source dat: https://api.nasa.gov/
* email: majer.ad.2019@skola.ssps
* tel.: +420 606 971 015

## 2. Celkový popis
  ### 2.1 Produkt jako celek
  Product bude bude WPF aplikace. 
  ### 2.2 Funkce
  Aplikace bude mít search bar pomocí, kterého se profiltruje datábáze a poté se podle toho najde list možností, ze kterých si budete moci vybrat. Dota se poté budou     ukazovat a uživatel je bude muc zaměňovat pomocí vybírání si v listu. 
  ### 2.3 Uživatelské skupiny
  Není potřeba rozděli uživatele do skupin, všichni budou mít stejná opravnění. Uživatel bude mít pístup ke všem funkčnostím aplikace.
  ### 2.4 Provozní prostředí
  PC zatím, možná expanze na mobilní platformy. První se bude prioritizovat funkčnost na PC.
  ### 2.5 Uživatelské prostředí
  Windows presentation foundation
  ### 2.6 Omezení návrhu a implementace
  Pro funkci programu bude za potřeba pipojení k internetu a malé využití CPI. Zárověň taky bude zaujímat malou část paměti.
## 3. Požadavky na rozhraní
  ### 3.1 Uživatelská rozhraní
  Provozní prostředí se bude odehrávet všechno na jednom panelu. Na něm bude serchbar, otevřou se tam obrázky a i se tam bude ukazovat list možností provýběr z dat.
  ### 3.2 Hardwarová rozhraní
  N/A
  ### 3.3 Softwarová rozhraní 
  N/A
## 4. Vlastnosti systému
  ### 4.1 Search bar 
  Pomicí něj se budou vyhledávat data, který si bude zákazník chtít zobrazit. Měl by být schopen přijmout i nedokončené informace a být schopen najít list možností pro   aplikaci.
  ### 4.2 List
  Pokud je Search bar prázný list bude schovaný. V tu chvíly co se něco napíše do něj něco napíše. List se zviditelní a ukáže možnosti ze kterých si pak můžeme vybrat   a rozhodnout se jaký znich si chceme prohlédnout
  ### 4.2 View
  Když je z dat vybranná image. Imige se zobrazí pro naše prohlidnutí. Tuto image budeme moc kdikoli změnit pokud klikneme na jíná data v listu.

