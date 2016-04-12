---
layout: post
title: Skicka påminnelser från Trello till 2Do
date: 2016-04-03
image: ![IFTTT Trello till Reminders](http://www.appleyra.se/wp-content/uploads/2016/04/IFTTT-Trello-till-Reminders.jpg)
---


*Som jag nämnde i ett [tidigare inlägg så använder jag Trello](http://www.appleyra.se/genomgangar/skapa-flera-kort-i-trello-med-drafts/) för att organisera Appleyra. Men samtidigt använder jag 2Do för alla andra uppgifter jag ska göra privat. För att saker inte ska falla mellan stolarna så har jag automatiserat så att alla kort som  jag sätter mitt namn på i Trello  hamnar i min inkorg i 2Do med en länk tillbaka till det kortet.*

För att detta ska fungera behöver du ett konto på IFTTT.com, ett konto på [Trello](https://trello.com/ "Trello") samt använda dig av Apples Påminnelser som synkroniseringsmetod i 2Do. Använder du inte 2Do så fungerar det även i alla appar som använder sig av Påminnelser. 

## IFTTT

IFTTT står för *If This Than That* och är en kostnadsfri webbtjänst som knyter ihop massa olika appar och tjänster. Det gör att du på ett ganska smidigt sätt kan flytta information mellan tjänster som egentligen inte pratar med varandra. Börja med att [ladda ner appen till iOS](https://itunes.apple.com/se/app/if-by-ifttt/id660944635?mt=8&uo=4&at=10lKZy&ct=twitter) och skapa ett konto. Väl inne i appen knackar du på knappen Browse i övre hörnet. Då kommer du till ett läge för att hantera dina recept.[^1] Nästa steg är att knacka på det stora **+** för att skapa receptet. Nu startas en guide som hjälper dig. Tryck på det första blåa **+** och leta upp Trello. Innan du kan lägga till en kanal så måste den aktiveras, detta behöver bara göras en gång. Som Trigger väljer du **Card assigned to me** och sen vilken tavla i Trello det gäller. Nästa steg är att aktivera Påminnelser och välja vilken lista uppgiften ska hamna i. Detta gör du genom att knacka på det röda **+**. 

Här kan du välja en titel på din påminnelse och vilken lista den ska hamna i. Jag har valt att det ska hamna i min inkorg så jag kan hantera den i min morgongenomgång. Du kan kombinera egen text med taggar som finns inbyggda i IFTTT. Här lägger jag till en text innan och sen vill jag ha titel på kortet i Trello samt länk till kortet. När du är nöjd sparar du och det är klart. 

![Konfiguration av Reminders](http://www.appleyra.se/wp-content/uploads/2016/04/Konfiguration-av-Reminders.jpg)

## 2Do

När uppgiften dyker upp i min inkorg klipper jag ut länken till kortet i Trello och lägger in det som en URL-action. Jag sätter också ett förfallodatum och flyttar den till rätt lista. Genom att jag har länken som en åtgärd kan jag enkelt knacka på den och kortet öppnas i Trello-appen. Detta är riktigt smidigt eftersom jag har all information och eventuella länkar samlade där. När uppgiften är slutförd markerar jag den som klar i 2Do och i Trello flyttar jag det till listan publicerade och tar bort mig från kortet. Använder du dig av Påminnelser finns det inget stöd för att lägga till länkar, även om du klistrar in länken som en anteckning så är den inte klickbar. 

## Sammanfattning

Jag tycker detta är ett smidigt sätt för mig att få de bästa av två världar. Trello ger mig översikten och möjligheten att samarbeta och 2Do ser till att det blir gjort. Det kan ibland ta en stund innan uppgiften dyker upp i inkorgen. Detta beror på att IFTTT kollar dina recept i intervaller och har du precis missat en koll får du vänta på nästa. 

För att detta ska fungera behöver du ladda ner följande appar:

**[IF by IFTTT](https://itunes.apple.com/se/app/if-by-ifttt/id660944635?mt=8&uo=4&at=10lKZy&ct=twitter) är en universal-app som finns att hämta på App Store [Gratis]**

**[Trello](https://itunes.apple.com/se/app/trello/id461504587?mt=8&uo=4&at=10lKZy&ct=appleyra) är en universal-app som finns att hämta på App Store [Gratis]**

**[2Do](https://itunes.apple.com/se/app/2do/id303656546?mt=8&uo=4&at=10lKZy&ct=appleyra) är en universal-app som finns att hämta på App Store [159 kr]**

[^1]: Varje länk du skapar mellan olika tjänster kallas recept.
