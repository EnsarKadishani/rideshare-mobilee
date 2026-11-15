# RideShare - Java 3

Ruaje këtë skedar si `java-03.md` pranë README në repository-n tënd, jashtë dosjes `aplikacioni/`. Mos shto `.txt` pas emrit. Zëvendëso të gjitha shenjat e plotësimit me atë që ndodhi vërtet. Mjafton një fjali e qartë për çdo provë, por trego çfarë prite dhe çfarë pe.

## Çfarë ndërtova
Sot ndërtova aplikacionin RideShare në Next.js me App Router, duke përfshirë faqen kryesore me tri kartat e udhëtimeve fiktive, faqen dinamike të detajeve `/udhetimi/[id]`, faqen e simulimit të kërkesës `/udhetimi/[id]/kerkesa`, faqen e personalizuar 404 `not-found.tsx`, si dhe komponentin e ripërdorshëm `KartaUdhetimi.tsx`.

## Provat që bëra
### Prova 1: Lista në telefon
Hapa faqen kryesore në pamjen e telefonit (375px me Inspect); prisja tri karta pa lëvizje anash; pashë saktësisht tri kartat e stiluara me kornizë, tekst të qartë dhe përshtatje të plotë responsive pa asnjë scroll horizontal.

### Prova 2: Detajet e udhëtimit të dytë
Klikova kartën 2; prisja adresën /udhetimi/2 dhe vendtakimin e saj; pashë titullin "Fushë Kosovë – AAB", orën 08:15, vendtakimin "Te stacioni kryesor" dhe butonin aktiv "Kërko vend".
Shënova edhe çfarë ndodhi te karta 3 (zero vende) dhe te /udhetimi/99: te karta 3 butoni u shfaq i çaktivizuar me tekstin "Nuk ka vende të lira", kurse te /udhetimi/99 u shfaq faqja e personalizuar "Udhëtimi nuk u gjet" me butonin për kthim te lista.

### Prova 3: Kërkesa në pritje
Klikova Kërko vend; prisja "Simulim: Në pritje", pa rezervim real; pashë titullin "Simulim: Në pritje", njoftimin se kërkesa nuk është dërguar ende te shoferi dhe lidhjen për kthim mbrapa te detajet. Pastaj u ktheva te detajet dhe lista: të gjitha navigimet me lidhjet Next.js funksionuan menjëherë dhe pa rifreskim të faqes.

## Çfarë do të përmirësoj
Për javët e ardhshme do të shtoj ruajtjen reale të të dhënave në një bazë të dhënash (database), autentikimin e përdoruesve (hyrjen e studentëve) dhe zbritjen reale të numrit të vendeve kur shoferi pranon kërkesën.

## Ndihma nga AI (Artificial Intelligence - inteligjencë artificiale)
Përdora AI për të gjeneruar strukturën e projektit me Next.js App Router dhe për të organizuar komponentët e faqet sipas udhëzimeve; kontrollova vetë kodin burimor në çdo skedar, testova personalisht të tri provat në shfletues dhe verifikova kalimin e testeve automatike.
