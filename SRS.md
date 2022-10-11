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
   * 1.3 [Cílová skupina ](#13-cílová-skupina )
   * 1.4 [Odkazy na ostatní dokumenty](#14-odkazy-na-ostatní-dokumenty)
   * 1.5 [Kontakty](#15-kontakty)
* 2 [2.	Celkový popis](#2-celkový-popis)
   * 2.1 [Produkt jako celek ](#21-produkt-jako-celek)
   * 2.2 [Funkce](#22-funkce)
   * 2.3 [Uživatelské skupiny](#23-uživatelské-skupiny)
   * 2.4 [Provozní prostředí ](#23-provozní-prostředí)
   * 2.5 [Uživatelské prostředí ](#24-uživatelské-prostředí)
   * 2.6 [Omezení návrhu a implementace](#25-omezení-návrhu-a-implementace)
* 3 [Požadavky na rozhraní](#3-požadavky-na-rozhraní)
   * 3.1 [Uživatelská rozhraní](#31-uživatelská-rozhraní)
   * 3.2 [Hardwarová rozhraní](#32-hardwarová-rozhraní)
   * 3.3 [Softwarová rozhraní ](#33-softwarová-rozhraní)
* 4 [Vlastnosti systému](#4-otevřené-otázky)
   * 4.1 [Části, na kterých se zatím nedosáhlo shody](#41-searching)
   * 4.2 [Poznámka pro realizaci](#42-poznámky-pro-realizai) 

## 1. Úvod 
  ### 1.1 Účel
Cílem je vytvoření programu, který bude brát data z internetu (právě ze sránky https://api.nasa.gov/). Data budou ve formě obrázků a klient je bude moc jednoduše vyhledat pomocí programu. Při připojení k internet bude program načítat nejnovější obrázky. Pokud program ztatí připojení k internetyu bude je načítat z paměti.
  ### 1.2 Konvence Dokumentu
Dokument slouží k vymězení vlastností programu, které jsou  vyžadáné zákazníkem, aby nenastaly nedorozumění.
  ### 1.3 Pro koho je dokument určený
Dokument je určený jak pro tvůrce programu tak i pro zákazníka. Slouží k vytvoření stejné myšlenky, v obou stranách, to znamená programátora a zákazníka. Budou zde uvedeny informace, jak zhotovený sofware bude vypadat, čeho bude schopný a čeho schopný nebude. Tento dokument také tvoří základ pro tvorbu práce a je možno na něj odkazovat v případě nespokojenosti.
  ### 1.4 Odkazy na ostatní dokumenty

  ### 1.5 Kontakty
* source dat: https://api.nasa.gov/
* email: majer.ad.2019@skola.ssps
* tel.: +420 606 971 015
