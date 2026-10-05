# HišniHeroj

Družinska aplikacija za opravila, točke in nagrade. Add-on poganja strežnik in spletno aplikacijo (PWA)
na portu **3000**. Podatki (baza, slike, skrivnost za seje) so v `/data` in so vključeni v varnostne
kopije Home Assistanta.

## Nastavitve

| Nastavitev | Pomen |
|---|---|
| `base_url` | Javni naslov aplikacije, npr. `https://hisniheroj.gbartol.com`. Mora se ujemati z naslovom v brskalniku. |
| `smtp_url` | SMTP za potrditev e-pošte in pozabljeno geslo, npr. `smtps://uporabnik:geslo-za-aplikacije@smtp.gmail.com:465`. Prazno = e-pošta se samo izpiše v log. |
| `mail_from` | Pošiljatelj e-pošte. |
| `require_email_verification` | Zahtevaj potrditev e-pošte pred prijavo (privzeto: da, če je nastavljen SMTP). |

## Javni dostop (Cloudflare Tunnel)

V add-onu **Cloudflared** dodaj nov javni hostname:

```yaml
additional_hosts:
  - hostname: hisniheroj.gbartol.com
    service: http://homeassistant.local:3000
```

(namesto `homeassistant.local` lahko uporabiš IP naslov Raspberry Pi-ja). HTTPS zagotovi Cloudflare.
