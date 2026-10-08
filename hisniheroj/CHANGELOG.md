# Spremembe

## 0.6.0

- Zvonec na Domov pokaže le, kar je nujno: oranžen klicaj, ko imaš opravila z rokom danes, rdeč klicaj, ko imaš
  zamujena opravila, ki jih še lahko opraviš. Dotik odpre seznam teh opravil (stari seznam obvestil je odstranjen).
- Ponavljajoči se opomniki na telefon: za vsako tvoje opravilo z rokom danes (privzeto vsako uro) in za vsako
  zamujeno, ki ga še lahko opraviš (privzeto vsake pol ure). Pogostost nastaviš v Profil → Obvestila; gumb
  »Samo opomniki« izklopi vsa ostala obvestila. Ponoči (22:00–7:00) opomnikov ni.
- Push obvestila se pošiljajo z visoko nujnostjo, zato na Androidu pridejo takoj, tudi ko telefon miruje.

## 0.5.2

- Zaključen nakup je opravljeno opravilo »Nakup · N izdelkov« (kategorija Nakupi): vidi se v Opravljeno na Domov,
  v zgodovini in koledarju opravil ter v statistiki (opravila, kategorije). Točke ostanejo enake (1 na izdelek),
  nakupa ni mogoče razveljaviti. Že zaključeni nakupi se ob posodobitvi dopišejo (brez dodatnih točk).
- Številka na ikoni aplikacije: koliko tvojih današnjih opravil še ni opravljenih. Osveži se ob odprtju aplikacije
  in ob vsakem obvestilu. Deluje na iPhonu (aplikacija na začetnem zaslonu, obvestila dovoljena) in na računalniku;
  Android številk na ikonah spletnih aplikacij ne podpira (pokaže le piko ob neprebranih obvestilih).

## 0.5.1

- Številke v spodnjem meniju: na Domov koliko tvojih današnjih opravil še ni opravljenih, na Nakupi koliko
  izdelkov je na seznamu za kupiti.

## 0.5.0

- Nakupovalni seznam (nov zavihek Nakupi): skupen za ves dom in osvežen v živo. Dodajanje s predlogi pogosto
  kupljenega, brez podvajanja (tudi s šumniki), dotik izdelka: količina/opomba ali odstrani.
- Nakup: kdor gre v trgovino, tapne Začni nakup, kljuka, kar da v košarico, in Zaključi nakup. Vsak kupljen
  izdelek je 1 točka (ne glede na količino). Česar ni bilo, ostane na seznamu. Ostali vidijo, kdo je v trgovini.
- Zgodovina nakupov (ikona ure): nakupi po dnevih – kdo, kdaj, koliko izdelkov; dotik pokaže, kaj je bilo kupljeno
  in česa ni bilo, z gumbom »Dodaj vse spet na seznam«.

## 0.4.2

- Popravek: izbirnik doma na zaslonu Domov je imel bele (nevidne) črke.

## 0.4.1

- Profil po dizajnu: stopnja z napredkom, mesečni povzetek (opravila, niz, prevzemi) in seznam nastavitev.
- Profilna slika: naloži ali odstrani (telefon jo obreže na kvadrat). Vidijo jo člani tvojih domov – na opravilih,
  koledarju, zgodovini, lestvici in v družini.
- Nove strani: Ime in slika, Geslo in prijava (menjava gesla, geslo za Google račun, odjava drugih naprav), Obvestila.
- Menjava doma: gumb Preklopi pri vsakem domu, izbirnik v glavi profila in na Domov (če si v več domovih).
- Opravila drugih: jasneje, da zamujena opravila lahko prevzameš takoj (zaklep velja le za ostala).
- Kdor prevzame zamujeno opravilo, dobi vse točke (pol točk velja le za tistega, ki ga je zamudil).
- Odbitek za neopravljeno: če zamujenega opravila do konca ne opravi nihče, se zadolženemu odštejejo njegove točke
  (do 0). Pravilo je privzeto vklopljeno, izklopi ga ustanovitelj v nastavitvah doma. Stara zamujena opravila
  se ob nadgradnji ne kaznujejo za nazaj.
- Namestitev iz drugih brskalnikov: na Androidu "Prenesi aplikacijo" stran odpre v Chromu (Samsung Internet,
  Firefox, Messenger, Instagram …); na iPhonu gumb "Odpri v Safariju". Ostanejo tudi navodila za trenutni brskalnik.

## 0.4.0

- Statistika: lestvica z odrom (teden / mesec / vse), graf zbranih točk skozi čas (dotik imena poudari črto,
  dotik grafa pokaže vrednosti, tudi kot razpredelnica), kdo je opravil največ opravil, opravila po kategorijah
  in značke (niz brez zamude, prevzemi, najmanj zamud). Dotik člana odpre njegova opravila v obdobju in zgodovino.
- Lestvica šteje zaslužene točke – nakupi nagrad je ne zmanjšajo.
- Opravljene kartice (Domov, koledar, zgodovina) imajo debelo zeleno obrobo in svetlo zeleno ozadje;
  opravljene, ki čakajo potrditev, vijolično.

## 0.3.0

- Nagrade: trgovina v Profilu (dodajanje z ikono, ceno, prostimi dnevi in izbiro, kdo jo lahko kupi; hitre predloge).
  Nakup odšteje točke (stopnja ostane), do unovčitve jo lahko vrneš. Unovčiš za danes ali izbran dan – vsi v domu dobijo obvestilo;
  navadno nagrado na Domov označiš »Prejel(a) sem«.
- Prosti dnevi: v teh dneh te rotacija preskoči, pri skupnih nisi med izbranimi, tvoja ostala opravila so prosta za prevzem
  (če jih nihče ne vzame, zapadejo brez zamude in kazni). Vidno na Domov in v koledarju.
- Potrjevanje: opravilo lahko zahteva potrditev – točke se pripišejo, ko skrbnik ali ustanovitelj potrdi (ali zavrne z razlogom).
- Nove vrste obvestil: potrjevanje in nagrade (vklop v Profilu).
- Spodnji meni ima 4 zavihke: Družina se zdaj odpre s kartico doma v Profilu (Moji domovi), z gumbom nazaj.
- Pregled strežnika v Home Assistant (plošča HišniHeroj v stranskem meniju, samo za skrbnike): vsi domovi, člani,
  aktivnost, uporabniki, velikost baze; brisanje domov z vsem v njih in uporabnikov brez doma.

## 0.2.2

- Nov izgled kartic opravil (slog A): nižje in preglednejše, okrogel gumb s kljukico, točke ★ na vsaki kartici.
- Brez kupčkov: opravila so razvrščena po kategorijah in vedno vidna (Domov in Uredi).
- Spodnji meni čez celo širino, prilepljen na spodnji rob in tanjši.

## 0.2.1

- Foto dokaz: opravila, ki zahtevajo sliko, se opravijo s fotografijo (telefon jo pomanjša); slika je vidna samo članom doma.
- Osveževanje v živo: ko nekdo opravi ali prevzame opravilo, se zasloni drugih takoj osvežijo.
- Push obvestila na telefon: novo opravilo zate, prevzem tvojega opravila, opomnik pred rokom, zamujeno,
  razveljavljeno, jutranji povzetek. Vklop in izbira vrst v Profilu; seznam obvestil pod zvoncem. Nočni mir 22:00–7:00.
- Tišji log: samo napake in počasne zahteve.
- Družina: ustanovitelj ureja ime in ikono doma; pri članih so vidne točke in stopnja; ponastavitev točk enemu ali vsem (po želji tudi stopnje).
- Opravila: zavihek Upravljanje je zdaj rumen »✎ Uredi« s kratkim uvodom.
- Samodejna ponastavitev točk (Družina): vsak teden, mesec ali leto od izbranega dne; zmagovalec obdobja v obvestilih.
- Naslovi: Č, Ć in Đ so zdaj enako debeli kot ostale črke (pisava Fredoka jih nima, dopolnjene so iz Nunito Black).

## 0.2.0

- Opravila: kategorije, razpisi (enkratno, dnevno, tedensko, mesečno, letno, vsak n-ti), rok na dan ali v obdobju (z uro),
  rotacija, vsak svoje, skupno; skrbniki; ustavljanje, brisanje v koš in obnova; predloge; hitro opravilo.
- Domači zaslon: opravila v kupčkih, opravljanje z animacijo in razveljavitvijo, točke in stopnje, zamujena (pol točk),
  prevzem opravil drugih s kaznijo za neopravljen prevzem.
- Koledar s prihodnjimi pojavitvami in zgodovina s filtri ter CSV izvozom.
- Razporejevalnik vsako minuto razpiše opravila in obdela zamujena.
- Ob posodobitvi se baza samodejno nadgradi; računi in domovi ostanejo.

## 0.1.3

- Strani Pravila zasebnosti (/zasebnost) in Pogoji uporabe (/pogoji) – potrebni za objavo Google prijave.

## 0.1.2

- Predstavitvena stran na naslovu domene z gumbom »Prenesi aplikacijo« (Android, iPhone, QR za PC).
- Aplikacija je zdaj na /app; nameščena aplikacija se odpre neposredno tam.
- Prijava z Google (gumb) in samodejna prijava z Google One Tap; nastavitvi `google_client_id`, `google_client_secret`.
- Lepša e-poštna sporočila (potrditev, novo geslo), ponovno pošiljanje potrditve, nova povezava ob prijavi nepotrjenega računa.
- Navodila za e-pošto prek Resend.

## 0.1.1

- Privzeti port na RPi-ju je 8270 (3000 pogosto uporablja Grafana).

## 0.1.0

- Prva različica (faza 1): prijava z e-pošto ali uporabniškim imenom (otroški profili),
  gospodinjstva s kodo/QR povabilom, člani in pravice, pravila doma, PWA.
