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
   * 3.3 [Softwarová rozhraní ](#33-softwarová-rozhraní)
* 4 [Vlastnosti systému](#4-otevřené-otázky)

## 1. Úvod 
  ### 1.1 Účel
Cílem je vytvoření programu, který bude brát data z internetu (právě ze sránky https://api.nasa.gov/). Data budou ve formě obrázků a klient je bude moc jednoduše vyhledat pomocí programu. Při připojení k internet bude program načítat nejnovější obrázky. Pokud program ztatí připojení k internetyu bude je načítat z paměti.
  ### 1.2 Konvence Dokumentu
Dokument slouží k vymězení vlastností programu, které jsou  vyžadáné zákazníkem, aby nenastaly nedorozumění.
  ### 1.3 Cílová skupina
Program je tvořen pro vášnívce vesmíru, kteří se chtějí kouknout na různé obrázky, které nasa zveřejňuje.
  ### 1.4 Odkazy na ostatní dokumenty
* FS: https://github.com/MajerAdam/Srovn-vacDat/blob/main/FS.md
  ### 1.5 Kontakty
* source dat: https://api.nasa.gov/
* email: majer.ad.2019@skola.ssps
* tel.: +420 606 971 015

## 2. Celkový popis
  ### 2.1 Produkt jako celek
Nejčastější způsob bude pro rychlejší a jednoduší prohlížení obrázku (právě ze sránky https://api.nasa.gov/). Ale program může sloužit k jejich prohlížení i při nestabilním internetu nebo jako uložiště pro tyto obrázky. Program může být použit jako základ načítání dat z internetu pro vytvoření jiného programu na jiné data.
  ### 2.2 Funkce
S ohledem na typ programu, procházení dat, bude jen jeden typ uživatele, který bude mít přístup ke všem vlatostem programu. Nebude proto existovat jíné typy uživatele jako např. admin a jiné.
  ### 2.3 Uživatelské skupiny
Cílem je zhotovení programu, který bude shopen načítat data z internetu dokáže se v nich vyznat a bude si schopen zapamtovat poslodní vyhledané data. Vytvořené tedy bude přehledné menu na vyhledávaní dat, ale i část zobrazující vyhledané data a paměť na tyto data.
  ### 2.4 Provozní prostředí
Program nebude obsahovat:
  * kopletní knihonu při ztrátě internetu.
    * program si bude pamatovat poslední vyhledáné data, při ztrátě internetu, ne celou knihovnu.
  * uložiště na vyhledáná data
    * program si nebude pamatovat a nebudete si možné ukládat předchozí vyhledaná data.   
  * shopnost projíždení bez specifického hledání
    * program bude fungovat na bází hledání specifických dat ne projíždění knihovny.
  * uživatelská nastavení
    * program nebude nějak kastomizovatlný při spuštění programu pokut chcete změnit vizulizaci program k prosm kontaktujte mě a domluvíme se.
  ### 2.5 Uživatelské prostředí
Nebude se klást důraz na:
  * design aplikace 
  * optimalizace kodu
  * rychlost a responzivita
    * program se bude snažit docílit určitých norem, ale nebude se bát je překročit, kvůli funkčnosti.
  ### 2.6 Omezení návrhu a implementace
  
## 3. Celková hrubá archytektura
  ### 3.1 Pracovní tok
Pracovní postup začne při vizuální částí programu, které by měla zabrat nejmíň času, to znamená vytvoření způsobu vložezní žádosti o data a i jeho zobrazení. Pokud tato část bude funkční. Začne se pracovat na propojení s internetem (a právě se sránkou https://api.nasa.gov/). Po spojení se zažne pracovat na spojení vizuální a internetovou částí, které musí být scela funkční a ke konci se teprve začne pracovat na paměti.
  ### 3.2 Hlavní moduly
Aplikace bude jednoduché okno kde si uživatel bude moc vyhledat data. Pokud uživatel vyhledá nějaká data data se mu zobrazí na stejném okně. Uživatel bude muset vyhledat nové informace pro změnu zobrazených informací. 
  ### 3.3 Všechny detaily obrazovky, okna, tisky, chybové zprávy, logování
Hlavní okno a jeho časti budou zhotovení pomocí Windows Presentation Foundation a celý program bude napsaný v jazyce C#
  ### 3.4 Všechny možné toky programu a jejich projevy
Program by měl být ve své věcnosti pouze vyhledání určitýh dat z internetu (právě ze sránky https://api.nasa.gov/), k vyhledaným datům by neměl uživatel ztratit přístup i při ztrátě internetu.
  ### 3.5 Všechny dohodnuté principy
Dohodnuté principy jsou takové že program musí obsahot způsob jak data vyhledat a také způsob jak dat zobrazit. Následně zobrazená data nesmí zmizet při ztrátě k internetu.
## 4. Otevřené otázky
  ### 4.1 Části, na kterých se zatím nedosáhlo shody
Krom částí funkčnosti programu a funkce vyhledávání nebylo projednáno nic konkrétnějšího. Možnosti probgramu zmíněné výše budou ještě diskutovány a popřípadě změny bude tento dokumen tupraven aby korespondoval s myšlenkou a požadavky zákazníka programu
  ### 4.2 Poznámka pro realizaci
Realizace bude náročná, je třeba propojit program s internetem a stránkou ze které má brát data, poté prostředí a způsob pro jednoduché vyhledávání dat, program bude také muset zobrazovat vyhledaná data a na závěr určitá dat neztrácet při odpojení k internetovému připojení
