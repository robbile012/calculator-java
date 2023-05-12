# calculator-java
simple calculator written in Java; supports addition, subtraction, multiplication and division
fajl START :               start line  end line  cyclomatic complexity   lines of code   parameter count             
start::main                  5         24               3                   16               1








FAJL CALCULATOR :              start line  end line  cyclomatic complexity  lines of code  parameter count

calculator:operations:operations     15         16          1                       2             0
calcucaotr:operations:to string      18         20          1                       3             0
calculator::run                      18         26          1                       3             1
calculator:evalutionexpression       28         72         12!                      33            1
calculator:calculate                 74        186         12!                      77!           2








FAJL START :
Start.java - red 1: Uvoz klase Scanner iz paketa java.util.
Start.java - red 3: Deklaracija javne klase "Start".
Start.java – red 5-7: Deklaracija glavnog metoda koji prima niz stringova kao ulazne parametre.
Start.java - red 9-11: Deklaracija lokalnih promenljivih "Ekpression" i "active". „Izraz“ je inicijalizovan kao string, dok je „aktivan“ logički postavljen na tačno.
Start.java - red 12: Izlaz poruke na konzolu.
Start.java - red 13: Kreiranje nove instance klase Scanner.
Start.java - red 15-21: vhile petlja koja nastavlja da radi dok je "aktivna" je istina. On prima unos od korisnika preko objekta Scanner, proverava da li je unos jednak nizu "ekit", a ako jeste, zatvara objekat Scanner i postavlja "active" na false. Ako unos nije jednak "ekit", on poziva metodu Calculator.Run i šalje rezultat na konzolu.
Start.java – red 23-25: Zatvaranje vitičastih zagrada za glavni metod i klasu.

FAJL CALCULATOR :
Varijabla finalResult je deklarirana kao static. To bi moglo uzrokovati probleme ako se isti kalkulator koristi za više različitih izraza. Bolje bi bilo da se ova varijabla deklarira unutar metode Run() i da se vrati kao povratna vrijednost.
Metoda ToString() u klasi Operations je neispravno napisana. Naziv metode bi trebao početi s malim slovom, a ne velikim, da bi slijedio standard Jave za nazive metoda. Također, ova bi metoda trebala vratiti niz znakova koji sadrži operatore, a ne samo jedan operator. Ime metode bi se trebalo promijeniti u toString() ili getOperators().
Metoda evaluateExpression() vrši mnogo obrade niza, što može dovesti do problema s performansama ako se ulazni niz znakova postane jako veliki.
U metodi Calculate() postoje mnoge slične if-statement grane koje računaju matematičke operacije. Bolje bi bilo napisati jednu opću metodu za obavljanje svih matematičkih operacija umjesto da se ovaj kod ponavlja.
Ako se izraz sadrži negativne brojeve, trenutni kod pokušava pretvoriti niz "-Infinity" ili "Infinity" u float vrijednosti. Ovo će izazvati iznimku NumberFormatException. Bolje bi bilo rukovati ovim slučajem slijedeći standardne matematičke konvencije za negativne brojeve i umetnuti znak minus (-) prije broja.
Magični brojevi – Simboli aritmetičkih operacija su definisani kao magični brojevi u klasi Operacije. Umesto toga, treba ih definisati kao konstante sa smislenim imenima.
