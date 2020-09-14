1. Vad är syftet med automatiserings-processen? 
```
Svar: Syftet är att skapa en snabbare utvecklingsprocess.
Autiomatiserings-processen bidrar till att 




2. Vilka paket och verktyg har du använt och varför? 
Svar: Jag har använt paket för att minifiera filer, för att kopiera filer samt för att hålla min 
webbplats uppdaterad automatiskt då förändringar sker. De jag använt är följande: 

"browser-sync": Används för att göra en live-reload. Det vill säga uppdaterar webbplatsen med nya inställningar.
"gulp": Grunden av automatiseringen. Genom detta använder jag alla följande verktyg. 
"gulp-clean-css": Minifierar mina css-filer.
"gulp-concat": Konkatinerar mina JS-filer.
"gulp-concat-css": Konkatinerar CSS-filerna.
"gulp-imagemin": Optimerar mina bilder.
"gulp-uglify-es": Minifierar JS-filerna.

***

3. Beskriv systemet du skapat, hur man startar upp det och de tasks som ingår. 
Svar: För att starta systemet skriver användaren "gulp". 
Kommandot kör igång alla de "tasks" som jag skapat vilket innebär att html-filerna, js-filerna, css-filerna samt bilderna kollas igenom.
Dem minifieras/optimeras sedan och konkatineras sedan innan dem hamnar i "pub-mappen", det vill säga mappen som ska innehålla de färdiga filerna. 
Genom watch och browser-sync så håller hela tiden --- koll på förändingar som görs vilket genom dessa två funktioner medför att filerna i pub-mappen förändras
efter filerna i src-mappen samt att webbläsaren laddar om sidan för att läsa in de nya inställningarna då dessa genomförs. 

