# Project team 5 with Boolean
## Installation / Introduction
1. Install the repository on your PC.
2. Open your folder in an editor of your choice (we'll use Visual Studio Code as an example)
3. Open your terminal and type this command: ``` npm install ```
4. Once the installation has finished loading, type this command to send the project via a server to a local link that you will take and open on your favorite search engine: ```npm run dev```
5. Don't forget to enjoy the experience of discovering not only the visual part but also the implementation of the code!!

Have fun!!

## Le tecnologie utilizzate
- HTML v5
- CSS 
- sass v1.79.3 : ```npm i sass```
- Vue v3.4.37
- Bookshops:
  - wow.js v1.2.2 : ```npm i wow.js```
  - bootstrap v5.3.3 :  ```npm i bootstrap```
  - bootstrap-icons v1.11.3 : ```npm i bootstrap-icons```
  - animate.css v4.1.1 : ```npm i animate.css```
- Build Tool: 
    - Vite v5.4.1 : ```create vite@latest```

## Description
The project has been divided into components. Below we will show you the entire structure step by step with explanations of each component.

# AppVue
It is the main component of the project, here we focus on implementing its 3 underlying components and focus on the reasoning of the animations on the general CSS.

Inside we have 4 components:
- AppHeader : is intended to enclose its components (it is fully responsive) which are divided into <br>
    - AppHeaderNavbar : there is a dynamic cart which, with a click, allows you to open it and, if there are any items, to delete them. <br>On the navbar links there is a hover effect for the color and for opening the drop-down menu. <br> With a click you have the possibility to change them whenever new pages are connected. <br>
    The navbar has the same background as the header but when scrolling the page it goes to fixed position and will have a different background color and also presents a "fadeInDown" animation.
    - AppHeaderSection : there is the generic description of the page. There are two images both positioned via position.

- AppMain : it also contains its components:
    - AppMainFeatureMakeYourMark : in this section there is a representation of the various offers there are, it is divided into two parts where the left part has an image in absolute position of a gamer and on the right part the entire description of the offers. <br>
    There are two components:
      - AppMainFeatureMakeYourMarkCardList: contains the reasoning carried out on its internal component on the representation of offers
        - AppMainFeatureMakeYourMarkCardListItem : has the function of dynamically representing each individual offer
    - AppMainFeatureBattle: represents the current clashes that will occur soon, is divided into two components:
      - FeatureBattleCardList: contains the reasoning carried out on its internal component on the representation of the matches
      - BattleCardListItem:It has the function of dynamically representing every single match
    - AppMainFeatureFacts: presents current statistics in the world of E-Sports, is divided into 2 components:
      - FeatureFactsCardList: contains the reasoning carried out on its internal component on the representation of statistics
      - BattleCardListItem : it has the function of dynamically representing each single statistic and there is a method on the scroll where every time the section is present in the viewport the statistics will be updated randomly
    - AppMainFeatureStreaming : allows you to see a preview of a stream and is organized with an image and a generic component positioned in absolute
    - AppMainFeatureFeedback: contains all the reviews and is divided into three components:
      - ProfileCard: it is a specific component that is responsible for implementing people's profiles in a dynamic way.
      - FeatureFeedbackSlider: takes care of implementing the logical basis on which the review card will then be represented
        - FeatureFeedbackSliderCard: dynamically fill out the card
    - AppMainFeatureBanner :shows the currently active banner
    - AppmainFeatureNews : it is a graphic representation of the news via card and is divided into two components:
      - FeatureNewsList : contains the reasoning carried out on its internal component on the representation of news and the most popular main news
      - FeatureNewsListCard: has the function of dynamically representing every single lateral news

- AppFooter : gives the possibility of accessing different links that lead to the respective pages, it is divided into three components:
  - AppFooterNewsLetter: it is in relative position between the FeatureNews and the footer and allows you to register for the site's newsletter.
  - AppFooterColList : divides the footer structure into multiple columns based on the titles and contains its single column component where it dynamically fills each column.
  - AppFooterCopyright :copyright section.
- AppLoader : a specific component for dummy loading of the home page

## Base components
The components reused by all or almost all the sections are 3:
- BaseButton: a button present in many parts of the project and has a condition to check whether the arrows are present or not.
- BaseSectionTitle: the generic title of each section of the main and header
- PlayButton :a generic button with the play symbol

# CREDITI

- Paolo Orazi Front-End
- Melvin Jerome Maligaya Front-End
- Tommaso Panarotto Front-End
- Orsol Filaj Front-End