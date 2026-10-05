# HišniHeroj

Družinska aplikacija za opravila, točke in nagrade. Add-on poganja strežnik in spletno aplikacijo (PWA)
na portu **8270** (v add-onu teče na 3000; port na RPi-ju lahko spremeniš v zavihku *Omrežje*). Podatki (baza, slike, skrivnost za seje) so v `/data` in so vključeni v varnostne
kopije Home Assistanta.

## Nastavitve

| Nastavitev | Pomen |
|---|---|
| `base_url` | Javni naslov aplikacije, npr. `https://hisniheroj.gbartol.com`. Mora se ujemati z naslovom v brskalniku. |
| `smtp_url` | SMTP za potrditev e-pošte in pozabljeno geslo, npr. `smtps://uporabnik:geslo-za-aplikacije@smtp.gmail.com:465`. Prazno = e-pošta se samo izpiše v log. |
| `mail_from` | Pošiljatelj e-pošte. |
| `require_email_verification` | Zahtevaj potrditev e-pošte pred prijavo (privzeto: da, če je nastavljen SMTP). |

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
