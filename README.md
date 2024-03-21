# EbCase24
APiTest
Case för QA Engineer

Flödet

Teststrategi:
Genom att täcka både positiva och negativa scenarier säkerställer jag att API:t hanterar olika typer av input korrekt och även negativa test mot felaktiga anrop. Testfallen skulle i detta fall få mer detaljerade teststeg och med hjälp av testdata skulle vi även skapa ett förväntat resultat. Jag har lagt upp testdata för flöde “5. Verifiera trackingsida” detta har jag tagit fram med hjälp av testerna som finns på GitHub.ss

 1.Autentisering
Positiva testfall:
-Autentisera med giltiga användaruppgifter och förvänta sig statuskod 200 och ett giltigt autentiseringstoken.
-Förnya autentiseringstoken med giltig förnyelse-token och förvänta sig statuskod 200 och ett nytt autentiseringstoken.

Negativa testfall:
-Autentisera med ogiltiga användaruppgifter och förvänta sig ett felmeddelande med statuskod 401.
-Försöka använda utgånget autentiseringstoken och förvänta sig ett felmeddelande med statuskod 401
 2.Kolla så att leverans är möjlig till vald adress
Positiva testfall:
-Skicka en giltig adress där leverans är möjlig och förvänta sig statuskod 200 med en bekräftelse.

Negativa testfall:
-Skicka en ogiltig adress och förvänta sig ett felmeddelande med statuskod 400.
-Skicka en giltig adress där leverans inte är möjlig och förvänta sig ett felmeddelande med statuskod 422. 
3.Boka leverans för vald adress
Positiva testfall:
-Boka leverans med alla nödvändiga och giltiga uppgifter för en produkt (ex. ‘home’) och förvänta sig statuskod 200 med bokningsbekräftelse.
-Boka leverans med begäran om specialhantering och förvänta sig statuskod 200 med bokningsbekräftelse som inkluderar specialhantering.

Negativa testfall:
-Boka leverans utan nödvändiga uppgifter och förvänta sig ett felmeddelande med statuskod 400.
-Boka leverans med ogiltig produkt-id och förvänta sig ett felmeddelande med statuskod 404.

 4.Kolla status för bokning
Positiva testfall:
-Kolla status för en giltig bokning och förvänta sig statuskod 200 med korrekt statusinformation.

Negativa testfall:
-Testfall: Kolla status med ogiltigt boknings-ID och förvänta sig ett felmeddelande med statuskod 404.


5.Verifiera att trackingsida visar korrekt status

Positiva testfall:
Testfall: Använd tracking-ID från en giltig bokning på trackingsidan och förvänta sig att sidan visar korrekt status för leveransen.

Testdata: https://track-test.earlybird.se/home?a=UE954142770SE&b=simo

Negativa testfall:
Testfall: Använd ett ogiltigt tracking-ID på trackingsidan och förvänta sig ett felmeddelande eller indikation på att ingen information hittades.
 


