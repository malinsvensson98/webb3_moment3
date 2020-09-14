# Webbutveckling 3 - moment 2

#### 1. Vad är syftet med automatiserings-processen? 

Syftet är att skapa en snabbare utvecklingsprocess.
Autiomatiserings-processen bidrar till att filstorlekarna blir mindre, bilderna optimeras och allt samlas tillsammans i en publicerings-katalog utan att utvecklaren behöver genomföra dessa stegen manuellt. Således blir utvecklingen både mer effektiv men även mindre upprepande då delar som utvecklaren annars skulle gjort själv körs automatiskt. Dessutom så blir slutresultatet, det vill säga webbplatsen snabbare då alla filer minifieras. 

***

 #### 2. Vilka paket och verktyg har du använt och varför? 
Jag har använt paket för att minifiera filer, optimera bilder, för att konkantinera filer samt för att hålla min 
webbplats uppdaterad automatiskt då förändringar sker. De paket jag använt är följande: 

```
• "browser-sync": Öppnar en lokal webbserver där webbplatsen som skapas speglas och hela tiden uppdateras då utvecklaren gör förändringar i filerna. Live-reload.
• "gulp": Systemet, det vill säga grunden av automatiseringen. Genom detta använder jag alla följande verktyg. 
• "gulp-clean-css": Minifierar mina css-filer.
• "gulp-concat": Konkantenerar mina JS-filer.
• "gulp-concat-css": Konkantenerar CSS-filerna.
• "gulp-imagemin": Optimerar bilderna.
• "gulp-uglify-es": Minifierar JS-filerna.
```

Då jag valde de olika paketen så kollade jag dels på hur många som laddat ned dem varje vecka, detta för att se så att det är paket som många troligtvis gillar. Dessutom kollade jag även på hur längesedan det var paketen skapades för att veta så att jag använder verktyg som ej gått ur tiden. 
Tillsist så kollade jag igenom hur paketen används för att säkerställa att jag förstod hur jag på rätt sätt skulle implementera dessa för att få ett fungerande och sammanhängande system. 
***

#### 3. Beskriv systemet du skapat, hur man startar upp det och de tasks som ingår. 
*För att använda dig av systemet behöver du ha node.js samt npm installerat på datorn* 

För att använda det skapade systemet börjar användaren med att öppna upp terminalen fristående eller genom tillexempel visual studio code. Navigera dig sedan fram till platsen som du vill spara mappen med systemet i, tillexempel skrivbord (desktop). 
```
cd desktop 
```
Därefter används följande kommando för att hämta system-mappen
```
git clone https://github.com/malinsvensson98/Webb3_moment2.git 
```
Användaren har efter detta laddat ned filerna från GitHub och kan därefter öppna upp dessa i valfri kodeditor, tillexempel det tidigare nämnda vsc. 
För att sedan installera alla paket som krävs för att systemet ska fungera så används följande: 
```
npm install 
```
Då dessa är installerade kan användaren starta systemet genom att skriva:
```
gulp 
```
Det som sker då kommandot används är att en ny mapp vid namn "pub" skapas. 
Denna mappen är till för att innehålla alla "färdiga" filer som sedan ska laddas upp. 
Till mappen flyttas alla skapade html-filer, bilder, css-filer samt JavaScript-filer och innan dem hamnar där går dem igenom en process där allting minimeras/optimeras och om det finns flera filer, tillexempel två skilda css-filer så slås dem samman. 

Systemet innehåller även den tidigare nämnda "watcher" som hela tiden håller koll på om förändringar görs. Detta innebär att utvecklaren kan justera filerna som ligger i "src-mappen", det vill säga filer under redigering och under tiden utvecklaren gör detta så överförs även justeringarna till pub-mappen. 
Med hjälp av browser-sync så genomförs en live-reload vilket gör så att webbplatsen som skapas hela tiden även uppdateras med de nya filerna som ligger i pub. 

#### Samanfattning av tasks som genomförs: 
 ```
 htmlTask: Kopierar och flyttar över html-filerna till pub-mappen. 
 jsTask: Konkantenerar alla js-filer och skapar en enda, minifierar koden och flyttar detta till pub. 
 cssTask: Gör samma som jsTask fast för CSS-filerna.
 imageTask: Optimerar bilderna och skickar dessa vidare till pub-mappen.
 
 updateBrowser: Härifrån styrs watcher som kontrollerar förändringar och browser-sync som visar webbplatsen och hela tiden håller sig uppdaterad med hjälp av watcher. 
 ```









