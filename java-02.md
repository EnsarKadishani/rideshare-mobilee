# RideShare - Java 2

**Shkurtesat:** MVP (Minimum Viable Product - produkti minimal i përdorshëm); AI (Artificial Intelligence - inteligjencë artificiale).

## 1. Problemi
Studentët që udhëtojnë çdo ditë për në kolegjin AAB përballen me vështirësi dhe mungesë koordinimi, pasi njoftimet për udhëtime të përbashkëta janë të shpërndara në shumë biseda e grupe joformale (Viber, WhatsApp, rrjete sociale). Kjo shkakton humbje kohe, pasiguri për gjetjen e një vendi të lirë para orarit të mësimit, kosto më të larta të udhëtimit individual dhe shpesh vonesa në ligjërata.

## 2. Përdoruesit
- **Shoferi (p.sh. Dreni):** Dëshiron të ndajë shpenzimet e karburantit duke publikuar vendet e lira në makinën e tij, të dijë me saktësi se kush do të udhëtojë me të dhe të ketë mundësi të pranojë ose refuzojë kërkesat e udhëtarëve para nisjes.
- **Udhëtari (p.sh. Arta):** Dëshiron të gjejë shpejt dhe lehtë një udhëtim të përshtatshëm drejt AAB-së sipas orarit të ligjëratave, të shohë vendin e takimit dhe numrin e vendeve të lira, si dhe të dërgojë kërkesë e të marrë konfirmim të menjëhershëm e të sigurt nga shoferi.

## 3. Tri ekranet
1. Lista e udhëtimeve: Shfaq të gjitha udhëtimet aktive të disponueshme drejt AAB-së me të dhënat kryesore (relacionin p.sh. Prishtinë – AAB, orën e nisjes 08:00 dhe numrin e vendeve të lira 2 vende), së bashku me butonin "Shiko" për të hapur detajet e secilit udhëtim.
2. Detajet e udhëtimit: Paraqet informacionin e plotë për udhëtimin e zgjedhur, përfshirë relacionin, orën, vendet e mbetura, pikën e saktë të takimit (p.sh. Takimi: Biblioteka) dhe butonin kryesor të veprimit "Kërko një vend" (i cili çaktivizohet nëse nuk ka vende të lira).
3. Kërkesa në pritje: Shfaq konfirmimin vizual me shenjë miratimi (checkmark) që kërkesa u regjistrua me sukses me tekstin "Kërkesa u dërgua" dhe statusin "Prit konfirmimin e shoferit", duke parandaluar kërkesa të dyfishta derisa shoferi të vendosë (pranim ose refuzim).

## 4. MVP - vetëm tri veçori
1. Publikimi i udhëtimit nga shoferi (shoferi vendos relacionin, orën e nisjes, pikën e takimit dhe numrin e vendeve të lira në dispozicion).
2. Shfletimi dhe dërgimi i kërkesës nga udhëtari (udhëtari sheh listën e udhëtimeve, kontrollon detajet dhe dërgon kërkesën për një vend).
3. Menaxhimi i përgjigjes dhe statusi në kohë reale (shoferi pranon ose refuzon kërkesën; me pranimin e kërkesës numri i vendeve të lira zbritet me një dhe udhëtari e sheh statusin e përditësuar nga "Në pritje" në "Pranuar").

## 5. Çfarë e lëmë për më vonë?
1. Sistemi i pagesave elektronike brenda aplikacionit me kartela bankare ose kupona (në MVP llogaritja bëhet manualisht/kesh).
2. Ndjekja e vendndodhjes me hartë live (harta GPS në kohë reale) dhe sistemi i bisedave (chat) mes shoferit dhe udhëtarit.

## 6. Si e provoj?
Kur kërkoj një vend: Udhëtari hap detajet e një udhëtimi me vende të lira dhe klikon butonin "Kërko një vend". Sistemi dërgon kërkesën, butoni bëhet i klikuar dhe shfaqet ekrani "Kërkesa u dërgua - Prit konfirmimin e shoferit". Një klikim i dytë nuk lejohet për të shmangur duplikimet. Pas pranimit nga shoferi, vendet e lira zbriten automatikisht me 1.
Nëse nuk ka vende të lira: Kur numri i vendeve arrin në 0, butoni "Kërko një vend" çaktivizohet menjëherë (disabled) dhe sistemi shfaq qartë njoftimin që nuk ka më vende të lira në këtë udhëtim. Në rast se dy studentë kërkojnë vendin e fundit njëkohësisht, serveri pranon vetëm kërkesën e parë dhe të dytit i kthen arsyen e refuzimit.

## 7. Prova me kolegun
Gjatë demonstrimit të skicës me kolegun, ai fillimisht mendoi se butoni "Rezervo" nënkuptonte që vendi rezervohet automatikisht pa pasur nevojë për aprovimin e shoferit. Për ta bërë rrjedhën plotësisht intuitive dhe reale, e ndryshova tekstin e butonit në "Kërko një vend" dhe te ekrani i fundit shtova statusin e qartë "Kërkesa u dërgua - Prit konfirmimin e shoferit", si dhe treguesin e qartë kur vendet mbarojnë.

## 8. Ndihma nga AI
Përdora inteligjencën artificiale për të strukturuar qartë përgjigjet sipas modelit të kërkuar `java-02-model.md` dhe për të artikuluar saktë kriteret e testimit të MVP-së. Kontrollova personalisht çdo pikë në raport me skicën e tri ekraneve (lista, detajet, kërkesa në pritje) dhe u sigurova që specifikat e relacionit dhe kufizimet e MVP-së t'i përgjigjen me saktësi skenarit të RideShare.
