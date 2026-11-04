# Design system prezentacji

meta/wersja: **2026-11-04.13**

meta/zmiana: Usunięte sprzeczności: odstęp nagłówek–treść 64 (ramka bez gap), skracanie a dobór układu, zakres skali odstępów, rozmiary ikon, reguły ogólne ze źródłem. Wcześniej: Atom „Źródło w stopce”. Wcześniej: Molekuły „Wiersz listy z ikoną”, „Łącznik pionowy”, „Karta wyśrodkowana” (schemat spółka matka–spółka zależna). Wcześniej: Molekuły „Wiersz składnika” (mały kafelek logo + nazwa) i „Tabela wyników (okresy)”. Wcześniej: Szerokie boxy (Tekst, Wykres w dwóch kolumnach). Wcześniej: Przekładka (zdjęcie, numer części, tytuł) i wiersz tabeli z ikoną. Wcześniej: Ściana logo partnerów (wzorzec i 19 plików logo przyciętych do znaku, folder logo-partnerow). Wcześniej: Nadtytuł (dawniej „eyebrow”), nagłówek stałej wysokości 112 (tytuł 56 lub 48), sekcja „Odstępy i obszar treści” (skala, centrowanie, pojemności), molekuły: karta osoby, ikona z opisem, kolumna z ikoną i listą. Wcześniej: dodane atomy (ikony, punktor, znak plus, odznaka, karta szklana, ramka zdjęcia 2 px), zasady zdjęć i wykresów. Wcześniej: Kolor pasa wskaźników zmieniony na ciemniejszy z palety (rgba(17,46,23,0.75)). Wcześniej: Dodana zasada „Układ ze źródła” (pierwszeństwo przed doborem układu, gdy użytkownik załączył slajd źródłowy). Wcześniej: dodane zasady zasobów ze źródła i mapowania slajdów 1:1. Wcześniej: dodane elementy i układ „Opis funduszu” (kafelek logo partnera, QR z podpisem, sekcje tekstowe, portret w kółku, pasek wskaźników, stopka z pasem) oraz zasady doboru układu. Wcześniej: Okładka slajdu. Poprzednio: zamknięta paleta (6 kolorów), wzorce: nagłówek, stopka, boxy danych, wykres poziomy, tabela.

Źródło wartości: ten plik jest jedynym źródłem wyglądu prezentacji dla skilla. Wartości przepisuj dosłownie, niczego nie zaokrąglaj i nie dopisuj.

## 1. Role kolorów

W szablonach zastępuj `[[rola]]` wartością z tabeli. `[[rola@0]]` to ten sam kolor RGB z kryciem 0. Kolor jest dozwolony tylko, jeśli ma tu rolę. Nieużywane kolory marki: #447B3A, #595246, #D8D3CA, #2AABE2, #2A034E, #EC6608.

| Rola | Wartość | Zastosowanie |
|---|---|---|
| tlo/tresc | #284833 | tło slajdu treści |
| tlo/okladka | #112E17 | tło okładki |
| tlo/karta | #112E17 | tło kart (boxów danych) |
| tlo/kafelek-logo | #FFFFFF | biały kafelek pod logo partnera |
| tlo/tor-paska | #34493D | tor paska wykresu |
| tlo/smuga-mocna | rgba(247,252,246,0.12) | smuga światła, mocna |
| tlo/smuga-slaba | rgba(247,252,246,0.06) | smuga światła, słaba |
| tlo/winieta | rgba(17,46,23,0.22) | winieta |
| tlo/kolumna-funduszu | rgba(17,46,23,0.75) | tło kolumny B w tabeli |
| tabela/naglowek-lokata | #34493D | nagłówek kolumny A tabeli |
| tabela/naglowek-fundusz | #C0D436 | nagłówek kolumny B tabeli |
| tekst/podstawowy | #F7FCF6 | tekst podstawowy |
| tekst/tytul | #FFFFFF | tytuły |
| tekst/na-limonce | #112E17 | tekst na limonkowym tle |
| akcent/glowny | #C0D436 | akcent (limonka z logo) |
| linia/tabela | rgba(192,212,54,0.35) | linie tabeli |
| linia/karta | rgba(247,252,246,0.45) | linie w kartach |
| linia/ramka-okladki | rgba(192,212,54,0.55) | ramka okładki |
| tlo/pasek-wskaznikow | rgba(17,46,23,0.75) | pas wskaźników na całą szerokość slajdu (to samo co tlo/kolumna-funduszu) |
| tlo/stopka-pas | #112E17 | ciemny pas stopki |

## 2. Wymiary (px)

| Nazwa | Wartość |
|---|---|
| Płótno | 1920×1080 px |
| margines/boki-gora | 128 |
| margines/dol | 160 |
| stopka/odstep-od-dolu | 64 |
| promien/karta | 40 |
| promien/karta-allianz | 32 |
| promien/pasek-info | 29 |
| promien/naglowek-tabeli | 16 |
| promien/kafelek-logo | 14 |
| promien/kafelek-qr | 12 |
| promien/tor-paska | 4 |
| linia/gorna-karty | 4 |
| linia/tabeli | 1 |
| odstęp liter nadtytułu | 5 |
| odstep liter etykieta | 3 |
| odstęp nagłówek–treść | 64 (treść zaczyna się w y=304; wyjątek: układ Opis funduszu ma własny odstęp 24) |
| kafelek logo partnera | 360×112, promień 14 |
| kafelek QR | 144×144, promień 12 |
| portret w kółku | średnica 288 (zdjęcie 284 + ramka 2 px w kolorze akcent/glowny) |
| promien/zdjecie | 24 (prostokątna ramka zdjęcia) |
| linia/ramka-zdjecia | 2 (limonka) |
| pas wskaźników | wysokość 176, od y=788 do 964 |
| pas stopki | wysokość 116, od y=964 |

## 3. Typografia

Font: Montserrat. Face: https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap . Minimalny rozmiar tekstu 24 px. Używaj wyłącznie tych stylów.

| Styl | Rozmiar px | Waga | Interlinia | Dodatkowo |
|---|---|---|---|---|
| Okładka – tytuł | 84 | 700 | 1,1 |  |
| Liczba duża | 96 | 700 | 1,1 |  |
| Liczba KPI | 72 | 700 | 1,1 |  |
| Tytuł slajdu | 56 | 700 | 1,1 |  |
| Tytuł slajdu – kompaktowy | 48 | 700 | 1,1 | gdy tytuł nie mieści się w jednej linii w rozmiarze 56 |
| Jednostka | 40 | 700 | 1,1 |  |
| Podtytuł | 32 | 400 | 1,3 |  |
| Podtytuł – pogrubiony | 32 | 700 | 1,3 |  |
| Tytuł karty | 30 | 700 | 1,2 |  |
| Tekst karty | 26 | 400 | 1,35 |  |
| Tekst karty – pogrubiony | 26 | 700 | 1,25 |  |
| Tekst | 24 | 400 | 1,35 |  |
| Tekst – pogrubiony | 24 | 700 | 1,3 |  |
| Nadtytuł | 24 | 400 | 1,4 | wielkie litery, odstęp 5 |
| Etykieta bloku | 24 | 600 | 1,3 | wielkie litery, odstęp 3 |

## 4. Wzorce (szablony HTML)

Zastępuj `[[rola]]` i `{pole}`. Twarda spacja w HTML to `&#160;` (tylko encje numeryczne). Nie zmieniaj struktury, kolejności ani odstępów, zmieniaj tylko pola. Brak pasującego wzorca: zgłoś w raporcie, nie improwizuj.

### Slajd treści (rama)

Kiedy: Każdy slajd poza okładką. Kąt światła {kat}: 120, 60, 150, 180, potem od nowa.

```html
<section id="{id}" style="background:[[tlo/tresc]];color:[[tekst/podstawowy]];font-family:'Montserrat', Arial, sans-serif;padding:128px 128px 160px;display:flex;flex-direction:column;gap:0px">
<div style="position:absolute;left:0px;top:0px;width:1920px;height:1080px;background:linear-gradient({kat}deg, [[tlo/smuga-mocna@0]] 0%, [[tlo/smuga-mocna@0]] 28%, [[tlo/smuga-mocna]] 46%, [[tlo/smuga-mocna@0]] 64%, [[tlo/smuga-mocna@0]] 100%)"></div>
<div style="position:absolute;left:0px;top:0px;width:1920px;height:1080px;background:linear-gradient({kat}deg, [[tlo/smuga-slaba@0]] 0%, [[tlo/smuga-slaba@0]] 52%, [[tlo/smuga-slaba]] 62%, [[tlo/smuga-slaba@0]] 72%, [[tlo/smuga-slaba@0]] 100%)"></div>
<div style="position:absolute;left:0px;top:0px;width:1920px;height:1080px;background:radial-gradient(ellipse at 50% 50%, [[tlo/winieta@0]] 45%, [[tlo/winieta]] 100%)"></div>
{NAGŁÓWEK}
{TREŚĆ}
{STOPKA}
<aside>{notatki: skróty; wersja design systemu}</aside>
</section>
```

### Nagłówek slajdu

Kiedy: Początek każdego slajdu treści. Pola: nadtytuł (krótka etykieta nad tytułem, obowiązkowy: jeśli brief go nie podaje, wyprowadź z nazwy sekcji lub prezentacji), tytuł (jedna linia). Nagłówek ma stałą wysokość 112 px niezależnie od rozmiaru tytułu, żeby treść pod nim zawsze zaczynała się w tym samym miejscu. Tytuł do 52 znaków w rozmiarze 56, 53–61 znaków w rozmiarze 48 (styl „Tytuł slajdu – kompaktowy”), dłuższy skróć i wpisz do raportu. Wyjątek: układ „Opis funduszu” ma własny nagłówek (szerokość 1060, do 2 linii).

```html
<div style="display:flex;flex-direction:column;gap:16px;height:112px">
<p style="font-size:24px;line-height:1.4;letter-spacing:5px;text-transform:uppercase;color:[[tekst/podstawowy]]">{nadtytuł}</p>
<h2 style="font-size:56px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{tytuł}</h2>
</div>
```

### Stopka slajdu

Kiedy: Każdy slajd treści. Pola: numer strony (dwie cyfry). Logo jako zasób wgrany przez użytkownika.

```html
<img src="{logo}" alt="Logo" style="position:absolute;left:128px;bottom:64px;width:274px;height:20px;object-fit:contain">
<p style="position:absolute;right:128px;bottom:64px;width:200px;font-size:24px;line-height:1.2;text-align:right;color:[[tekst/podstawowy]]">{nn}</p>
```

### Źródło w stopce

Kiedy: slajd ma podane źródło danych lub odnośnik do rejestru. Pole: tekst „Źródło: …” (do ok. 70 znaków, 1 linia). Stoi w stopce obok logo, na dole, w tej samej linii co numer strony. Odnośnik z oryginału zachowaj (adres w raporcie, jeśli Slajdy go nie przyjmują).

```html
<p style="position:absolute;left:520px;bottom:64px;width:927px;font-size:24px;line-height:1.2;color:[[tekst/podstawowy]]">Źródło: <u>{tekst źródła}</u></p>
```

### Box danych – rama

Kiedy: Wyróżniony blok, 2–4 obok siebie. Układ w rzędzie: display:flex;gap:32px; dla czterech: display:grid;grid-template-columns:1fr 1fr;gap:32px.

```html
<div style="flex:1;display:flex;flex-direction:column;gap:{gap}px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:{pad}">{ZAWARTOŚĆ}</div>
```

### Box danych – Typ=Liczba

Kiedy: Jedna kluczowa liczba z jednostką i jednozdaniowym opisem. gap 20, padding 40px.

```html
<p style="font-size:24px;line-height:1.4;letter-spacing:5px;text-transform:uppercase;color:[[tekst/podstawowy]]">{etykieta}</p>
<div style="display:flex;flex-direction:row;align-items:baseline;gap:16px"><p style="font-size:96px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{liczba}</p><p style="font-size:40px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{jednostka}</p></div>
<div style="border-top:1px solid [[linia/karta]]"></div>
<p style="font-size:26px;line-height:1.4;color:[[tekst/podstawowy]]">{opis}</p>
```

### Box danych – Typ=Tekst

Kiedy: Krótki opis z etykietą, do ok. 250 znaków. gap 8, padding 32px 40px.

```html
<p style="font-size:24px;line-height:1.3;font-weight:600;letter-spacing:3px;text-transform:uppercase;color:[[tekst/podstawowy]]">{etykieta}</p>
<p style="font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{treść}</p>
```

### Box danych – Typ=Wyliczenie

Kiedy: Numerowana karta z tytułem i dokładnie trzema punktami. gap 16, padding 32px 48px.

```html
<div style="display:flex;flex-direction:row;align-items:center;gap:24px"><p style="font-size:56px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{nn}</p><h3 style="font-size:30px;font-weight:700;line-height:1.2;color:[[tekst/tytul]]">{tytuł}</h3></div>
<div style="display:flex;flex-direction:column">
<div style="border-top:1px solid [[linia/karta]];padding:8px 0"><p style="font-size:26px;line-height:1.3;color:[[tekst/podstawowy]]">{punkt}</p></div>
(… dokładnie trzy punkty)
</div>
```

### Box danych – Typ=Wykres

Kiedy: Struktura procentowa, do 5 wierszy. gap 16, padding 28px 40px. Najpierw etykieta bloku jak w Typ=Tekst, potem wiersze. {udział} to liczba procent szerokości paska.

```html
<div style="display:flex;flex-direction:column;gap:8px">
<div style="display:flex;flex-direction:row;align-items:center;gap:16px"><p style="width:104px;font-size:32px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{84&#160;%}</p><p style="flex:1;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{opis}</p></div>
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
<div style="width:393px;display:flex;flex-direction:row;align-items:center;gap:16px;padding:12px 20px"><img src="{ikona}" alt="" style="width:48px;height:48px"><p style="font-size:24px;line-height:1.25;font-weight:700;color:[[tekst/podstawowy]]">{kryterium}</p></div>
<div style="width:566px;display:flex;flex-direction:column;justify-content:center"><p style="padding:10px 20px;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{A}</p></div>
<div style="width:665px;display:flex;flex-direction:column;justify-content:center;background:[[tlo/kolumna-funduszu]]"><p style="padding:10px 20px;font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{B}</p></div>
</div>
```

### Okładka slajdu

Kiedy: Wyłącznie pierwszy slajd. Pola: nadtytuł, tytuł (max 2 linie), podtytuł (1 linia), zdjęcie pełnoekranowe, logo. Bez smug światła i stopki. Tekst zawsze po lewej.

```html
<section id="cover" style="background:[[tlo/okladka]]">
<img src="{zdjęcie}" alt="{opis}" style="position:absolute;top:0;left:0;width:1920px;height:1080px;object-fit:cover">
<div style="position:absolute;top:0;left:0;width:1920px;height:1080px;display:flex;flex-direction:column;background:linear-gradient(90deg, rgba(17,46,23,0.97) 0%, rgba(17,46,23,0.86) 48%, rgba(17,46,23,0.22) 100%)"></div>
<div style="position:absolute;top:48px;left:48px;width:1824px;height:984px;display:flex;flex-direction:column;border:1px solid [[linia/ramka-okladki]]"></div>
<img src="{logo}" alt="Logo" style="position:absolute;top:120px;left:128px;width:374px;height:28px;object-fit:contain">
<p style="position:absolute;top:405px;left:128px;width:1280px;font-size:24px;line-height:1.4;letter-spacing:5px;text-transform:uppercase;color:[[tekst/podstawowy]]">{nadtytuł}</p>
<div style="position:absolute;top:469px;left:128px;width:120px;height:4px;background:[[akcent/glowny]]"></div>
<h1 style="position:absolute;top:505px;left:128px;width:1470px;font-size:84px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{tytuł}</h1>
<p style="position:absolute;top:824px;left:128px;width:1210px;font-size:32px;line-height:1.4;color:[[tekst/podstawowy]]">{podtytuł}</p>
<aside>Wersja design systemu: {meta/wersja}</aside>
</section>
```

### Przekładka

Kiedy: początek nowej części prezentacji (rozdział), zwykle co kilka slajdów. Pola: numer części (dwie cyfry), tytuł (max 2 linie), podtytuł (opcjonalny, 1 linia), zdjęcie pełnoekranowe, logo, numer strony. Zdjęcie z pliku użytkownika (sekcja „Zdjęcia i wykresy”); bez zdjęcia użyj gładkiego tła tlo/okladka. Zdjęcie jest widoczne w całości (tylko lekka winieta), a tekst leży na karcie szklanej. Dzięki temu przekładka wyraźnie różni się od okładki (ciemny gradient z lewej, ramka). Bez smug światła.

```html
<section id="divider" style="background:[[tlo/okladka]]">
<img src="{zdjęcie}" alt="{opis}" style="position:absolute;top:0;left:0;width:1920px;height:1080px;object-fit:cover">
<div style="position:absolute;top:0;left:0;width:1920px;height:1080px;display:flex;flex-direction:column;background:[[tlo/winieta]]"></div>
<div style="position:absolute;top:330px;left:128px;width:988px;display:flex;flex-direction:column;gap:16px;background:[[tlo/kolumna-funduszu]];border-radius:40px;padding:48px 56px">
<p style="font-size:96px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{nn}</p>
<div style="width:120px;height:4px;background:[[akcent/glowny]]"></div>
<h1 style="font-size:56px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{tytuł}</h1>
<p style="font-size:32px;line-height:1.3;color:[[tekst/podstawowy]]">{podtytuł}</p>
</div>
<img src="{logo}" alt="Logo" style="position:absolute;left:128px;bottom:64px;width:274px;height:20px;object-fit:contain">
<p style="position:absolute;right:128px;bottom:64px;width:200px;font-size:24px;line-height:1.2;text-align:right;color:[[tekst/podstawowy]]">{nn strony}</p>
<aside>Wersja design systemu: {meta/wersja}</aside>
</section>
```

Pojemność tytułu: 2 linie po ok. 31 znaków (56 px pogrubiony, szerokość 988 px w karcie), do ok. 60 znaków łącznie; dłuższy skróć i wpisz do raportu. Podtytuł: 1 linia do ok. 55 znaków. Karta ma wysokość naturalną (ok. 420 px przy tytule 2-liniowym i podtytule).

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
<img src="{portret}" alt="{osoba}" style="position:absolute;left:1504px;top:440px;width:284px;height:284px;border:2px solid [[akcent/glowny]];border-radius:144px;object-fit:cover">
```

### Pasek wskaźników

Kiedy: 2–4 kluczowe liczby w jednym pasie na całą szerokość. Pierwsza kolumna używa szablonu „kolumna pierwsza”, kolejne „kolumna kolejna” (z pionowym separatorem). `{waga}` to szerokość kolumny względem pozostałych (domyślnie 1; kolumna z dłuższym opisem 1.3–2). Opis wskaźnika: maks. 2 linie (ok. 45 znaków w kolumnie wagi 1, ok. 90 w wagi 2). Jednostka krótka (SRI, %, miesięcy).

```html
<div style="position:absolute;left:0px;top:788px;width:1664px;height:176px;padding:0 128px;background:[[tlo/pasek-wskaznikow]];display:flex;flex-direction:row">
{kolumny}
</div>
```

Kolumna pierwsza:

```html
<div style="flex:{waga};display:flex;flex-direction:column;justify-content:center;gap:8px;padding:0 32px 0 0"><div style="display:flex;flex-direction:row;align-items:baseline;gap:12px"><p style="font-size:72px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{liczba}</p><p style="font-size:40px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{jednostka}</p></div><p style="font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{opis}</p></div>
```

Kolumna kolejna:

```html
<div style="flex:{waga};display:flex;flex-direction:column;justify-content:center;gap:8px;padding:0 32px;border-left:1px solid [[linia/karta]]"><div style="display:flex;flex-direction:row;align-items:baseline;gap:12px"><p style="font-size:72px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{liczba}</p><p style="font-size:40px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{jednostka}</p></div><p style="font-size:24px;line-height:1.25;color:[[tekst/podstawowy]]">{opis}</p></div>
```

### Stopka z pasem

Kiedy: układy z paskiem wskaźników (pas stopki idzie zaraz za tłem smug, przed treścią). Pas, potem logo i numer jak w „Stopka slajdu”.

```html
<div style="position:absolute;left:0px;top:964px;width:1920px;height:116px;background:[[tlo/stopka-pas]]"></div>
```

### Układ: Opis funduszu

Kiedy: dużo tekstu opisowego (2–3 sekcje, do ok. 1000 znaków) plus 2–4 wskaźniki; opcjonalnie logo partnera, QR i portret. Kolejność elementów w sekcji slajdu treści: 1) trzy smugi światła, 2) pas stopki, 3) nagłówek slajdu (nadtytuł + tytuł, szerokość 1060, odstęp ramy 24), 4) kafelek logo partnera, 5) QR z podpisem, 6) kolumna sekcji tekstowych, 7) portret, 8) pasek wskaźników, 9) logo i numer strony. Elementy opcjonalne pomijaj, jeśli nie ma ich w materiale; pozostałe zostają na swoich miejscach. Rama slajdu jak „Slajd treści (rama)”, ale z `gap:24px` zamiast `gap:0px` (wyjątek od sekcji „Odstępy i obszar treści”: ten układ nie używa szablonu obszaru treści, a kolumna tekstu płynie pod nagłówkiem).

## 5. Dobór układu

- **Dużo tekstu opisowego i kilka liczb:** układ „Opis funduszu”. Pojemność: patrz opisy elementów. Pełny tekst zachowaj, jeśli mieści się; jeśli nie, skróć minimalnie i wpisz do raportu.
- **Wiele krótkich faktów (do ok. 35 słów na pole):** siatka kart (box danych).
- **Porównanie dwóch opcji według kryteriów:** tabela porównawcza.
- **Jedna liczba lub struktura procentowa:** box danych Liczba lub Wykres.
- **Nic nie ginie:** każdy element źródła (zdjęcie, QR, link, logo, podpis) musi dostać miejsce na slajdzie. Jeśli żaden układ nie ma na niego miejsca, zgłoś to użytkownikowi przed budową slajdu, zamiast go pomijać.
- **Układ dobieraj do treści, nie treść do układu.** Nie skracaj tekstu tylko dlatego, że wybrany układ jest za ciasny; wybierz układ o większej pojemności.

## 6. Zasoby ze źródła i mapowanie slajdów

- **Jeden slajd źródła = jeden slajd wyniku.** Nie dziel slajdu na dwa i nie łącz dwóch w jeden bez wyraźnej prośby użytkownika. Jeśli treść nie mieści się w żadnym układzie, zgłoś to i zapytaj, zamiast dzielić.
- **Zasoby graficzne bierz ze źródła, nie rezygnuj z nich.** Gdy użytkownik załączył prezentację (.pptx): rozpakuj plik (to archiwum zip), obrazy są w `ppt/media/`, a które należą do danego slajdu, wskazuje `ppt/slides/_rels/slideN.xml.rels`. Zdjęcia, logo, kody QR i portrety przypisz do miejsc układu (kafelek logo partnera, QR, portret) i wgraj do talii. Pliki SVG i PNG są dopuszczalne.
- **Brak zasobu w źródle:** zostaw w układzie wyraźne puste miejsce lub pomiń element opcjonalny, ale zgłoś to w raporcie. Nie dopisuj zdjęć z internetu.
- **Raport musi wymieniać:** które elementy źródła (zdjęcie, QR, link, logo, podpis) trafiły na slajd, a które nie i dlaczego.
- **Struktura procentowa to wykres.** Udziały procentowe (np. struktura portfela) pokaż jako box Wykres lub wykres poziomy, a nie jako zdanie w boxie Tekst.

## 7. Układ ze źródła (ma pierwszeństwo przed sekcją 5)

Gdy użytkownik załączył slajd źródłowy (.pptx, PDF, obraz), ma dostać slajd o tym samym układzie, który sobie wymyślił, w naszej szacie graficznej. Wygląd (kolory, fonty, elementy) bierzesz z systemu, a **rozmieszczenie elementów ze źródła**. Sekcja 5 „Dobór układu” obowiązuje tylko wtedy, gdy nie ma slajdu źródłowego.

1. **Odczytaj układ źródła.** W pptx odczytaj pozycje i rozmiary kształtów slajdu (`a:off`, `a:ext` w EMU; rozmiar slajdu w `ppt/presentation.xml`, `p:sldSz`) i przelicz na płótno 1920×1080 (x_px = x_EMU / szerokość_slajdu_EMU × 1920, analogicznie y). W PDF lub obrazie opisz strefy z podglądu. Zapisz listę elementów: rodzaj (tytuł, tekst, obraz, liczba, tabela, wykres), strefa i kolejność czytania.
2. **Sprawdź, czy pasuje programowany układ.** Układ z tego pliku (np. „Opis funduszu”, siatka kart, tabela) jest użyteczny tylko wtedy, gdy (a) każdy element źródła ma w nim miejsce i (b) rozmieszczenie stref jest takie samo jak w źródle (te same grupy w tych samych częściach slajdu). Jeśli tak, użyj go i wypełnij pola.
3. **Jeśli nie pasuje, odtwórz układ ze źródła.** Zachowaj strefy, ich kolejność, grupowanie i proporcje z źródła. Zrób to elementami z tego pliku (kafelek logo, box danych, sekcja tekstowa, wykres, tabela, pas wskaźników) w ich rozmiarach i stylach, a brakujące elementy jako zwykłe bloki tekstu w stylach ze skali typografii. Pozycje dopasuj do marginesów 128 px (boki, góra) i 160 px (dół) oraz do odstępów systemu.
4. **Czego nie wolno bez prośby użytkownika:** dzielić slajdu na dwa, łączyć dwóch w jeden, przenosić elementu do innej strefy, zmieniać kolejności, zamieniać typu elementu (np. liczba ze źródła w kartę tekstową, tekst ze wskaźnikami w tabelę). Jeśli element ze źródła nie mieści się w układzie (np. za długi tekst), najpierw skróć tekst, nie zmieniaj układu; jeśli to nie wystarcza, zapytaj.
5. **Reguły ogólne obowiązują też ze źródłem:** zdjęcia w tle tylko na okładce i przekładkach (sekcja 11; tło ze zdjęciem na slajdzie treści zastąp tłem treści i wpisz do raportu), paleta i skala typografii z systemu, obszar treści z sekcji 10 (y 304–920).
6. **Raport:** napisz, którą drogą poszedłeś (programowany układ albo odtworzenie ze źródła) i wymień odstępstwa od źródła (przesunięte elementy, skrócone teksty, brakujące zasoby).

## 8. Atomy

Najmniejsze elementy, z których składają się molekuły i układy.

### Ikony

Jeden styl: linia 1,75, końce i łączenia zaokrąglone, bez wypełnienia, jeden kolor. Używaj wyłącznie ikon z poniższej listy, wybierając według znaczenia; nie rysuj i nie przenoś ikon ze źródła. Dwa warianty koloru: `limonka` (na ciemnych kartach i tle, kolor akcent/glowny) oraz `ciemne` (na limonkowym tle, kolor tekst/na-limonce). Domyślny rozmiar 64×64 px; w wierszu listy 40×40, w wierszu tabeli 48×48 (inne rozmiary niedozwolone). Pliki SVG:

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

Kiedy: zdjęcie osoby lub ilustracja w treści. Limonkowa linia 2 px. Kółko (średnica {d}, zdjęcie {d} minus 4 px, promień połowa d) lub prostokąt (promień 24 px).

```html
<img src="{zdjęcie}" alt="{opis}" style="width:{d-4}px;height:{d-4}px;border:2px solid [[akcent/glowny]];border-radius:{d/2}px;object-fit:cover">
```

```html
<img src="{zdjęcie}" alt="{opis}" style="width:{szer-4}px;height:{wys-4}px;border:2px solid [[akcent/glowny]];border-radius:24px;object-fit:cover">
```

## 9. Molekuły

Gotowe połączenia atomów. Wszystkie stoją w ramie box danych (cienka limonkowa kreska u góry) i mają wysokość naturalną, bez rozciągania. Szerokość boxu w rzędzie: 2 boxy 816, 3 boxy 533, 4 boxy 392 (odstęp 32). Pojemności liczone dla Montserrat (średnio 12,7 px na znak w 24 px; 13,8 w 26 px; 16,8 w 30 px pogrubionym; 16,2 w 24 px półpogrubionym z odstępem 3).

### Karta osoby

Kiedy: zarządzający, zespół, doradcy: 2–4 osoby obok siebie. Pola: zdjęcie (kwadrat), imię i nazwisko, rola, opis. Zdjęcie w kółku średnicy 200 (zdjęcie 196 + ramka 2 px).

```html
<div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:16px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:40px">
<img src="{zdjęcie}" alt="{imię i nazwisko}" style="width:196px;height:196px;border:2px solid [[akcent/glowny]];border-radius:100px;object-fit:cover">
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

Kiedy: lista partnerów, dystrybutorów lub towarzystw (do 20 logo). Pola: logo z biblioteki (poniżej), nadtytuł i tytuł nagłówka. Logo bierz z biblioteki, nie z pamięci; logo spoza biblioteki wgraj od użytkownika. Kolejność alfabetyczna, chyba że brief mówi inaczej. Pięć kafli w rzędzie, ostatni niepełny rząd wyśrodkowany. Kafel 307×112 (padding 20, pole kafla 267×72, logo w polu 227×64 (object-fit contain), promień 14, tło tlo/kafelek-logo), odstęp 32. Rzędy: 1–5 logo 1 rząd, 6–10 dwa, 11–15 trzy, 16–20 cztery (wysokość 544). Więcej niż 20: zgłoś i zapytaj. Cała ściana jest blokiem w obszarze treści (sekcja „Odstępy i obszar treści”), wyśrodkowanym w pionie.

Adres logo: `https://raw.githubusercontent.com/tomaszkaczmarek-ai/ds-assets/main/logo-partnerow/{plik}.svg`. Pliki: allianz, blackrock, caspar, erste-tfi, esaliens, fidelity-international, franklin-templeton, generali-investments, ing, investors-tfi, ipopema, pzu-inwestycje, quercus, rockbridge, schroders, skarbiec, superfund, uniqa, vig-c-quadrat.

```html
<div style="display:flex;flex-direction:row;justify-content:center;gap:32px">{KAFLE}</div>
```

Kafel:

```html
<div style="width:267px;height:72px;padding:20px;background:[[tlo/kafelek-logo]];border-radius:14px;display:flex;align-items:center;justify-content:center"><img src="{logo}" alt="{nazwa}" style="width:227px;height:64px;object-fit:contain"></div>
```

### Wiersz składnika

Kiedy: lista składników, partnerów lub funduszy z logo i nazwą (np. skład portfela). Pola: logo z biblioteki (folder logo-partnerow), nazwa. Małe kafelki logo 144×32 w polu 144×32 z paddingiem 8 (razem 160×48), odstęp między wierszami 16. Nazwa 1 linia do ok. 53 znaków przy szerokości 680 px (kolumna 864 px); dłuższa zawija się do 2 linii (wiersz 65 px).

```html
<div style="display:flex;flex-direction:row;align-items:center;gap:24px"><div style="width:144px;height:32px;padding:8px;background:[[tlo/kafelek-logo]];border-radius:14px;display:flex;align-items:center;justify-content:center"><img src="{logo}" alt="{nazwa}" style="width:144px;height:32px;object-fit:contain"></div><p style="width:680px;font-size:24px;line-height:1.35;color:[[tekst/podstawowy]]">{nazwa}</p></div>
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
<div style="width:648px;display:flex;flex-direction:column;align-items:center;gap:16px;background:[[tlo/karta]];border-top:4px solid [[akcent/glowny]];border-radius:0 0 40px 40px;padding:32px 40px">{ZAWARTOŚĆ}</div>
```

### Łącznik pionowy

Kiedy: między dwiema kartami wyśrodkowanymi (zależność). Linia 3×48.

```html
<div style="width:3px;height:48px;background:[[linia/karta]]"></div>
```

Kolumnę schematu układaj jako `display:flex;flex-direction:column;align-items:center;width:728px`: karta, łącznik, karta.

## 10. Odstępy i obszar treści

Cel: brak pustych połaci, brak nachodzenia elementów, takie same odstępy na każdym slajdzie.

- **Skala odstępów:** 8, 16, 24, 32, 40, 48 px. Nie używaj innych wartości.
- **Standardowy odstęp między boxami i blokami: 32 px** (w pionie i w poziomie). Wewnątrz boxu 16 px między elementami, 12 px między pozycjami listy.
- **Nagłówek:** stała wysokość 112 (y 128–240). Treść zaczyna się najwyżej w y=304 (odstęp od nagłówka min. 64).
- **Obszar treści:** x 128–1792 (1664), y 304–920 (616). Poniżej, do y=964, wolny margines. W układach z paskiem wskaźników (od y=788) obszar kończy się 24 px nad paskiem.
- **Boxy nie są rozciągane**, żeby wypełnić obszar. Box ma wysokość naturalną. Boxy w jednym rzędzie mają jednakową wysokość (najwyższego z nich).
- **Wyrównanie w pionie:** blok treści niższy niż 70% obszaru (poniżej ok. 431 px) wyśrodkuj w pionie względem obszaru treści. Blok wyższy trzymaj od góry (y=304). Środek geometryczny, bez korekt optycznych; osoba tworząca może sama poprosić o przesunięcie.
- **Strefy zarezerwowane:** elementy o stałej pozycji (kafelek logo, QR, portret, pasek wskaźników, stopka) mają wokół siebie min. 24 px wolnego miejsca. Treść nie wchodzi w ich strefę.
- **Za dużo treści na obszar:** bez slajdu źródłowego wybierz układ o większej pojemności (sekcja 5), a teksty skracaj dopiero, gdy żaden układ się nie mieści. Ze slajdem źródłowym obowiązuje sekcja 7 pkt 4 (najpierw skrócenie, potem pytanie). Nie zmniejszaj odstępów poniżej skali.
- **Zakres skali:** skala dotyczy odstępów układu (między blokami, boxami i kolumnami). Odstępy wewnątrz wzorców (np. 4, 6, 10, 12, 20, 28 px) są częścią szablonu i zostają takie, jak w szablonie.
- **Obszar treści zastępuje odstęp ramy:** blok z szablonu „obszar treści” jest przypięty bezwzględnie (top 304) i nie zależy od odstępów w ramie slajdu.

Szablon obszaru treści:

```html
<div style="position:absolute;left:128px;top:304px;width:1664px;height:616px;display:flex;flex-direction:column;justify-content:{center albo flex-start};gap:32px">{BLOKI}</div>
```

Szablon rzędu boxów:

```html
<div style="display:flex;flex-direction:row;gap:32px">{BOXY}</div>
```

## 11. Zdjęcia i wykresy

- **Zdjęcia w tle** tylko na okładce i przekładkach. Na pozostałych slajdach tylko na wyraźną prośbę osoby tworzącej prezentację i tylko z plików wystarczającej jakości (w pełnym rozmiarze slajdu min. 1920 px szerokości). Jeśli plik jest za mały, zgłoś to w raporcie i użyj gładkiego tła.
- **Wykresy i diagramy złożone nie są odrysowywane.** Wykres ze źródła wstaw jako obraz ze źródła, w ramce o stałych wymiarach, bez przeróbki danych i kolorów, i wpisz to do raportu. Wyjątek: struktura procentowa o kilku wartościach (box Wykres lub wykres poziomy), gdy liczby są podane w tekście źródła i skill przepisuje je dosłownie.

---

KONIEC PLIKU (meta/wersja 2026-11-04.13)
