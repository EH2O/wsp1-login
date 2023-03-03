# PM grupparbete Login 

Edwin H.O 2023-03-03

Git: https://github.com/EH2O/wsp1-login

## Inledning

I denna uppgift blev vi indelade in i grupper våran grupp hette hala grävlingar (tror jag). Målet var att bygga en login som är kopplat till en databas. Vad det skulle innehålla är register funktion,login samt en session för att använda information efter personen var inloggad. För att göra detta krävdes det att vi använda mysql2 och express-session samt fler NPM packet. Vi behövde mysql2 för att kunna prata med databasen för att hämta och lägga in information. Express-session behövdes för att kunna göra saker efter användaren har loggat in.

Vi arbetar genom att diskutera i gruppen för att lösa ett problem sedan turades vi om att skriva koden som utför den diskuterade lösningen. 



## Bakgrund 

Uppgiften gick ut på att bygga ett inloggningssystem till en test webbsida målet var att kunna registrera en användare, logga in som den skapade användaren, visa viss information beroende på den inloggade användaren. Uppgiften hade ingen grafisk del.

Första problem vi valda att lösa var att logga in som en tidigare manuellt gjord använder. Detta gjordes genom SQL frågor och IF/ELSE satser samt några inmatningsfält som man kunde skriva användarnamn samt lösenord. Detta gjordes genom att först kolla om användarnamnet fanns i databasen sedan om använder namnets krypterade lösenord stämmer med det nuvarande lösenord. För att kryptera samt dekryptera lösenordet använde vi Bcrypt. 

Nästa sak vi gjorde var en profile page skriven i nunjucks (html) för att kunna visa användarnamnet samt senar logga ut användaren.

Efter detta gjorde vi en register funktion så använder kunde registrera nya användare. Detta var relativt likt login funktionen. Vi gjorde detta på sättet att kolla om användaren finns i databasen sedan om den inte fanns la vi till den i databasen med det krypterat lösenord (för säkerhet) antag att både lösenordet och bekräfta lösenordet var lika. Sedan skickade vi användaren till login in sidan för att logga in. 

Till sist gjorde vi en session så att användaren kan gå runt på sidan och göra vad nu man skulle kunna göra på sidan. Till detta användes express session vilket sparade datan temporärt (fliken stängdes eller användaren loggade ut) Detta var enkelt på grund av allt vi gjorde var att sätta några variabler i session. 


Vi hade också automatiska tester som kunde testa programmet åt oss under tiden vi jobbade. Detta gjorde det enkelt att se om den skrivna koden funkade eller ej istället för att behöva pröva manuellt. Vilket gjorde att arbetet gick snabbare framåt. 

## Positiva erfarenheter

Jag gillade arbetssättet med att kunna diskutera med en grupp innan man började göra något. Detta hade självklar några problem men det kommer senare. 

Det gick väldigt bra att skriva koden och det blev inte mycket strul med det. Jag tror detta gick bra på grund av att vi diskuterade lösningen till vi visste hur vi skulle göra innan vi började skriva det. Detta är något jag kommer ta med mig till framtid att ha en lösning på en del av problemet innan jag börja koda. 

Att ha tester så man inte måste manuellt testa koden varje gång hjälpte väldigt mycket. 

Jag har lärt mig mer om hur Github funkar så jag känner att jag faktiskt kan börja använda forks för att testa saker innan jag ändrar på fungerande kod. Detta kommer från att läraren berättade hur man gjorde. 

## Negativa erfarenheter

I sluted visade det sig att vi diskuterade som en grupp men vi hade mest en person som skrev koden. Detta gjorde ju att bara en av oss fick skriva koden vilket gjorde det lite tråkigt att vänta på att person som skrev koden skulle bli klart. 

Vi använde väldigt mycket res.json vilket förmodligen inte är det bästa sättet att lösa problemet (tror jag) hade varit bättre om vi kunde visa på samma sida att något gick fel istället för att man blir fast på en sida som säger “Blabalb blabla bla”

Testerna gjorde att koden var tvungen att skicka vissa responses vilket blev lite irriterande i slutet men testerna hjälpte mer än att vara irriterande men det blir lite störande att få fel när man inte använde en stor bokstav.  Jag skulle istället ha console.log meddelandet och skrivit vad den fick och ungefär vad det borde ha varit och låtit använder  bestämma om det stämmer eller inte. 

## Sammanfattning 

I slutendan var det ett roligt projekt/uppgift som jag fick lärde mig mycket från. Det var inte mycket jag lärde mig om javascript men med alla npm paket vi hade fick jag lära mig mycket. Jag tror att i framtiden att jag skulle kunna skriva ett login program igenom om någon bad mig utan väldigt stora problem. Även om det inte gick 100 med grupparbetet så tycker jag att det fortfarande var bättre än att jobba själv på grund av att få fler än en input gjorde att allting gick lättare och vi stötte på mindre problem än om vi hade gjort detta individuellt.  




