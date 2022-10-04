# Software Requirements Specification
## Srvnávač dat
Verze 1  
Adam Majer 4.C  
SSPŠ  
4-th of October 2022  

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
* 3 [Celková hrubá archytektura](#3-celková-hrubá-archytektura)
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
Cílem je vytvoření programu, který bude brát data z internetu (právě ze sránky https://api.nasa.gov/). Data budou ve formě obrázků a budou klient je bude moc jednoduše vyhledat pomocí programu. Při připojení k internet bude program načítat nejnovější obrázky. Pokud program ztatí připojení k internety bude je načítat z paměti.
  ### 1.2 Konvence Dokumentu
Dokument slouží k vymězení vlastností programu, které jsou  vyžadáné zákazníkem, aby nenastaly nedorozumění.
  ### 1.3 Pro koho je dokument určený
Dokument je určený jak pro tvůrce programu tak i pro zákazníka. Slouži k vytvoření stejné myšlenky, v obou stranách, to znamená programátora a zákazníka. Budou zde uvedeny informace, jak zhotovený sofware bude vypadat, čeho bude schopný a čeho schopný nebude. Tento dokument také tvoří základ pro tvorbu práce a je možno na něj odkazovat v případě nespokojenosti.
  ### 1.4 Odkazy na ostatní dokumenty
V tuto chvíli nejsou vytvořeni žádné jiné dokumenty a proto na ně není možno odkazovat. Hned jak budou vytvořeni tento doukument bude zhotovena novější verze.
  ### 1.5 Kontakty
* source dat: https://api.nasa.gov/
* email: majer.ad.2019@skola.ssps
* tel.: +420 606 971 015

## 2. Scénáře
  ### 2.1 Všechny reálné způsoby použití
Nejčastější způsob bude pro rychlejší a jednoduší prohlížení obrázku (právě ze sránky https://api.nasa.gov/). Ale program může sloužit k jejich prohlížení i při nestabilním internetu nebo jako uložiště pro tyto obrázky. Program může být použit jako základ načítání dat z internetu pro vytvoření jiného program na jiné data.
  ### 2.2 Typy uživatelských rolí
S ohledem na typ programu, procházení dat, bude jen jeden ty uživatele který bude mýt přístup ke všem vlatostem programu. Nebude proto existovat jí typy jako např. admin a jiné.
  ### 2.3 Detaily, motivace, příklady
Cílem je zhotovení programu, který bude shopen načítat data z internetu dokáže se v nich vyznat a bude si schopen zapamtovat poslodní vyhledané data. Vytvořené tedy bude přehledné menu na vyhledávaní dat, ale i část zobrazující vyhledané data a paměť na tyto data.
  ### 2.4 Vymezení rozsahu, co v sw Nebude
  
  ### 2.5 Na co se nebude klást důraz
  
## 3. Celková hrubá archytektura
  ### 3.1 Pracovní tok

  ### 3.2 Hlavní moduly

  ### 3.3 Všechny detaily obrazovky, okna, tisky, chybové zprávy, logování
  
  ### 3.4 Všechny možné toky programu a jejich projevy
  
  ### 3.5 Všechny dohodnuté principy

## 4. Otevřené otázky
  ### 4.1 Části, na kterých se zatím nedosáhlo shody
  
  ### 4.2 Poznámka pro realizaci
