## Individuell reflektion 

## Steg 1 – Produktens livscykel

Under DevOps-kursen har jag arbetat individuellt med ett projekt där jag steg för steg lärde mig hur man utvecklar, testar och publicerar en webbtjänst. I början visste jag inte så mycket om hur hela processen fungerar. Nu förstår jag bättre hur olika delar hänger ihop och varför de behövs.

I M1 började jag med Git och GitHub. Jag lärde mig att skapa commits och använda ett repository för att spara mitt arbete. I M2 arbetade jag med branches och Pull Requests. Jag testade också hur konflikter kan uppstå när man ändrar samma kod i olika branches. Det var nyttigt att se hur Git hjälper till att hantera ändringar.
I M3 började jag använda Docker. Jag lärde mig att köra backend och frontend i containers med Docker Compose. Det gjorde det enklare att starta hela applikationen. I M4 arbetade jag med tester och hittade ett fel i backend. Jag skrev ett test som visade felet och rättade sedan koden. Då förstod jag varför tester är viktiga.
I M5 började jag arbeta med GitHub Actions och CI. Jag testade att göra en ändring som gjorde att kontrollen blev röd. Jag kunde inte mergea min Pull Request förrän felet var rättat. Det visade mig att CI hjälper till att upptäcka problem innan de kommer till main.
I M6 lärde jag mig att automatiskt bygga och publicera Docker-images. I M7 arbetade jag med en virtuell server på cPouta och fick applikationen att fungera där. I M8 använde jag Terraform för att hantera serverns infrastruktur med kod.
Till slut, i M9, kopplade jag ihop allt med automatisk deployment. Jag ändrade rubriken på webbplatsen och mergade min Pull Request. GitHub Actions byggde och publicerade nya images och uppdaterade applikationen på servern. När jag öppnade webbplatsen såg jag den nya rubriken.

Den största skillnaden för mig är att jag i början gjorde nästan allt manuellt. I slutet kunde flera steg köras automatiskt. Jag behövde fortfarande kontrollera resultatet, men jag behövde inte göra varje steg själv.

## Steg 2 – Vad går sönder utan automation?

Under kursen förstod jag att automation inte bara handlar om att spara tid. Den hjälper också till att minska risken för misstag.

Ett tydligt exempel är M4 och M5. I M4 hittade jag ett fel där antalet tecken inte uppdaterades korrekt när en anteckning togs bort. Jag skrev ett test som visade problemet och rättade det. Utan automatiska tester hade jag behövt kontrollera detta manuellt varje gång jag ändrade koden. Det skulle ta mer tid, och jag skulle lätt kunna glömma något.
I M5 testade jag också att göra en ändring som fick CI att misslyckas. GitHub visade att kontrollen var röd och blockerade min Pull Request. Jag behövde rätta felet innan jag kunde fortsätta. Det var ett konkret exempel på hur automation kan stoppa problem innan de hamnar i main.
Ett annat exempel är M9. Tidigare behövde jag själv ansluta till servern och arbeta med Docker för att uppdatera applikationen. Med automatisk deployment räckte det att göra en ändring och mergea den till main. Resten av processen kördes av GitHub Actions.

Om jag skulle göra detta manuellt varje gång skulle det ta längre tid. Jag skulle också kunna glömma ett kommando, använda fel version eller missa att uppdatera någon container. Med automation blir processen mer likadan varje gång.

Jag har också förstått att automation inte betyder att man kan sluta kontrollera sitt arbete. Man måste fortfarande läsa felmeddelanden, förstå vad som händer och testa att applikationen fungerar.

För mig har kursen varit både utmanande och lärorik. Eftersom jag arbetade ensam behövde jag själv lösa problemen och förstå varje steg. Det viktigaste jag tar med mig är att DevOps handlar om hela vägen från kod till en fungerande tjänst, och att tester, samarbete via Git och automation gör den processen säkrare och enklare.