# Wzorce: elementy (atomy i molekuły)

meta/wersja: **2026-11-17.3**

Atomy i molekuły: ikony, punktor, odznaka, karta szklana, ramki zdjęć, karty, ściana logo, wiersze list i tabel. Tokeny są w pliku indeksu `prezentacje-v1.md`.

Zastępuj `[[rola]]` i `{pole}`. Twarda spacja w HTML to `&#160;` (tylko encje numeryczne). Nie zmieniaj struktury, kolejności ani odstępów w szablonie, zmieniaj tylko pola.

### Kafelek logo partnera

Kiedy: logo partnera lub TFI w nagłówku, po prawej. Pole: plik logo (wgrany przez użytkownika, najlepiej SVG/PNG na przezroczystym tle). Pozycja stała: x=1224, y=128.

```html
<div style="position:absolute;left:1224px;top:128px;width:360px;height:112px;background:[[tlo/kafelek-logo]];border-radius:14px;display:flex;flex-direction:column;justify-content:center;align-items:center"><img src="{logo}" alt="{nazwa}" style="width:328px;height:80px;object-fit:contain"></div>
```

### QR z podpisem

Kiedy: odnośnik do strony funduszu lub materiałów. Pola: kod QR (obraz od użytkownika), podpis (do 2 linii, twarde spacje). Pozycja stała: kod x=1648 y=128, podpis x=1552 y=284.

```html
<div style="position:absolute;left:1648px;top:128px;width:144px;height:144px;background:[[tlo/kafelek-logo]];border-radius:12px;display:flex;flex-direction:column;justify-content:center;align-items:center"><img src="{qr}" alt="Kod QR" style="width:128px;height:128px;object-fit:contain"></div>
<p style="position:absolute;left:1552px;top:284px;width:240px;font-size:24px;line-height:1.2;text-align:right;text-decoration:underline;color:[[tekst/podstawowy]]">{podpis}</p>
```

### Sekcja tekstowa

Kiedy: dłuższy opis z nagłówkiem, bez karty. Sekcje układaj w kolumnie szerokości 1312 px z odstępem 20 px: `<div style="display:flex;flex-direction:column;gap:20px;width:1312px">` … sekcje … `</div>`. Pojemność kolumny: 2–3 sekcje, łącznie do 12 linii akapitów (ok. 1000 znaków, ok. 92 znaki w linii).

```html
<div style="display:flex;flex-direction:column;gap:6px"><p style="font-size:24px;line-height:1.3;font-weight:600;letter-spacing:3px;text-transform:uppercase;color:[[tekst/podstawowy]]">{naglowek}</p><p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{akapit}</p></div>
```

### Portret w kółku

Kiedy: zdjęcie osoby (np. zarządzającego). Pole: zdjęcie kwadratowe lub przycięte do kwadratu, imię i nazwisko w alt. Pozycja stała: x=1504, y=440 (nad paskiem wskaźników, pod podpisem QR).

```html
<div style="position:absolute;left:1504px;top:440px;width:288px;height:288px;background:[[akcent/glowny]];border-radius:144px;display:flex;align-items:center;justify-content:center"><img src="{portret}" alt="{osoba}" style="width:284px;height:284px;border-radius:142px;object-fit:cover"></div>
```

## Atomy

Najmniejsze elementy, z których składają się molekuły i układy.

### Ikony

Jeden styl: linia 1,75, końce i łączenia zaokrąglone, bez wypełnienia, jeden kolor. Używaj wyłącznie ikon z poniższej listy, wybierając według znaczenia; nie rysuj i nie przenoś ikon ze źródła. Dwa warianty koloru: `limonka` (na ciemnych kartach i tle, kolor akcent/glowny) oraz `ciemne` (na limonkowym tle, kolor tekst/na-limonce). Domyślny rozmiar 64×64 px (wyjątek: łączniki cyklu 328×192, tylko w Diagramie cyklu); w wierszu listy 40×40, w wierszu tabeli 48×48 (inne rozmiary niedozwolone). Pliki SVG:

- limonka: `https://raw.githubusercontent.com/tomaszkaczmarek-ai/ds-assets/main/ikony/limonka/<plik>`
- ciemne: `https://raw.githubusercontent.com/tomaszkaczmarek-ai/ds-assets/main/ikony/ciemne/<plik>`

Pobierz potrzebne pliki poleceniem w powłoce (np. `curl -sSLO <adres>`), wgraj do talii jako zasób i użyj zwróconego adresu `/_blob/…`. Jeśli pobranie się nie uda, zgłoś to w raporcie i zostaw w miejscu ikony puste miejsce 64×64.

| Znaczenie | Plik |
|---|---|
| bezpieczeństwo | bezpieczenstwo.svg |
| środki | srodki.svg |
| wzrost | wzrost.svg |
| oszczędności | oszczednosci.svg |
| bank, instytucja | bank.svg |
| gotówka | gotowka.svg |
| koszty, opłaty | koszty.svg |
| współpraca | wspolpraca.svg |
| klienci | klienci.svg |
| osoba | osoba.svg |
| doradztwo | doradztwo.svg |
| firma | firma.svg |
| świat | swiat.svg |
| czas, horyzont | czas.svg |
| termin | termin.svg |
| ochrona | ochrona.svg |
| dostęp | dostep.svg |
| regulacje, prawo | regulacje.svg |
| dokument | dokument.svg |
| wyniki | wyniki.svg |
| notowania | notowania.svg |
| struktura | struktura.svg |
| oprocentowanie | oprocentowanie.svg |
| ochrona kapitału | ochrona-kapitalu.svg |
| dywersyfikacja | dywersyfikacja.svg |
| cel | cel.svg |
| analiza | analiza.svg |
| potwierdzenie | potwierdzenie.svg |
| kontakt | kontakt.svg |
| platforma online | platforma.svg |
| nagrody | nagrody.svg |
| płynność | plynnosc.svg |
| łącznik cyklu, komórka w prawym górnym rogu (z góry w dół) | lacznik-gora-prawo.svg |
| łącznik cyklu, prawy dolny róg (z prawej w lewo) | lacznik-dol-prawo.svg |
| łącznik cyklu, lewy dolny róg (z dołu w górę) | lacznik-dol-lewo.svg |
| łącznik cyklu, lewy górny róg (z lewej w prawo) | lacznik-gora-lewo.svg |

Szablon ikony:

```html
<img src="{ikona}" alt="" style="width:64px;height:64px">
```

### Punktor „//”

Kiedy: pozycja listy w sekcji tekstowej lub wyliczeniu.

```html
<div style="display:flex;flex-direction:row;gap:12px"><p style="font-size:24px;font-weight:700;line-height:1.35;color:[[akcent/glowny]]">//</p><p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{pozycja}</p></div>
```

### Znak „+”

Kiedy: między elementami formuły (A + B + C).

```html
<p style="font-size:56px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">+</p>
```

Rząd z operatorem „+”: gdy źródło nie ma opisów kart, karty zostają małe (tytuł i ikona) i rząd jest wyśrodkowany w pionie; nie dopisuj opisów i nie powiększaj kart dla wypełnienia slajdu. Gdy źródło ma opisy, użyj kart „Ikona z opisem” (ikona 64, tytuł 30, opis 26) w tym samym rzędzie. Karty w rzędzie mają jednakową wysokość (`align-items:stretch`), znak „+” jest wyśrodkowany w pionie względem rzędu, a cały rząd podlega zasadom z sekcji „Odstępy i obszar treści” (wyśrodkowanie w pionie, gdy blok jest niższy niż 70% obszaru).

```html
<div style="display:flex;flex-direction:row;align-items:stretch;gap:16px">{KARTA A}<div style="display:flex;flex-direction:column;justify-content:center"><p style="font-size:56px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">+</p></div>{KARTA B}<div style="display:flex;flex-direction:column;justify-content:center"><p style="font-size:56px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">+</p></div>{KARTA C}</div>
```

### Odznaka

Kiedy: krótka etykieta kategorii w rogu slajdu lub nad treścią (np. FUNDUSZ INWESTYCYJNY). Do 3 słów.

```html
<div style="display:flex;flex-direction:row"><p style="font-size:24px;font-weight:600;letter-spacing:3px;text-transform:uppercase;line-height:1.3;color:[[tekst/na-limonce]];background:[[akcent/glowny]];border-radius:16px;padding:8px 20px">{tekst}</p></div>
```

### Karta szklana

Kiedy: blok treści na zdjęciu (okładka, przekładka) lub gdy zdjęcie jest dozwolone zgodnie z sekcją 9. Bez limonkowej kreski.

```html
<div style="display:flex;flex-direction:column;gap:8px;background:[[tlo/kolumna-funduszu]];border-radius:40px;padding:32px 40px">{ZAWARTOŚĆ}</div>
```

### Ramka zdjęcia

Kiedy: wyłącznie portret osoby w treści. Grafiki, zrzuty ekranu, schematy i ilustracje nie dostają ramki. Limonkowa linia 2 px. Kółko (średnica {d}, zdjęcie {d} minus 4 px, promień połowa d) lub prostokąt (promień 24 px).

```html
<div style="width:{d}px;height:{d}px;background:[[akcent/glowny]];border-radius:{d/2}px;display:flex;align-items:center;justify-content:center"><img src="{zdjęcie}" alt="{opis}" style="width:{d-4}px;height:{d-4}px;border-radius:{d/2-2}px;object-fit:cover"></div>
```

```html
<div style="width:{szer}px;height:{wys}px;background:[[akcent/glowny]];border-radius:24px;display:flex;align-items:center;justify-content:center"><img src="{zdjęcie}" alt="{opis}" style="width:{szer-4}px;height:{wys-4}px;border-radius:22px;object-fit:cover"></div>
```

## Molekuły

Gotowe połączenia atomów. Wszystkie stoją w ramie box danych (cienka limonkowa kreska u góry) i mają wysokość naturalną, bez rozciągania. Szerokość boxu w rzędzie: 2 boxy 816, 3 boxy 533, 4 boxy 392 (odstęp 32). Pojemności liczone dla Montserrat (średnio 12,7 px na znak w 24 px; 13,8 w 26 px; 16,8 w 30 px pogrubionym; 16,2 w 24 px półpogrubionym z odstępem 3).

### Karta osoby

Kiedy: zarządzający, zespół, doradcy: 2–4 osoby obok siebie. Pola: zdjęcie (kwadrat), imię i nazwisko, rola, opis. Zdjęcie w kółku średnicy 200 (zdjęcie 196 + ramka 2 px).

```html
<div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:16px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:40px">
<div style="width:200px;height:200px;background:[[akcent/glowny]];border-radius:100px;display:flex;align-items:center;justify-content:center"><img src="{zdjęcie}" alt="{imię i nazwisko}" style="width:196px;height:196px;border-radius:98px;object-fit:cover"></div>
<p style="font-size:30px;font-weight:700;line-height:1.2;text-align:center;color:[[tekst/tytul]]">{imię i nazwisko}</p>
<p style="font-size:24px;font-weight:600;letter-spacing:3px;text-transform:uppercase;line-height:1.3;text-align:center;color:[[akcent/glowny]]">{rola}</p>
<div style="width:100%;border-top:1px solid [[linia/karta]]"></div>
<p style="font-size:24px;line-height:1.35;text-align:center;color:[[tekst/podstawowy]]">{opis}</p>
</div>
```

Pojemność (padding 40): w rzędzie po 3 osoby: imię i nazwisko do 26 znaków (1 linia), rola do 2 linii po 28 znaków, opis do 4 linii po 35 znaków (ok. 140 znaków). Po 2 osoby: imię i nazwisko do 40 znaków, rola do 2 linii po 45 znaków, opis do 4 linii po 60 znaków. Po 4 osoby: padding 32, zdjęcie 160 (156 + ramka 2 px, promień 80), imię i nazwisko do 19 znaków, rola do 2 linii po 20 znaków, opis do 4 linii po 25 znaków (ok. 100 znaków). Wysokość: 3 osoby ok. 546 px, 4 osoby ok. 510 px.

### Ikona z opisem

Kiedy: pojedyncza cecha, korzyść lub krok. Pola: ikona (z sekcji Atomy → Ikony, limonkowa), tytuł, opis.

```html
<div style="flex:1;display:flex;flex-direction:column;gap:16px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:40px">
<img src="{ikona}" alt="" style="width:64px;height:64px">
<p style="font-size:30px;font-weight:700;line-height:1.2;color:[[tekst/tytul]]">{tytuł}</p>
<p style="font-size:26px;line-height:1.35;color:[[tekst/podstawowy]]">{opis}</p>
</div>
```

Pojemność w rzędzie po 3 (padding 40): tytuł 26 znaków w linii, opis 32 znaki w linii. Dwa rzędy po 3 (6 pozycji): tytuł 1 linia, opis do 2 linii (ok. 64 znaków); wysokość boxu ok. 286, dwa rzędy z odstępem 32 ok. 604. Jeden rząd po 3: tytuł do 2 linii, opis do 5 linii (ok. 160 znaków). Rząd po 4 (padding 32): tytuł 19 znaków w linii, opis 23 znaki w linii, tytuł do 2 linii, opis do 4 linii.

### Box z logo

Kiedy: podmiot, partner lub produkt, który ma logo (spółki grupy, partnerzy, fundusze). Pola: logo (biblioteka partnerów lub plik od użytkownika), tytuł (nazwa), opcjonalnie opis i dodatkowy znak (np. drugie małe logo). Logo stoi na białym kafelku u góry boxu; kafelek ma wysokość 96 i szerokość boxu, logo 240×64 (contain). Tytuł i opis są wyśrodkowane w poziomie. Boxy w rzędzie mają jednakową wysokość.

```html
<div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:16px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:32px">
<div style="width:100%;height:96px;display:flex;flex-direction:row;align-items:center;justify-content:center;background:[[tlo/kafelek-logo]];border-radius:14px"><img src="{logo}" alt="{nazwa}" style="width:240px;height:64px;object-fit:contain"></div>
<p style="font-size:30px;font-weight:700;line-height:1.2;text-align:center;color:[[tekst/tytul]]">{tytuł}</p>
<p style="font-size:26px;line-height:1.35;text-align:center;color:[[tekst/podstawowy]]">{opis}</p>
</div>
```

Pojemność w rzędzie po 4 (wewnętrzna szerokość 328): tytuł 19 znaków w linii, do 3 linii; opis 23 znaki w linii, do 4 linii. Po 3 (padding 40 zamiast 32): tytuł 26 znaków, opis 32. Brak opisu: pomiń drugi akapit. Dodatkowy znak (np. logo giełdy z krótkim podpisem) wstaw pod opisem jako wiersz: kafelek logo 160×48 plus tekst 24 px.

### Kolumna z ikoną i listą

Kiedy: kategoria z kilkoma punktami (np. obszary usług, zalety). Pola: ikona, tytuł, 2–5 pozycji listy. Pozycja ma do 2 linii.

```html
<div style="flex:1;display:flex;flex-direction:column;gap:16px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:40px">
<img src="{ikona}" alt="" style="width:64px;height:64px">
<p style="font-size:30px;font-weight:700;line-height:1.2;color:[[tekst/tytul]]">{tytuł}</p>
<div style="border-top:1px solid [[linia/karta]]"></div>
<div style="display:flex;flex-direction:column;gap:12px">{POZYCJE: atom „Punktor //”}</div>
</div>
```

Pojemność: w rzędzie po 3 (padding 40) pozycja ma 33 znaki w linii; w rzędzie po 4 (padding 32) 22 znaki w linii. Wysokość: tytuł 1 linia, 5 pozycji po 2 linie ok. 590 px; mniej pozycji odpowiednio mniej (pozycja 1-liniowa 33 px, 2-liniowa 65 px, odstęp 12).

### Ściana logo partnerów

Kiedy: lista partnerów, dystrybutorów lub towarzystw (do 20 logo). Pola: logo z biblioteki (poniżej), nadtytuł i tytuł nagłówka. Logo bierz z biblioteki, nie z pamięci; logo spoza biblioteki wgraj od użytkownika. Kolejność alfabetyczna, chyba że brief mówi inaczej. Pięć kafli w rzędzie, ostatni niepełny rząd wyśrodkowany. Kafel 307×112 (promień 14, tło tlo/kafelek-logo), odstęp 32. Logo jest wyśrodkowane w kaflu i ma własny rozmiar dobrany optycznie (tabela niżej), żeby wysokie logo (Allianz, VIG, Quercus, Franklin Templeton) nie wyglądały na małe obok szerokich. Rzędy: 1–5 logo 1 rząd, 6–10 dwa, 11–15 trzy, 16–20 cztery (wysokość 544). Więcej niż 20: zgłoś i zapytaj. Cała ściana jest blokiem w obszarze treści (sekcja „Odstępy i obszar treści”), wyśrodkowanym w pionie.

Adres logo: `https://raw.githubusercontent.com/tomaszkaczmarek-ai/ds-assets/main/logo-partnerow/{plik}.svg`. Pliki: allianz, blackrock, caspar, erste-tfi, esaliens, fidelity-international, franklin-templeton, generali-investments, ing, investors-tfi, ipopema, pzu-inwestycje, quercus, rockbridge, schroders, skarbiec, superfund, uniqa, vig-c-quadrat, caspar-asset-management-dark, caspar-asset-management-light, caspar-tfi-dark, caspar-tfi-light. Wersja „dark” (ciemne litery) jest na biały kafelek, wersja „light” (białe litery) na ciemne tło; na kafelku zawsze „dark”.

Logo FTiW (stopka, okładka, zamknięcie, kafelek): `https://raw.githubusercontent.com/tomaszkaczmarek-ai/ds-assets/main/logo-ftiw/{plik}.svg`. Pliki: poziom-biale (na ciemne tło, stopka i okładka, proporcje 1152×85), poziom-kolor, pion-biale, pion-kolor (na białe tło lub kafelek). Gdy użytkownik nie wgrał własnego logo, użyj stąd.

```html
<div style="display:flex;flex-direction:row;justify-content:center;gap:32px">{KAFLE}</div>
```

Rozmiar logo w kaflu (szerokość × wysokość w px, proporcje pliku zachowane): allianz 140×88, blackrock 267×43, caspar-asset-management-dark 191×70, caspar-tfi-dark 191×70, erste-tfi 188×71, esaliens 267×48, fidelity-international 205×65, franklin-templeton 165×81, generali-investments 243×55, ing 226×59, investors-tfi 215×62, ipopema 241×55, pzu-inwestycje 189×70, quercus 165×81, rockbridge 239×56, schroders 262×51, skarbiec 257×52, superfund 209×64, uniqa 225×59, vig-c-quadrat 89×88. Wersje „dark” i „light” Caspar mają ten sam rozmiar; stary plik caspar.svg nie jest używany na ścianie. Logo spoza biblioteki: proporcje p = szerokość/wysokość pliku, wysokość h = min(88; pierwiastek z (13350 / p)), szerokość w = h × p; gdy w > 267, przyjmij w = 267 i h = 267 / p. Pliki w bibliotece mają przycięte marginesy do zawartości (viewBox), więc rozmiar nie zawiera pustego pola.

Kafel (szerokość i wysokość logo z tabeli):

```html
<div style="width:307px;height:112px;background:[[tlo/kafelek-logo]];border-radius:14px;display:flex;align-items:center;justify-content:center"><img src="{logo}" alt="{nazwa}" style="width:{szerokość}px;height:{wysokość}px;object-fit:contain"></div>
```

### Wiersz składnika

Kiedy: lista składników, partnerów lub funduszy z logo i nazwą (np. skład portfela). Pola: logo z biblioteki (folder logo-partnerow), nazwa. Małe kafelki logo 144×32 w polu 144×32 z paddingiem 8 (razem 160×48), odstęp między wierszami 16. Nazwa 1 linia do ok. 53 znaków przy szerokości 680 px (kolumna 864 px); dłuższa zawija się do 2 linii (wiersz 65 px).

```html
<div style="display:flex;flex-direction:row;align-items:center;gap:24px"><div style="width:160px;height:48px;background:[[tlo/kafelek-logo]];border-radius:14px;display:flex;align-items:center;justify-content:center"><img src="{logo}" alt="{nazwa}" style="width:144px;height:32px;object-fit:contain"></div><p style="width:680px;font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{nazwa}</p></div>
```

### Tabela wyników (okresy)

Kiedy: jeden wiersz wartości w kilku okresach (np. stopa zwrotu 1M, 3M, 6M, 12M, 36M, 60M, YTD). Szerokość 736 px: pierwsza kolumna 100, siedem kolumn po 90. Nagłówek pogrubiony z linią limonkową pod spodem, bez tła. Wartość do 6 znaków (np. „18,07%”). Dla szerszej tabeli dostosuj kolumny tak, aby suma szerokości = szerokość kolumny slajdu.

```html
<div style="display:flex;flex-direction:column">
<div style="display:flex;flex-direction:row;border-bottom:1px solid [[akcent/glowny]]"><div style="width:100px;display:flex;flex-direction:column;justify-content:center"><p style="padding:10px 4px;font-size:24px;line-height:1.25;font-weight:700;color:[[tekst/podstawowy]]">{nazwa wiersza nagłówka}</p></div>(… kolumny nagłówka po 90 px, ten sam styl)</div>
<div style="display:flex;flex-direction:row"><div style="width:100px;display:flex;flex-direction:column;justify-content:center"><p style="padding:10px 4px;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{nazwa wiersza}</p></div>(… wartości po 90 px, ten sam styl)</div>
</div>
```

### Wiersz listy z ikoną

Kiedy: lista 2–5 faktów z ikoną, w kolumnie tekstowej (np. obok opisu). Ikona z biblioteki w rozmiarze 40, linia nad każdym wierszem i jedna pod ostatnim (linia/karta). Tekst do 2 linii. Wiersze łączysz w kolumnie bez odstępów, z linią zamykającą na dole.

```html
<div style="display:flex;flex-direction:row;align-items:center;gap:24px;border-top:1px solid [[linia/karta]];padding:20px 0"><img src="{ikona}" alt="" style="width:40px;height:40px"><p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{tekst}</p></div>
```

Kolumna z wierszami kończy się: `<div style="border-bottom:1px solid [[linia/karta]]">{WIERSZE}</div>`. Wysokość wiersza 1-liniowego 81 px.

### Karta wyśrodkowana

Kiedy: element schematu lub podsumowania (np. spółka matka, spółka zależna), treść wyśrodkowana. Rama jak box danych, szerokość 648 (kolumna 728 z paddingiem 40), padding 32px 40px, gap 16. Wewnątrz: etykieta bloku, nazwa (Tytuł karty), odznaka, logo, liczba KPI (72 px) wyśrodkowane (`align-items:center`, `text-align:center`).

```html
<div style="width:728px;display:flex;flex-direction:column;align-items:center;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px"><div style="height:32px"></div><div style="width:648px;display:flex;flex-direction:column;align-items:center;gap:16px">{ZAWARTOŚĆ}</div><div style="height:32px"></div></div>
```

### Łącznik pionowy

Kiedy: między dwiema kartami wyśrodkowanymi (zależność). Linia 3×48.

```html
<div style="width:3px;height:48px;background:[[linia/karta]]"></div>
```

Kolumnę schematu układaj jako `display:flex;flex-direction:column;align-items:center;width:728px`: karta, łącznik, karta.

---

KONIEC PLIKU (meta/wersja 2026-11-17.3)
