# Webbutveckling 3 - moment 2

#### 1. Vad är syftet med automatiserings-processen? 

Syftet är att skapa en snabbare utvecklingsprocess.
Autiomatiserings-processen bidrar till att 

***

 #### 2. Vilka paket och verktyg har du använt och varför? 
Jag har använt paket för att minifiera filer, för att kopiera filer samt för att hålla min 
webbplats uppdaterad automatiskt då förändringar sker. De jag använt är följande: 

```
• "browser-sync": Används för att göra en live-reload. Det vill säga uppdaterar webbplatsen med nya inställningar.
• "gulp": Grunden av automatiseringen. Genom detta använder jag alla följande verktyg. 
• "gulp-clean-css": Minifierar mina css-filer.
• "gulp-concat": Konkatinerar mina JS-filer.
• "gulp-concat-css": Konkatinerar CSS-filerna.
• "gulp-imagemin": Optimerar mina bilder.
• "gulp-uglify-es": Minifierar JS-filerna.
```
***

#### 3. Beskriv systemet du skapat, hur man startar upp det och de tasks som ingår. 
*För att använda dig av systemet behöver du ha node.js samt npm installerat på datorn* 

 För att använda det skapade systemet börjar användarn med att öppna upp terminalen fristående eller genom tillexempel visual studio code. Navigera dig sedan fram till platsen som du vill spara mappen med systemet i, tillexempel skrivbord. 
```
cd desktop 
```
Därefter används följande kommando för att hämta system-mappen
```
git clone https://github.com/malinsvensson98/Webb3_moment2.git 
```
Användaren har därefter laddat ned filerna och kan därefter öppna upp dessa i valfri kodeditor, tillexempel det tidigare nämnda visual studio code. 
För att sedan installera alla paket som krävs så används 
```
npm install 
```
och då detta är installerat kan användaren starta systemet genom att skriva
```
gulp 
```
Det som sker då kommandot används är att en ny mapp vid namn "pub" skapas. 
Denna mappen är till för att innehålla alla "färdiga" filer som sedan ska laddas upp. 
Till mappen flyttas alla skapade html-filer, bilder, css-filer samt JavaScript-filer upp och innan dem hamnar där går dem igenom en process där allting minimeras/optimeras och om det finns flera filer, tillexempel två skilda css-filer så slås dem samman. 



