# Project team 5 with Boolean
## Installazione / Introduzione
1. Installare la repository sul vostro pc.
2. Aprite la vostra cartella in un editor che preferite (faremo l'esempio con Visual Studio Code)
3. Aprite il vostro terminale e digitate questo comando: ``` npm install ```
4. Finito il caricamento dell'installazione, digitate questo comando per far andare il progetto tramite un server in un link locale che prenderete e lo aprirete sul vostro motore di ricerca preferito: ```npm run dev```
5. Non scordatevi di godere dell'esperienza di scoprire non solo la parte visiva ma anche l'implementazione del codice!!

Buon divertimento!!

## Le tecnologie utilizzate
- HTML v5
- CSS 
- sass v1.79.3 : ```npm i sass```
- Vue v3.4.37
- Librerie:
  - wow.js v1.2.2 : ```npm i wow.js```
  - bootstrap v5.3.3 :  ```npm i bootstrap```
  - bootstrap-icons v1.11.3 : ```npm i bootstrap-icons```
  - animate.css v4.1.1 : ```npm i animate.css```
- Strumento di compilazione: 
    - Vite v5.4.1 : ```create vite@latest```

## Description
Il progetto è stato suddiviso in componenti qui sotto vi illustreremo passo passo tutta la struttura con le spiegazioni di ogni componente.

# AppVue
E' il componente principale del progetto, qui ci si concentra sull'implementare i suoi 3 componenti sottostanti e ci si sofferma sul ragionamento delle animazioni sul CSS generale.

Al suo interno abbiamo 4 componenti:
- AppHeader : ha lo scopo di racchiudere i suoi componenti (è completamente responsive) che sono suddivisi in <br>
    - AppHeaderNavbar : vi è un carrello dinamico che tramite un click permette di aprirlo e qualora presenti degli elementi di eliminarli. <br> Sui link della navbar è presente un effetto di hover per il colore e per l'apertura del menù a tendina. <br> Al click si ha la possibilà qual'ora si collegassero nuove pagine di cambiarle. <br>
    La navbar presenta lo stesso sfondo dell'header ma allo scrollo della pagina va in posizione fixed ed avrà un background color diverso inoltre presenta un animazione di "fadeInDown".
    - AppHeaderSection : vi è la descrizione generica della pagina. Vi sono due immagini entrambe posizionate tramite position.

- AppMain : anche lui contiene i suoi componenti:
    - AppMainFeatureMakeYourMark : in questa sezione vi è una rappresentazione delle varie offerte che vi sono, è suddiviso in due parti dove la parte sinistra abbiamo un immagine in position absolute di un gamer e nella parte destra tutta la descrizione delle offerte. <br>
    Vi sono due componenti:
      - AppMainFeatureMakeYourMarkCardList: contiene il ragionamento svolto sul suo componente interno sulla rappresentazione delle offerte
        - AppMainFeatureMakeYourMarkCardListItem : ha la funzione di rappresentare in maniera dinamica ogni singola offerta
    - AppMainFeatureBattle: rappresenta gli attuali scontri che avverrano a breve, viene suddiviso in due componenti:
      - FeatureBattleCardList: contiene il ragionamento svolto sul suo componente interno sulla rappresentazione dei match
      - BattleCardListItem: ha la funzione di rappresentare in maniera dinamica ogni singolo match
    - AppMainFeatureFacts: presenta le statistiche attuali nel mondo degli E-Sport, si divide in 2 componenti:
      - FeatureFactsCardList: ontiene il ragionamento svolto sul suo componente interno sulla rappresentazione delle statistiche
      - BattleCardListItem : ha la funzione di rappresentare in maniera dinamica ogni singola statistica e vi è un metodo sullo scroll dove ogni volta che la sezione sarà presente nella viewport saranno aggiornate le statistiche in maniera casuale
    - AppMainFeatureStreaming : permette di vedere un anteprima di una stream ed è organizzata con un immagine e un componente generico posizionato in absolute
    - AppMainFeatureFeedback: contiene l'insieme delle recensioni e viene suddiviso in tre componenti:
      - ProfileCard: è un componente specifico che si occupa di implementare i profili delle persone in maniera dinamica.
      - FeatureFeedbackSlider: si occupa di implementare la base logica su cui poi verrà rappresentata la card della recensione 
        - FeatureFeedbackSliderCard: compila in maniera dinamica la card
    - AppMainFeatureBanner : mostra il banner attivo attualmente
    - AppmainFeatureNews : è una rappresentazione grafica delle news tramite card si suddivide in due componenti:
      - FeatureNewsList : contiene il ragionamento svolto sul suo componente interno sulla rappresentazione delle news e la news principale piu in voga
      - FeatureNewsListCard: ha la funzione di rappresentare in maniera dinamica ogni singola news laterale

- AppFooter : da la possibilità di accedere a diversi link che portano alle rispettive pagine, è suddivisa in tre componenti:
  - AppFooterNewsLetter: è in position relative tra la FeatureNews e il footer e permette di registrarsi alla newsletter del sito.
  - AppFooterColList : suddivide in più colonne la struttura del footer basandosi sui titoli e contiene all interno il suo componente singolo per le colonne dove riempie dinamicamente ogni colonna.
  - AppFooterCopyright : sezione copyright.
- AppLoader : un componente specifico per il caricamento fittizio della pagina iniziale

## Base components
I componenti riutilizzati da tutte o quasi le sezioni sono 3:
- BaseButton: un bottone presente in molte parti del progetto ed ha una condizione per verificare se sono presenti le arrow o meno.
- BaseSectionTitle: il titolo generico di ogni sezione del main e dell'header
- PlayButton : un bottone generico con il simbolo play

# CREDITI

- Paolo Orazi Front-End
- Melvin Jerome Maligaya Front-End
- Tommaso Panarotto Front-End
- Orsol Filaj Front-End