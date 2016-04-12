---
layout: post
title: Skapa flera kort i Trello med Drafts 
categories: Genomgångar
tags: Trello Drafts iOS Automatisering
image: http://www.appleyra.se/wp-content/uploads/2016/03/Trello-Drafts-banner.jpeg
---

*Jag använder Trello både i jobbet och på Appleyra. Jag gillar översikten som Trello ger och jag kan snabbt se vart olika inlägg är i processen. Tidigare använde jag 2Do men hade svårt att se vad som skulle göras och vilka inlägg som borde skrivas. Det första jag märkte att jag saknade i Trello var möjligheten att snabbt skriva in nya idéer.*


## Inledning

Jag använder fortfarande 2Do som min att-göra-lista, men har flyttat alla inlägg för Appleyra till Trello. Trello har bra stöd för URL-schema men också ett API som gör att andra appar och tjänster kan kommunicera. Dessutom finns Trello på [IFTTT](https://ifttt.com) som ger ytterligare möjligheter [^2]. 

[^2]: Jag jobbar på ett inlägg om detta som snart kommer på Appleyra. 

När jag får en idé, oavsett vad det gäller så öppnar jag alltid Drafts. Så det var logiskt för mig att började leta efter en lösning som utgick därifrån. Det första jag gjorde var att leta efter färdiga åtgärder i [Drafts bibliotek](http://drafts4-actions.agiletortoise.com/), och hittade snart [denna åtgärd](http://drafts4-actions.agiletortoise.com/a/1im)[^3]. Den går igenom din text och skapar ett kort för varje rad. Det var precis vad jag behövde men det krävdes lite konfigurering innan den fungerade. 

[^3]: Den är skriven av Jesper som skriver på Appleyra. 


## Hitta shortlink

Först måste vi hitta något som kallas `shortlink` för att berätta vilken tavla kortet ska hamna i. Kortet kommer att hamna i listan längst till vänster, om du vill att den ska hamna i en specifik lista måste du hitta ett `list_id` som är betydligt krångligare [^1]. 

[^1]: Kanske skriver om detta vid ett senare tillfälle om det finns intresse. Eller kontakta mig via mail eller Twitter. 

För att hitta länken till den tavlan du vill använda måste du logga in på Trello i Safari. Det går inte att använda iOS appen till detta. När allt är klart så kommer dock appen att användas. När du loggar in på Trello så navigerar du till tavlan och öppnar den. Sen ställer du dig i adressfältet och kopierar texten som innehåller 8 tecken. För mig ligger den efter en enkel bokstav och innan namnet på tavlan. 

Efter det öppnar du Drafts och klistrar in det du kopierade. Det ska in efter `shortlink=`. Början på länken ska då se ut såhär 

`trello://x-callback-url/createCard?name=[[line|1]]&shortlink=f5aYQpin...`

![Skapa action set](http://i2.wp.com/www.appleyra.se/wp-content/uploads/2016/03/Skapa-action-set.jpeg)

## Flera tavlor

Åtgärden är nu fullt fungerande men de flesta som använder Trello misstänker jag har mer än en tavla. Då måste du skapa en åtgärd för varje tavla på samma sätt som ovan. Det blir lätt många åtgärder men dessa kan grupperas med något som kallas [action sets](https://nahumck.me/using-action-sets-drafts/). Det innebär att du skapar en åtgärd med genvägar till de övriga. Valet görs via en meny som vi skapar med en funktion som heter `[[prompt_button]]`. Börja med att skapa en ny åtgärd och ge den ett namn. Därefter lägger du till första steget som är en Prompt. Bläddra ner tills du hittar sektionen **Buttons**. Där fyller du i namnet på dina åtgärder till de olika tavlorna. Namnen skiljs med `|` och det är viktigt att du skriver exakt samma, annars fungerar det inte. Efter det lägger du till ett nytt steg i form av en URL. Den länken du ska använda är: 

`drafts4://x-callback-url/runAction?action=[[prompt_button]]&text=[[draft]]&allowEmpty=YES`

Den kör den åtgärden som du väljer i menyn, vilket resulterar i att texten läggs in i den tavlan på Trello. Har du flera rader kommer det hoppa mellan Trello och Drafts tills alla raderna lagts till. 

För att detta ska fungera behöver du ha ett konto på [Trello](https://trello.com/) och ladda ner följande appar. 

**[Trello](https://itunes.apple.com/se/app/trello/id461504587?mt=8&uo=4&at=10lKZy&ct=twitter) är en universal-app som finns att hämta på App Store [Gratis]**

**[Drafts 4 - Quickly Capture Notes, Share Anywhere!](https://itunes.apple.com/se/app/drafts-4-quickly-capture-notes/id905337691?mt=8&uo=4&at=10lKZy&ct=twitter) är en universal-app som finns att hämta på App Store [109 kr]**
