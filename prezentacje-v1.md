# Design system prezentacji

meta/wersja: **2026-11-04.3**

meta/zmiana: Dodana zasada „Układ ze źródła” (pierwszeństwo przed doborem układu, gdy użytkownik załączył slajd źródłowy). Wcześniej: dodane zasady zasobów ze źródła i mapowania slajdów 1:1. Wcześniej: dodane elementy i układ „Opis funduszu” (kafelek logo partnera, QR z podpisem, sekcje tekstowe, portret w kółku, pasek wskaźników, stopka z pasem) oraz zasady doboru układu. Wcześniej: Okładka slajdu. Poprzednio: zamknięta paleta (6 kolorów), wzorce: nagłówek, stopka, boxy danych, wykres poziomy, tabela.

Źródło wartości: plik projektowy właściciela (Figma). Ten plik jest odczytywalną kopią dla skilla do prezentacji. Wartości przepisuj dosłownie, niczego nie zaokrąglaj i nie dopisuj.

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
| tlo/pasek-wskaznikow | #34493D | pas wskaźników na całą szerokość slajdu |
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
| odstep liter eyebrow | 5 |
| odstep liter etykieta | 3 |
| odstęp ramy treści (nagłówek–treść) | 32 (przy tabeli 28, w układzie Opis funduszu 24) |
| kafelek logo partnera | 360×112, promień 14 |
| kafelek QR | 144×144, promień 12 |
| portret w kółku | średnica 288 (zdjęcie 272 + ramka 8 px w kolorze akcent/glowny) |
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
| Jednostka | 40 | 700 | 1,1 |  |
| Podtytuł | 32 | 400 | 1,3 |  |
| Podtytuł – pogrubiony | 32 | 700 | 1,3 |  |
| Tytuł karty | 30 | 700 | 1,2 |  |
| Tekst karty | 26 | 400 | 1,35 |  |
| Tekst karty – pogrubiony | 26 | 700 | 1,25 |  |
| Tekst | 24 | 400 | 1,35 |  |
| Tekst – pogrubiony | 24 | 700 | 1,3 |  |
| Eyebrow | 24 | 400 | 1,4 | wielkie litery, odstęp 5 |
| Etykieta bloku | 24 | 600 | 1,3 | wielkie litery, odstęp 3 |

## 4. Wzorce (szablony HTML)

Zastępuj `[[rola]]` i `{pole}`. Twarda spacja w HTML to `&#160;` (tylko encje numeryczne). Nie zmieniaj struktury, kolejności ani odstępów, zmieniaj tylko pola. Brak pasującego wzorca: zgłoś w raporcie, nie improwizuj.

### Slajd treści (rama)

Kiedy: Każdy slajd poza okładką. Kąt światła {kat}: 120, 60, 150, 180, potem od nowa.

```html
<section id="{id}" style="background:[[tlo/tresc]];color:[[tekst/podstawowy]];font-family:'Montserrat', Arial, sans-serif;padding:128px 128px 160px;display:flex;flex-direction:column;gap:32px">
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

Kiedy: Początek każdego slajdu treści. Pola: eyebrow (krótka etykieta), tytuł (jedno zdanie, do 2 linii).

```html
<div style="display:flex;flex-direction:column;gap:16px">
<p style="font-size:24px;line-height:1.4;letter-spacing:5px;text-transform:uppercase;color:[[tekst/podstawowy]]">{eyebrow}</p>
<h2 style="font-size:56px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{tytuł}</h2>
</div>
```

### Stopka slajdu

Kiedy: Każdy slajd treści. Pola: numer strony (dwie cyfry). Logo jako zasób wgrany przez użytkownika.

```html
<img src="{logo}" alt="Logo" style="position:absolute;left:128px;bottom:64px;width:274px;height:20px;object-fit:contain">
<p style="position:absolute;right:128px;bottom:64px;width:200px;font-size:24px;line-height:1.2;text-align:right;color:[[tekst/podstawowy]]">{nn}</p>
```

### Box danych – rama

Kiedy: Wyróżniony blok, 2–4 obok siebie. Układ w rzędzie: display:flex;gap:32px; dla czterech: display:grid;grid-template-columns:1fr 1fr;gap:28px 32px.

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

### Okładka slajdu

Kiedy: Wyłącznie pierwszy slajd. Pola: eyebrow, tytuł (max 2 linie), podtytuł (1 linia), zdjęcie pełnoekranowe, logo. Bez smug światła i stopki. Tekst zawsze po lewej.

```html
<section id="cover" style="background:[[tlo/okladka]]">
<img src="{zdjęcie}" alt="{opis}" style="position:absolute;top:0;left:0;width:1920px;height:1080px">
<div style="position:absolute;top:0;left:0;width:1920px;height:1080px;display:flex;flex-direction:column;background:linear-gradient(90deg, rgba(17,46,23,0.97) 0%, rgba(17,46,23,0.86) 48%, rgba(17,46,23,0.22) 100%)"></div>
<div style="position:absolute;top:48px;left:48px;width:1824px;height:984px;display:flex;flex-direction:column;border:1px solid [[linia/ramka-okladki]]"></div>
<img src="{logo}" alt="Logo" style="position:absolute;top:120px;left:128px;width:374px;height:28px;object-fit:contain">
<p style="position:absolute;top:405px;left:128px;width:1280px;font-size:24px;line-height:1.4;letter-spacing:5px;text-transform:uppercase;color:[[tekst/podstawowy]]">{eyebrow}</p>
<div style="position:absolute;top:469px;left:128px;width:120px;height:4px;background:[[akcent/glowny]]"></div>
<h1 style="position:absolute;top:505px;left:128px;width:1470px;font-size:84px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{tytuł}</h1>
<p style="position:absolute;top:824px;left:128px;width:1210px;font-size:32px;line-height:1.4;color:[[tekst/podstawowy]]">{podtytuł}</p>
<aside>Wersja design systemu: {meta/wersja}</aside>
</section>
```

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
<img src="{portret}" alt="{osoba}" style="position:absolute;left:1504px;top:440px;width:272px;height:272px;border:8px solid [[akcent/glowny]];border-radius:144px;object-fit:cover">
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

Kiedy: dużo tekstu opisowego (2–3 sekcje, do ok. 1000 znaków) plus 2–4 wskaźniki; opcjonalnie logo partnera, QR i portret. Kolejność elementów w sekcji slajdu treści: 1) trzy smugi światła, 2) pas stopki, 3) nagłówek slajdu (eyebrow + tytuł, szerokość 1060, odstęp ramy 24), 4) kafelek logo partnera, 5) QR z podpisem, 6) kolumna sekcji tekstowych, 7) portret, 8) pasek wskaźników, 9) logo i numer strony. Elementy opcjonalne pomijaj, jeśli nie ma ich w materiale; pozostałe zostają na swoich miejscach. Rama slajdu jak „Slajd treści (rama)” z odstępem 24.

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
5. **Raport:** napisz, którą drogą poszedłeś (programowany układ albo odtworzenie ze źródła) i wymień odstępstwa od źródła (przesunięte elementy, skrócone teksty, brakujące zasoby).

---

KONIEC PLIKU (meta/wersja 2026-11-04.3)
