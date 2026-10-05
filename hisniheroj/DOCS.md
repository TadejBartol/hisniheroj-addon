# HišniHeroj

Družinska aplikacija za opravila, točke in nagrade. Add-on poganja strežnik in spletno aplikacijo (PWA)
na portu **8270** (v add-onu teče na 3000; port na RPi-ju lahko spremeniš v zavihku *Omrežje*). Podatki (baza, slike, skrivnost za seje) so v `/data` in so vključeni v varnostne
kopije Home Assistanta.

## Nastavitve

| Nastavitev | Pomen |
|---|---|
| `base_url` | Javni naslov aplikacije, npr. `https://hisniheroj.gbartol.com`. Mora se ujemati z naslovom v brskalniku. |
| `smtp_url` | SMTP za potrditev e-pošte in pozabljeno geslo (glej spodaj). Prazno = e-pošta se samo izpiše v log. |
| `mail_from` | Pošiljatelj e-pošte; domena mora biti potrjena pri ponudniku (npr. `HišniHeroj <no-reply@gbartol.com>`). |
| `require_email_verification` | Zahtevaj potrditev e-pošte pred prijavo (privzeto: da, če je nastavljen SMTP). |
| `google_client_id`, `google_client_secret` | Prijava z Google in samodejna prijava (One Tap). Prazno = gumb Google se ne prikaže. |

## E-pošta (Resend)

1. Ustvari brezplačen račun na [resend.com](https://resend.com) (3000 sporočil/mesec).
2. **Domains → Add domain** → `gbartol.com` (regija EU). Resend ponudi samodejno dodajanje DNS zapisov
   v Cloudflare (*Sign in to Cloudflare*) — ali jih prepiši ročno v Cloudflare → DNS. Počakaj, da je domena *Verified*.
   Obstoječih MX zapisov za tvojo pošto se ne dotika (zapisi so na poddomeni `send.`).
3. **API Keys → Create API key** (dovoljenje *Sending access*, samo domena `gbartol.com`).
4. V nastavitvah add-ona:
   - `smtp_url`: `smtps://resend:<API ključ>@smtp.resend.com:465`
   - `mail_from`: `HišniHeroj <no-reply@gbartol.com>`
5. Ponovno zaženi add-on. Od zdaj nove registracije potrebujejo potrditev e-pošte.

## Prijava z Google

1. [Google Cloud Console](https://console.cloud.google.com) → nov projekt *HisniHeroj*.
2. **APIs & Services → OAuth consent screen** (Google Auth Platform): tip *External*, ime aplikacije HišniHeroj,
   podporni e-naslov, logotip (neobvezno). Pod **Audience** klikni *Publish app* (sicer se lahko prijavijo samo testni uporabniki).
   Obseg (scopes) `openid`, `email`, `profile` ne zahteva Googlovega preverjanja.
3. **Clients → Create client** → *Web application*:
   - Authorized JavaScript origins: `https://hisniheroj.gbartol.com`
   - Authorized redirect URIs: `https://hisniheroj.gbartol.com/api/auth/callback/google`
4. Client ID in Client secret vpiši v `google_client_id` in `google_client_secret`, ponovno zaženi add-on.

Če ima nekdo že račun z isto e-pošto, se prijava z Google samodejno poveže z njim.

## Javni dostop (Cloudflare Tunnel)

V **Cloudflare Zero Trust → Networks → Tunnels → (tunel) → Public Hostname** dodaj:

| Polje | Vrednost |
|---|---|
| Subdomain / Domain | `hisniheroj` / `gbartol.com` |
| Service | `HTTP` → `<IP Raspberry Pi>:8270` |

Cloudflare ustvari DNS zapis in zagotovi HTTPS. `base_url` v nastavitvah add-ona mora biti
točno ta naslov (`https://hisniheroj.gbartol.com`).

Če tunel upravljaš iz add-ona Cloudflared (lokalna konfiguracija), namesto tega dodaj:

```yaml
additional_hosts:
  - hostname: hisniheroj.gbartol.com
    service: http://<IP Raspberry Pi>:8270
```
