# Funkční specifikace
## Vyhledávač dat
Verze 1  
Adam Majer 4.C  
SSPŠ  
11.10 2022  

Table of Contents
================
* 1 [Úvod](#1-úvod)
   * 1.1 [Účel](#11-účel)
   * 1.2 [Konvence Dokumentu](#12-konvence-dokumentu)
   * 1.3 [Pro koho je dokument určený](#13-pro-koho-je-dokument-určený)
   * 1.4 [Odkazy na ostatní dokumenty](#14-odkazy-na-ostatní-dokumenty)
   * 1.5 [Kontakty](#15-kontakty)
* 2 [Scénáře](#2-scénáře)
   * 2.1 [Všechny reálné způsoby použití](#21-všechny-reálné-způsoby-použití)
   * 2.2 [Typy uživatelských rolí](#22-typy-uživateských-rolí)
   * 2.3 [Detaily, motivace, příklady](#23-detaily,-motivace,-příklady)
   * 2.4 [Vymezení rozsahu - co v sw Nebude](#24-vymezení-rozsahu,-co-v-sw-Nebude)
   * 2.5 [Na co se nebude klást důraz](#25-na-co-se-nebude-klást-důraz)
* 3 [Celková hrubá architektura](#3-celková-hrubá-architektura)
   * 3.1 [Pracovní tok](#31-pracovní-tok)
   * 3.2 [Hlavní moduly](#32-hlavní-moduly)
   * 3.3 [Všechny detaily: obrazovky, okna, tisky, chybové zprávy, logování](#33-všechny-detaily-obrazovky,-okna,-tisky,-chybové-zprávy,-logování)
   * 3.4 [Všechny možné toky programu a jejich projevy](#34-všechny-možné-toky-programu-a-jejich-projevy)
   * 3.5 [Všechny dohodnuté principy](#35-všechny-dohodnuté-principy)
* 4 [Otevřené otázky](#4-otevřené-otázky)
   * 4.1 [Části, na kterých se zatím nedosáhlo shody](#41-searching)
   * 4.2 [Poznámka pro realizaci](#42-poznámky-pro-realizai) 

## 1. Úvod 
  ### 1.1 Účel
Cílem je vytvoření programu, který bude brát data z internetu (právě ze stránky https://api.nasa.gov/). Data budou ve formě obrázků a klient je bude moc jednoduše vyhledat pomocí programu. Při připojení k internet bude program načítat nejnovější obrázky. Pokud program ztratí připojení k internetu bude je načítat z paměti.
  ### 1.2 Konvence Dokumentu
Dokument slouží k vymezení vlastností programu, které jsou  vyžádané zákazníkem, aby nenastaly nedorozumění.
  ### 1.3 Pro koho je dokument určený
Dokument je určený jak pro tvůrce programu, tak i pro zákazníka. Slouží k vytvoření stejné myšlenky, v obou stranách, to znamená programátora a zákazníka. Budou zde uvedeny informace, jak zhotovený software bude vypadat, čeho bude schopný a čeho schopný nebude. Tento dokument také tvoří základ pro tvorbu práce a je možno na něj odkazovat v případě nespokojenosti.
  ### 1.4 Odkazy na ostatní dokumenty
SRS: https://github.com/MajerAdam/Srovn-vacDat/blob/main/SRS.md
  ### 1.5 Kontakty
* source dat: https://api.nasa.gov/
* email: majer.ad.2019@skola.ssps
* tel.: +420 606 971 015

## 2. Scénáře
  ### 2.1 Všechny reálné způsoby použití
Nejčastější způsob bude pro rychlejší a jednoduší prohlížení obrázku (právě ze stránky https://api.nasa.gov/). Ale program může sloužit k jejich prohlížení i při nestabilním internetu nebo jako uložiště pro tyto obrázky. Program může být použit jako základ načítání dat z internetu pro vytvoření jiného programu na jiná data.
  ### 2.2 Typy uživatelských rolí
S ohledem na typ programu, procházení dat, bude jen jeden typ uživatele, který bude mít přístup ke všem vlatostem programu. Nebudou proto existovat jíný typy uživatele jako např. admin a jiné.
  ### 2.3 Detaily, motivace, příklady
Cílem je zhotovení programu, který bude schopen načítat data z internetu dokáže se v nich vyznat a bude si schopen zapamatovat poslední vyhledané data. Vytvořené tedy bude přehledné menu na vyhledávaná data, ale i část zobrazující vyhledená data a paměť na tato data.
  ### 2.4 Vymezení rozsahu, co v sw Nebude
Program nebude obsahovat:
  * kompletní knihovnu při ztrátě internetu.
    * program si bude pamatovat poslední vyhledaná data, při ztrátě internetu, ne celou knihovnu.
  * uložiště na vyhledaná data
    * program si nebude pamatovat a nebudete si možné ukládat předchozí vyhledaná data.   
  * schopnost projíždění bez specifického hledání
    * program bude fungovat na bází hledání specifických dat ne projíždění knihovny.
  * uživatelská nastavení
    * program nebude nějak kastomizovatlný při spuštění programu pokut chcete změnit vizualizaci program, prosím kontaktujte mě a domluvíme se.
  ### 2.5 Na co se nebude klást důraz
Nebude se klást důraz na:
  * design aplikace 
  * optimalizace kódu
  * rychlost a responzivita
    * program se bude snažit docílit určitých norem, ale nebude se bát je překročit, kvůli funkčnosti.
  
## 3. Celková hrubá architektura
  ### 3.1 Pracovní tok
Pracovní postup začne při vizuální částí programu, které by měla zabrat nejmíň času, to znamená vytvoření způsobu vložení žádosti (search bar) o data a i jeho zobrazení. Pokud tato část bude funkční. Začne se pracovat na propojení s internetem (a právě se sránkou https://api.nasa.gov/). Po spojení se zažne pracovat na spojení vizuální a internetovou částí, které musí být zcela funkční a ke konci se teprve začne pracovat na paměti.

![image](https://user-images.githubusercontent.com/97035550/195087874-1c067e4a-5177-40f7-92bd-862d67ac5e44.png)

  ### 3.2 Hlavní moduly
Aplikace bude jednoduché okno kde si uživatel bude moc vyhledat data. Pokud uživatel vyhledá nějaká data se mu zobrazí na stejném okně. Uživatel bude muset vyhledat nové informace pro změnu zobrazených informací. 

![image](https://user-images.githubusercontent.com/97035550/195100209-540e029d-26c5-4650-8a81-24149c9772fc.png)

  ### 3.3 Všechny detaily obrazovky, okna, tisky, chybové zprávy, logování
Hlavní okno a jeho časti budou zhotovení pomocí Windows Presentation Foundation a celý program bude napsaný v jazyce C#
  ### 3.4 Všechny možné toky programu a jejich projevy
Program by měl být ve své věcnosti pouze vyhledání určitých dat z internetu (právě ze stránky https://api.nasa.gov/), k vyhledaným datům by neměl uživatel ztratit přístup i při ztrátě internetu.
  ### 3.5 Všechny dohodnuté principy
Dohodnuté principy jsou takové že program musí obsahovat způsob jak data vyhledat a také způsob jak dat zobrazit. Následně zobrazená data nesmí zmizet při ztrátě k internetu.
## 4. Otevřené otázky
  ### 4.1 Části, na kterých se zatím nedosáhlo shody
Krom částí funkčnosti programu a funkce vyhledávání nebylo projednáno nic konkrétnějšího. Možnosti programu zmíněné výše budou ještě diskutovány a popřípadě změny bude tento dokument upraven aby korespondoval s myšlenkou a požadavky zákazníka programu
  ### 4.2 Poznámka pro realizaci
Realizace bude náročná, je třeba propojit program s internetem a stránkou ze které má brát data, poté prostředí a způsob pro jednoduché vyhledávání dat, program bude také muset zobrazovat vyhledaná data a na závěr určitá dat neztrácet při odpojení k internetovému připojení
