# Konfigurátor FMU Lab

Sestavit experiment nad hotovým modelem — bez instalace, bez serveru, bez připojení k síti.

## Jak začít

1. Otevřete v prohlížeči soubor **konfigurator.html** (stačí na něj poklepat).
2. V sekci 1 vyberte metadata modelu ze složky **metadata/**.
3. Projděte sekce 2 až 3C a nakonec v sekci 4 klikněte **Download experiment JSON**.
4. Stažený soubor pošlete kurátorovi; ten ho zařadí do katalogu.

## Modely v tomto balíku

| Model | Soubor s metadaty | Proměnných |
| --- | --- | --- |
| Alveolo-kapilární jednotka (s tkání) | `metadata/alveolar-capillary-tissue.json` | 310 |
| Dodání dortu (OPM, kvalitativní) | `metadata/cake-providing.json` | 54 |
| Kávovar (OPM, kvalitativní) | `metadata/coffee-brewing.json` | 31 |
| Zásoba železa ve ferritinu | `metadata/ferritin.json` | 39 |
| Zásoba železa ve ferritinu (varianta) | `metadata/ferritin-variant.json` | 41 |
| Hodgkin–Huxley — dráždivá membrána | `metadata/hodgkin-huxley.json` | 94 |
| Metabolismus železa | `metadata/iron-metabolism.json` | 260 |
| JWST — obrázek 3-5 (Dori, kapitola 3) | `metadata/jwst-fig35.json` | 77 |
| Normální krevní oběh | `metadata/normal-circulation.json` | 579 |
| Normální oběh (z OPM diagramu) | `metadata/normal-circulation-opm.json` | 225 |
| Vytápění místnosti | `metadata/room-heating.json` | 9 |
| Vytápění místnosti (varianta) | `metadata/room-heating-variant.json` | 9 |
| Samoobslužná myčka (OPM, kvalitativní) | `metadata/self-service-car-wash.json` | 54 |
| Jednoduchá respirace | `metadata/simple-respiration.json` | 527 |
| Jednoduchá respirace (z OPM diagramu) | `metadata/simple-respiration-opm.json` | 281 |
| Aktivace uživatele (OPM, kvalitativní) | `metadata/user-activation-process.json` | 31 |

## Co tady nefunguje a proč

Tlačítka **Test run** a **Open in simulator** otevírají skutečnou aplikaci, a ta musí být
na téže adrese jako tahle stránka. Ze souboru otevřeného z disku to nejde. Prakticky to
znamená jediné: **tempo simulace ověří až kurátor**, když experiment zařazuje. Ostatní
kontroly si konfigurátor dělá sám.

Tlačítko **Download page HTML** ze stejného důvodu nepracuje; potřebuje soubor s webovými
komponentami, který tenhle balík nenese.

## Na co si dát pozor

- **Výchozí hodnota posuvníku musí ležet na jeho mřížce.** Při minimu 2000 a kroku 10 je
  4860 v pořádku, 4865 ne.
- **Jedna osa na graf.** Veličiny různých řádů se v jednom grafu splácnou do rovnoběžek.
- **Čísla v textech kroků musí být odečtená z běžícího modelu**, ne odhadnutá.

Podrobný návod ke konfigurátoru má kurátor.
