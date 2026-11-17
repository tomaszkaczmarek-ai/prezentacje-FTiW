# Wzorce: układy treści

meta/wersja: **2026-11-17.1**

Boxy danych, tabele, pasek wskaźników i układy złożone. Tokeny są w pliku indeksu `prezentacje-v1.md`, elementy (atomy i molekuły) w `wzorce-elementy.md`, szkielet w `wzorce-szkielet.md`.

Zastępuj `[[rola]]` i `{pole}`. Twarda spacja w HTML to `&#160;` (tylko encje numeryczne). Nie zmieniaj struktury, kolejności ani odstępów w szablonie, zmieniaj tylko pola.

### Box danych – rama

Kiedy: Wyróżniony blok, 2–4 obok siebie. Układ w rzędzie: display:flex;gap:32px; dla czterech: display:grid;grid-template-columns:1fr 1fr;gap:32px.

```html
<div style="flex:1;display:flex;flex-direction:column;gap:{gap}px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:{pad}">{ZAWARTOŚĆ}</div>
```

### Box danych – Typ=Liczba

Kiedy: Jedna kluczowa liczba z jednostką i jednozdaniowym opisem. gap 20, padding 40px.

```html
<p style="font-size:24px;line-height:1.4;letter-spacing:5px;text-transform:uppercase;color:[[tekst/podstawowy]]">{etykieta}</p>
<div style="display:flex;flex-direction:row;align-items:baseline;gap:16px"><p style="font-size:96px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{liczba}</p><p style="font-size:40px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{jednostka}</p></div>
<div style="border-top:1px solid [[linia/karta]]"></div>
<p style="font-size:26px;line-height:1.4;color:[[tekst/podstawowy]]">{opis}</p>
```

### Box danych – Typ=Liczba szeroki

Kiedy: jedna kluczowa liczba na slajdzie z innymi boxami (np. pod rzędem kart), gdy w rzędzie nie ma na nią miejsca. Liczba i jednostka po lewej, pionowa kreska, jednozdaniowy opis po prawej (do 2 linii, ok. 90 znaków). Box na całą szerokość obszaru treści (1664), wysokość ok. 131. Zastępuje pas wskaźników przy jednej liczbie.

```html
<div style="display:flex;flex-direction:row;align-items:center;gap:32px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:24px 40px">
<div style="display:flex;flex-direction:row;align-items:baseline;gap:12px"><p style="font-size:72px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{liczba}</p><p style="font-size:40px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{jednostka}</p></div>
<div style="width:1px;align-self:stretch;background:[[linia/karta]]"></div>
<p style="flex:1;font-size:26px;line-height:1.35;color:[[tekst/podstawowy]]">{opis}</p>
</div>
```

### Box danych – Typ=Tekst

Kiedy: Krótki opis z etykietą, do ok. 250 znaków (jeden lub dwa akapity). gap 8, padding 32px 40px. Etykieta ma styl „Etykieta boxu” (24 px, pogrubiona, zwykłe litery, biała). Akapity w boxach jednego rzędu zaczynają się na tej samej wysokości: pole etykiety ma wysokość {wys etykiety} = liczba linii najdłuższej etykiety w rzędzie × 32 (ta sama we wszystkich boxach rzędu). Odstęp między akapitami 16. Pojemność etykiety: ok. 31 znaków w linii w rzędzie po 3 boxy, ok. 22 w rzędzie po 4, ok. 52 przy 2 boxach.

```html
<div style="height:{wys etykiety}px"><p style="font-size:24px;line-height:32px;font-weight:700;color:[[tekst/tytul]]">{etykieta}</p></div>
<div style="display:flex;flex-direction:column;gap:16px"><p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{akapit 1}</p><p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{akapit 2}</p></div>
```

### Box danych – Typ=Wyliczenie

Kiedy: Numerowana karta z tytułem i dokładnie trzema punktami. gap 16, padding 32px 48px.

```html
<div style="display:flex;flex-direction:row;align-items:center;gap:24px"><p style="font-size:56px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{nn}</p><h3 style="font-size:30px;font-weight:700;line-height:1.2;color:[[tekst/tytul]]">{tytuł}</h3></div>
<div style="display:flex;flex-direction:column">
<div style="border-top:1px solid [[linia/karta]];padding:8px 0"><p style="font-size:26px;line-height:1.3;color:[[tekst/podstawowy]]">{punkt}</p></div>
(… dokładnie trzy punkty)
</div>
```

### Box danych – Typ=Wykres

Kiedy: Struktura procentowa, do 5 wierszy. gap 16, padding 28px 40px. Najpierw etykieta bloku jak w Typ=Tekst, potem wiersze. {udział} to liczba procent szerokości paska.

```html
<div style="display:flex;flex-direction:column;gap:8px">
<div style="display:flex;flex-direction:row;align-items:center;gap:16px"><p style="width:104px;font-size:32px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{84&#160;%}</p><p style="flex:1;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{opis}</p></div>
<div style="height:8px;background:[[tlo/tor-paska]];border-radius:4px"><div style="width:{udział}%;height:8px;background:[[akcent/glowny]];border-radius:4px"></div></div>
</div>
```

### Box danych – Typ=Tekst szeroki

Kiedy: dłuższy opis na całą szerokość obszaru treści (1664 px), do ok. 370 znaków (3 linie po ok. 124 znaki). Rama i style jak Typ=Tekst, rama bez ustawionej szerokości, w kolumnie obszaru treści `align-self:stretch`. gap 8, padding 32px 40px. Wysokość ok. 172 px (2 linie) lub 205 px (3 linie).

```html
<div style="display:flex;flex-direction:column;gap:8px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:32px 40px">
<p style="font-size:24px;line-height:1.3;font-weight:600;letter-spacing:3px;text-transform:uppercase;color:[[tekst/podstawowy]]">{etykieta}</p>
<p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{treść}</p>
</div>
```

### Box danych – Typ=Wykres szeroki

Kiedy: struktura procentowa na całą szerokość, 4–6 wierszy w dwóch kolumnach (wiersze wypełniają kolumny od lewej, najpierw lewa). Każdy wiersz jak w Typ=Wykres. Opis wiersza do ok. 50 znaków w jednej linii. gap 16, padding 28px 40px. Wysokość: 4 wiersze ok. 226 px, 6 wierszy ok. 293 px.

```html
<div style="display:flex;flex-direction:column;gap:16px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:28px 40px">
<p style="font-size:24px;line-height:1.3;font-weight:600;letter-spacing:3px;text-transform:uppercase;color:[[tekst/podstawowy]]">{etykieta}</p>
<div style="display:flex;flex-direction:row;gap:32px">
<div style="flex:1;display:flex;flex-direction:column;gap:16px">{WIERSZE LEWEJ KOLUMNY}</div>
<div style="flex:1;display:flex;flex-direction:column;gap:16px">{WIERSZE PRAWEJ KOLUMNY}</div>
</div>
</div>
```

### Tabela porównawcza

Kiedy: Porównanie dwóch opcji według kryteriów; nagłówek raz, do 7 wierszy. Kolumny 433 / 566 / 665 px (razem 1664). Bez obramowań; nagłówek zaokrąglony 16 px tylko u góry na zewnętrznych krawędziach.

```html
<div style="display:flex;flex-direction:column">
<div style="display:flex;flex-direction:row">
<div style="width:433px"></div>
<div style="width:566px;display:flex;flex-direction:column;justify-content:center;background:[[tabela/naglowek-lokata]];border-radius:16px 0 0 0"><p style="padding:10px 20px;font-size:26px;line-height:1.25;font-weight:700;color:[[tekst/podstawowy]]">{nagłówek A}</p></div>
<div style="width:665px;display:flex;flex-direction:column;justify-content:center;background:[[tabela/naglowek-fundusz]];border-radius:0 16px 0 0"><p style="padding:10px 20px;font-size:26px;line-height:1.25;font-weight:700;color:[[tekst/na-limonce]]">{nagłówek B}</p></div>
</div>
<div style="display:flex;flex-direction:row;border-top:1px solid [[linia/tabela]]">
<div style="width:433px;display:flex;flex-direction:column;justify-content:center"><p style="padding:10px 20px;font-size:24px;line-height:1.25;font-weight:700;color:[[tekst/podstawowy]]">{kryterium}</p></div>
<div style="width:566px;display:flex;flex-direction:column;justify-content:center"><p style="padding:10px 20px;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{A}</p></div>
<div style="width:665px;display:flex;flex-direction:column;justify-content:center;background:[[tlo/kolumna-funduszu]]"><p style="padding:10px 20px;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{B}</p></div>
</div>
(… kolejne wiersze tak samo)
</div>
```

### Tabela porównawcza – wiersz z ikoną

Kiedy: kryterium tabeli ma ikonę (np. koszty, płynność, bezpieczeństwo). Ikona z biblioteki, w tabeli w rozmiarze 48 (zamiast 64). Wiersz zastępuje wiersz zwykły; wszystkie wiersze tabeli mają wtedy ikonę. Reszta tabeli bez zmian. Kolumna kryterium: tekst do 2 linii po ok. 24 znaki. Wysokość wiersza 72 px (1 linia) lub 85 px (2 linie); przy ikonach mieści się do 7 wierszy.

```html
<div style="display:flex;flex-direction:row;border-top:1px solid [[linia/tabela]]">
<div style="width:433px;display:flex;flex-direction:row;align-items:center"><div style="width:20px;height:1px"></div><img src="{ikona}" alt="" style="width:48px;height:48px"><p style="flex:1;padding:12px 20px 12px 16px;font-size:24px;line-height:1.25;font-weight:700;color:[[tekst/podstawowy]]">{kryterium}</p></div>
<div style="width:566px;display:flex;flex-direction:column;justify-content:center"><p style="padding:10px 20px;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{A}</p></div>
<div style="width:665px;display:flex;flex-direction:column;justify-content:center;background:[[tlo/kolumna-funduszu]]"><p style="padding:10px 20px;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{B}</p></div>
</div>
```

### Pasek wskaźników

Kiedy: 2–4 kluczowe liczby w jednym pasie na całą szerokość. Przy jednej liczbie nie używaj pasa: użyj „Box danych – Typ=Liczba” w rzędzie lub „Typ=Liczba szeroki”. Pierwsza kolumna używa szablonu „kolumna pierwsza”, kolejne „kolumna kolejna” (z pionowym separatorem). `{waga}` to szerokość kolumny względem pozostałych (domyślnie 1; kolumna z dłuższym opisem 1.3–2). Opis wskaźnika: maks. 2 linie (ok. 45 znaków w kolumnie wagi 1, ok. 90 w wagi 2). Jednostka krótka (SRI, %, miesięcy). Liczby we wszystkich kolumnach leżą na jednej linii (stała wysokość liczby 80 i opisu 60); etykietę wskaźnika zapisz pogrubioną na początku opisu.

```html
<div style="position:absolute;left:0px;top:788px;width:1920px;height:176px;background:[[tlo/pasek-wskaznikow]];display:flex;flex-direction:row;justify-content:center"><div style="width:1664px;height:176px;display:flex;flex-direction:row">
{kolumny}
</div></div>
```

Kolumna pierwsza:

```html
<div style="flex:{waga};display:flex;flex-direction:column;justify-content:center;gap:8px;padding:0 32px 0 0"><div style="height:80px;display:flex;flex-direction:row;align-items:baseline;gap:12px"><p style="font-size:72px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{liczba}</p><p style="font-size:40px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{jednostka}</p></div><div style="height:60px"><p style="font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{opis}</p></div></div>
```

Kolumna kolejna:

```html
<div style="flex:{waga};display:flex;flex-direction:column;justify-content:center;gap:8px;padding:0 32px;border-left:1px solid [[linia/karta]]"><div style="height:80px;display:flex;flex-direction:row;align-items:baseline;gap:12px"><p style="font-size:72px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{liczba}</p><p style="font-size:40px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{jednostka}</p></div><div style="height:60px"><p style="font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{opis}</p></div></div>
```

### Układ: Opis funduszu

Kiedy: dużo tekstu opisowego (2–3 sekcje, do ok. 1000 znaków) plus 2–4 wskaźniki; opcjonalnie logo partnera, QR i portret. Kolejność elementów w sekcji slajdu treści: 1) trzy smugi światła, 2) pas stopki, 3) nagłówek slajdu (nadtytuł + tytuł, szerokość 1060, odstęp ramy 24), 4) kafelek logo partnera, 5) QR z podpisem, 6) kolumna sekcji tekstowych, 7) portret, 8) pasek wskaźników, 9) logo i numer strony. Elementy opcjonalne pomijaj, jeśli nie ma ich w materiale; pozostałe zostają na swoich miejscach. Rama slajdu jak „Slajd treści (rama)”, ale z `gap:24px` zamiast `gap:0px` (wyjątek od sekcji „Odstępy i obszar treści”: ten układ nie używa szablonu obszaru treści, a kolumna tekstu płynie pod nagłówkiem).

### Układ: Diagram cyklu

Kiedy: proces, który się powtarza lub zamyka w pętlę (4 etapy wokół wspólnego środka), plus tekst wyjaśniający. Pola: tekst po lewej (nagłówek sekcji i akapit, do 500 znaków, ok. 47 znaków w linii), 4 etapy (tytuł do 16 znaków, opis do 2 linii po 22 znaki), opcjonalnie środek (tytuł do 16 znaków, opis do 2 linii). Etapy układaj zgodnie z kierunkiem czytania: góra, prawo, dół, lewo. Łączniki w narożnikach to łuki ze strzałką, które łączą sąsiednie karty i pokazują kierunek obiegu (pliki lacznik-* z biblioteki ikon, limonka, 328×192, jeden na narożnik). Bez środka pole środkowe zostaje puste. Dla 3 lub 5 etapów albo cyklu bez strzałek użyj najbliższego wzorca i zgłoś brak. Diagram wypełnia całą wysokość obszaru treści (wyjątek od zasady „boxy nie są rozciągane”), tekst po lewej wyśrodkuj w pionie.

Diagram to siatka 3×3: trzy kolumny po 328 i odstęp 16 (razem 1016), narożniki zajmują łączniki 328×192. Wiersze mają stałą wysokość 192, diagram 608. Tekst 600, odstęp 48.

```html
<div style="position:absolute;left:128px;top:304px;width:1664px;height:616px;display:flex;flex-direction:row;align-items:center;gap:48px">
<div style="width:600px;display:flex;flex-direction:column;gap:20px">{SEKCJE TEKSTOWE}</div>
<div style="width:1016px;height:608px;display:flex;flex-direction:column;gap:16px">
<div style="height:192px;display:flex;flex-direction:row;align-items:stretch;gap:16px">{ŁĄCZNIK gora-lewo}{KARTA 1}{ŁĄCZNIK gora-prawo}</div>
<div style="height:192px;display:flex;flex-direction:row;align-items:stretch;gap:16px">{KARTA 4}{KARTA ŚRODKA}{KARTA 2}</div>
<div style="height:192px;display:flex;flex-direction:row;align-items:stretch;gap:16px">{ŁĄCZNIK dol-lewo}{KARTA 3}{ŁĄCZNIK dol-prawo}</div>
</div>
</div>
```

Karta etapu (328 szerokości, tekst wyśrodkowany w poziomie i w pionie, wiersz 192, treść wyśrodkowana w pionie; kolejność wiersza środkowego: etap 4 po lewej, środek, etap 2 po prawej):

```html
<div style="width:328px;display:flex;flex-direction:row;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px"><div style="width:24px"></div><div style="width:280px;display:flex;flex-direction:column;justify-content:center;align-items:center;gap:8px"><p style="font-size:30px;font-weight:700;line-height:1.2;text-align:center;color:[[tekst/tytul]]">{tytuł}</p><p style="font-size:24px;line-height:1.35;text-align:center;color:[[tekst/podstawowy]]">{opis}</p></div><div style="width:24px"></div></div>
```

Karta środka (tło limonkowe, tekst ciemny, bez górnej kreski):

```html
<div style="width:328px;display:flex;flex-direction:row;background:[[akcent/glowny]];border-radius:40px"><div style="width:24px"></div><div style="width:280px;display:flex;flex-direction:column;justify-content:center;align-items:center;gap:8px"><p style="font-size:30px;font-weight:700;line-height:1.2;text-align:center;color:[[tekst/na-limonce]]">{tytuł}</p><p style="font-size:24px;line-height:1.35;text-align:center;color:[[tekst/na-limonce]]">{opis}</p></div><div style="width:24px"></div></div>
```

Komórka łącznika (plik z biblioteki, limonka, 328×192):

```html
<img src="{łącznik}" alt="" style="width:328px;height:192px">
```

Pusty narożnik (brak środka lub pusta komórka): `<div style="width:328px"></div>`.

### Układ: Opis i grafika

Kiedy: tekst opisowy i jedna grafika ze źródła (zrzut ekranu, schemat, ilustracja, infografika, nie zdjęcie stockowe). Pola: sekcje tekstowe (2 sekcje, do 600 znaków), grafika, opcjonalnie podpis grafiki (jedna linia, 24 px, poniżej grafiki). Tekst po lewej, grafika po prawej; cały blok wyśrodkowany w pionie względem obszaru treści. Grafika nie ma ramki ani tła (ramka z limonkową linią jest tylko dla portretów) i nigdy nie jest przycinana. Wymiary: przeskaluj grafikę z zachowaniem proporcji tak, by mieściła się w 840×616, i wpisz wyliczone szer i wys (zaokrąglone). Węższa grafika zostaje przy lewej krawędzi kolumny.

```html
<div style="position:absolute;left:128px;top:304px;width:1664px;height:616px;display:flex;flex-direction:row;align-items:center;gap:64px">
<div style="width:760px;display:flex;flex-direction:column;gap:20px">{SEKCJE TEKSTOWE}</div>
<div style="width:840px;display:flex;flex-direction:column;gap:16px">
<img src="{grafika}" alt="{opis}" style="width:{szer}px;height:{wys}px;border-radius:24px;object-fit:contain">
{PODPIS: <p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{podpis}</p>}
</div>
</div>
```

Pojemność tekstu: kolumna 760 daje ok. 59 znaków w linii, do 12 linii akapitów.

### Układ: Grafiki z podpisem

Kiedy: 2–3 grafiki obok siebie (ekrany aplikacji, produkty, dokumenty), każda z podpisem. Pola: grafika, tytuł podpisu (do 1 linii), opis (opcjonalny, do 2 linii). Wszystkie pola grafik w rzędzie mają tę samą wysokość {wys}, grafika jest w polu wyśrodkowana, bez ramki i tła: 2 grafiki szerokość 816, wys 420; 3 grafiki szerokość 533, wys 320. Dla grafik wyższych niż szerokie zwiększ wys do 480 (2 grafiki) lub 400 (3 grafiki). Grafika nigdy nie jest przycinana. Blok wyśrodkuj w pionie względem obszaru treści (szablon rzędu boxów).

```html
<div style="display:flex;flex-direction:row;gap:32px">{KOLUMNA 1}{KOLUMNA 2}{KOLUMNA 3}</div>
```

Kolumna (szer = 816 lub 533):

```html
<div style="width:{szer}px;display:flex;flex-direction:column;gap:16px">
<img src="{grafika}" alt="{opis}" style="width:{szer}px;height:{wys}px;object-fit:contain">
<p style="font-size:26px;font-weight:700;line-height:1.25;color:[[tekst/tytul]]">{tytuł podpisu}</p>
<p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{opis}</p>
</div>
```

Pojemność: tytuł podpisu 1 linia (2 grafiki ok. 59 znaków, 3 grafiki ok. 38), opis 2 linie (2 grafiki po 64 znaki, 3 grafiki po 41 znaków).

### Układ: Sekcje w dwóch kolumnach

Kiedy: 4–6 sekcji tekstowych z nagłówkami, bez grafik i liczb (opis oferty, zasad, zespołu). Przy 2–3 sekcjach użyj „Sekcja tekstowa” w jednej kolumnie. Kolejność czytania: lewa kolumna od góry, potem prawa. Podział: zachowaj kolejność i podziel sekcje tak, by kolumny miały zbliżoną wysokość (przy nieparzystej liczbie lewa ma więcej sekcji lub dłuższe teksty tak, by różnica wysokości była najmniejsza). Pojemność kolumny 816: ok. 64 znaków w linii, do 3 sekcji, akapit do 4 linii (ok. 250 znaków). Blok wyśrodkuj w pionie, gdy jest niższy niż 70% obszaru (sekcja „Odstępy i obszar treści”), inaczej od góry.

```html
<div style="position:absolute;left:128px;top:304px;width:1664px;height:616px;display:flex;flex-direction:column;justify-content:{center albo flex-start}">
<div style="display:flex;flex-direction:row;align-items:flex-start;gap:32px">
<div style="width:816px;display:flex;flex-direction:column;gap:20px">{SEKCJE LEWEJ KOLUMNY}</div>
<div style="width:816px;display:flex;flex-direction:column;gap:20px">{SEKCJE PRAWEJ KOLUMNY}</div>
</div>
</div>
```

Sekcja: szablon z „Sekcja tekstowa” (plik elementów).

---

KONIEC PLIKU (meta/wersja 2026-11-17.1)
