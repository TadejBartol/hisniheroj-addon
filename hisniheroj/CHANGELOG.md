# Spremembe

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
