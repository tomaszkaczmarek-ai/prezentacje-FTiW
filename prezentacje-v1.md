# Design system prezentacji

meta/wersja: **2026-11-05.1**

meta/zmiana: Box z logo, Box Liczba szeroki (zamiast pasa przy jednej liczbie), Sekcje w dwóch kolumnach (rola Tekst opisowy), wyśrodkowany tekst w kartach diagramu cyklu, wykres jako obraz skalowany do obszaru. Wcześniej: Nowe wzorce: Diagram cyklu, Opis i grafika, Grafiki z podpisem (role Cykl, Opis i grafika, Grafiki z podpisem), cztery ikony strzałek. Przebudowa na system: zasady nadrzędne, katalog ról slajdów, procedura decyzyjna, pytania do użytkownika z opisem skutków, lista potrzebnych wzorców. Plik wzorców rozbity na trzy pliki (szkielet, układy, elementy). Wcześniej (2026-11-04.15): szablony odporne na model pudełkowy, rząd z operatorem „+”, ściana logo, przekładka, molekuły, szerokie boxy. Punkt powrotu: gałąź punkt-powrotu-2026-11-04-15.

Ten plik jest indeksem i jedynym źródłem zasad oraz tokenów wyglądu (kolory, wymiary, typografia, odstępy). Szablony HTML wzorców są w trzech plikach z sekcji „Pliki wzorców”. Wartości przepisuj dosłownie, niczego nie zaokrąglaj i nie dopisuj.

## Zasady nadrzędne

1. **Cel to najlepszy slajd dla odbiorcy, nie kopia źródła.** Układ ze źródła jest wskazówką o intencji autora (co jest ważne, co z czym się łączy), a nie ramą. Claude dobiera najbliższy wzorzec według roli slajdu i może zaproponować lepszy układ lub lepszy sposób pokazania treści.
2. **Nic nie ginie.** Zdjęć, ikon, QR, logo, linków, podpisów i liczb nie usuwasz. Każdy element źródła dostaje miejsce, niekoniecznie w tym samym położeniu. Usunięcie lub zamianę elementu (np. zdjęcia stockowego na ikonę) możesz tylko zasugerować użytkownikowi; bez jego zgody element zostaje.
3. **Zmiany sugerujesz, nie robisz po cichu.** Wszystko, co odbiega od źródła (inny układ, inna rola, zamiana typu elementu, skrócony tekst), trafia do raportu z powodem, a istotne zmiany do pytania do użytkownika.
4. **Jeden slajd źródła to jeden slajd wyniku.** Nie dzielisz slajdu i nie łączysz dwóch bez prośby. Połączenie lub podział możesz zaproponować w raporcie.
5. **Czytelność wygrywa z dekoracją.** Tekst min. 24 px, brak nachodzenia, brak pustych połaci (sekcja „Odstępy i obszar treści”).
6. **Wszystko ma rolę.** Kolor, rozmiar tekstu, odstęp i ikona są dozwolone tylko wtedy, gdy mają rolę w tym pliku.
7. **Brak wzorca to nie powód do improwizacji.** Weź najbliższy wzorzec, napisz czego brakuje i dopisz do listy „Potrzebne wzorce”. O nowych wzorcach decyduje właściciel systemu.

## Role slajdów

Każdy slajd źródła klasyfikujesz do jednej roli według sygnałów (liczba i rodzaj elementów, nie wygląd). Rola wskazuje wzorzec domyślny i pliki do pobrania. Gdy dwie role pasują, wybierz tę z mocniejszymi sygnałami i zgłoś wątpliwość w raporcie.

| Rola | Sygnały rozpoznania | Wzorzec domyślny | Pliki |
|---|---|---|---|
| Okładka | pierwszy slajd; tytuł, podtytuł, zdjęcie, logo | Okładka slajdu | szkielet |
| Przekładka | krótki tytuł rozdziału, zwykle zdjęcie, brak treści, często numer | Przekładka | szkielet |
| Opis i liczby | 2–3 akapity opisowe i 2–4 liczby; często logo partnera, QR, portret | Układ: Opis funduszu | uklady, elementy |
| Karty faktów | 2–6 równorzędnych pozycji, każda z krótkim tytułem i opisem (z ikoną lub zdjęciem) | Ikona z opisem; Box Tekst; Kolumna z ikoną i listą; Box z logo (gdy pozycje mają logo) | elementy, uklady |
| Tekst opisowy | 2–6 sekcji z nagłówkami i akapitami, bez grafik i liczb | 2–3 sekcje: Sekcja tekstowa w jednej kolumnie; 4–6: Układ: Sekcje w dwóch kolumnach | elementy, uklady |
| Liczby kluczowe | 1–4 liczby z jednostką i opisem | Box Liczba w rzędzie; Pasek wskaźników tylko przy 2 lub więcej; jedna liczba obok innych boxów: Box Liczba szeroki | uklady |
| Osoby | zdjęcia osób z imieniem, rolą i opisem | Karta osoby | elementy |
| Porównanie | kryteria w wierszach, 2 opcje w kolumnach | Tabela porównawcza (z ikoną, jeśli kryteria mają ikony) | uklady |
| Wyniki i skład | wykres lub seria okresów, lista składników, krótki opis | Tabela wyników, obraz wykresu ze źródła, Wiersz składnika | elementy, uklady |
| Schemat i zależności | elementy połączone relacją (spółka matka–zależna, kroki, formuła A + B) | Karta wyśrodkowana + Łącznik pionowy; Rząd z „+” | elementy |
| Cykl | 4 etapy w pętli (strzałki, „cykl”, „proces”, kroki wracające do początku), często z hasłem w środku i tekstem wyjaśniającym | Układ: Diagram cyklu | uklady, elementy |
| Opis i grafika | akapit lub dwa i jedna grafika ze źródła (zrzut ekranu, schemat, infografika, nie zdjęcie stockowe) | Układ: Opis i grafika | uklady |
| Grafiki z podpisem | 2–3 grafiki (ekrany, produkty, dokumenty), każda z krótkim podpisem | Układ: Grafiki z podpisem | uklady |
| Opis i lista z ikonami | akapit opisu i 2–5 faktów jednozdaniowych z ikonami | Wiersz listy z ikoną + Sekcja tekstowa (lub Karta wyśrodkowana obok) | elementy |
| Ściana logo | 6 lub więcej logo bez długich opisów | Ściana logo partnerów | elementy |

Role bez wzorca: patrz „Potrzebne wzorce”.

## Procedura decyzyjna

1. **Sklasyfikuj każdy slajd źródła do roli** (tabela wyżej). Zapisz listę elementów: rodzaj (tytuł, tekst, obraz, zdjęcie, liczba, tabela, wykres, logo, QR, link), liczbę i kolejność czytania. W pptx odczytaj pozycje (`a:off`, `a:ext` w EMU, rozmiar slajdu z `p:sldSz`, przelicz na 1920×1080), a obrazy z `ppt/media/` przypisuj do slajdów przez `ppt/slides/_rels/slideN.xml.rels`. W PDF lub obrazie opisz strefy z podglądu.
2. **Wybierz wzorzec roli.** Użyj wzorca domyślnego, jeśli mieszczą się w nim wszystkie elementy. Rozmieszczenie ze źródła traktuj jako wskazówkę: jeśli wzorzec ustawia elementy inaczej, ale zachowuje ich grupowanie i kolejność czytania, to jest w porządku. Jeśli żaden wzorzec nie pasuje, złóż układ z molekuł (elementów) i zgłoś brak wzorca.
3. **Dobierz molekuły do elementów.** Teksty, liczby i podpisy przepisujesz dosłownie. Jeśli nie mieszczą się w pojemności elementu, bez slajdu źródłowego wybierz układ o większej pojemności, a skracaj dopiero, gdy żaden się nie mieści (z listą skróceń w raporcie). Zdjęcia, logo, QR i inne zasoby ze źródła wgraj do talii i przypisz do miejsc wzorca. Brak zasobu w źródle: puste miejsce lub pominięcie elementu opcjonalnego, z wpisem do raportu; nie dopisuj zdjęć z internetu.
4. **Przy wątpliwości zapytaj użytkownika, jeśli jest obecny.** Wątpliwość to sytuacja, w której dwa wzorce lub dwa sposoby pokazania elementu są równie dobre albo zmiana ze źródła byłaby istotna (np. zamiana zdjęć na ikony, jeden wskaźnik: pas czy box, tytuł za długi). Zapytaj jednym pytaniem z 2–3 opcjami. Każda opcja ma nazwę, jedno zdanie opisu wyglądu, co użytkownik zyskuje i co traci; opcja domyślna jest oznaczona i pierwsza. Przykład: „Jedna liczba obok kart: A) Box Liczba szeroki pod kartami (domyślnie; liczba jest wyraźna i spójna z kartami), B) box Liczba jako kolejna karta w rzędzie (równy rząd, ale liczba jest mała i traci na wadze)”. Pas wskaźników nie jest opcją przy jednej liczbie. Pytaj raz na typ decyzji w prezentacji i stosuj odpowiedź do pozostałych takich slajdów. Gdy użytkownika nie ma (praca zaplanowana lub bez odpowiedzi), użyj opcji domyślnej i wpisz decyzję do raportu.
5. **Sugestie.** Jeśli widzisz lepszy sposób pokazania treści (zdjęcia stockowe niosące niewiele treści zamień na ikony; dwa slajdy, które mogłyby być jednym; za długi tytuł), napisz to w raporcie jako propozycję z opisem skutku. Niczego z tego nie rób bez zgody użytkownika.
6. **Zbuduj slajdy zgodnie z wzorcami i tokenami**, a wzorce pobieraj z plików wskazanych w rolach (sekcja „Pliki wzorców”).
7. **Raport zgodności:** wersja design systemu, rola i użyty wzorzec każdego slajdu, droga (wzorzec domyślny, złożony z molekuł lub odtworzony ze źródła), elementy źródła, które trafiły na slajd (i te, które nie, z powodem), odstępstwa, sugestie, lista skróceń, brakujące wzorce.

## Pliki wzorców

Pobierz je w kolejności potrzeby (pierwszy zawsze), każdy z kontrolą znacznika „KONIEC PLIKU (meta/wersja …)” na końcu; wszystkie mają tę samą wersję co indeks.

- `https://raw.githubusercontent.com/tomaszkaczmarek-ai/ds-assets/main/wzorce-szkielet.md`: rama slajdu treści, nagłówek, stopka, źródło w stopce, stopka z pasem, okładka, przekładka. Potrzebny w każdej prezentacji.
- `https://raw.githubusercontent.com/tomaszkaczmarek-ai/ds-assets/main/wzorce-elementy.md`: atomy (ikony, punktor, „+”, odznaka, karta szklana, ramka zdjęcia), kafelek logo, QR, sekcja tekstowa, portret, molekuły (karta osoby, ikona z opisem, box z logo, kolumna z ikoną i listą, ściana logo, wiersze, karta wyśrodkowana, łącznik).
- `https://raw.githubusercontent.com/tomaszkaczmarek-ai/ds-assets/main/wzorce-uklady.md`: boxy danych (Liczba, Liczba szeroki, Tekst, Wyliczenie, Wykres, szerokie), tabele, pasek wskaźników, układy: Opis funduszu, Diagram cyklu, Opis i grafika, Grafiki z podpisem, Sekcje w dwóch kolumnach.

Pobieraj tylko te pliki, których wymagają role użyte w prezentacji (kolumna „Pliki” w tabeli ról). Ikony i logo partnerów: adresy w pliku elementów (foldery `ikony/` i `logo-partnerow/`).

## Potrzebne wzorce

Lista prowadzona przez właściciela systemu z raportów użytkowników. Dopóki wzorca nie ma, użyj najbliższego i zgłoś w raporcie.

- Zamknięcie (kontakt, adres www, zdjęcie zespołu).

## Role kolorów

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

## Wymiary (px)

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

## Typografia

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

## Odstępy i obszar treści

Cel: brak pustych połaci, brak nachodzenia elementów, takie same odstępy na każdym slajdzie.

- **Skala odstępów:** 8, 16, 24, 32, 40, 48 px. Nie używaj innych wartości.
- **Standardowy odstęp między boxami i blokami: 32 px** (w pionie i w poziomie). Wewnątrz boxu 16 px między elementami, 12 px między pozycjami listy.
- **Nagłówek:** stała wysokość 112 (y 128–240). Treść zaczyna się najwyżej w y=304 (odstęp od nagłówka min. 64).
- **Obszar treści:** x 128–1792 (1664), y 304–920 (616). Poniżej, do y=964, wolny margines. W układach z paskiem wskaźników (od y=788) obszar kończy się 24 px nad paskiem.
- **Boxy nie są rozciągane**, żeby wypełnić obszar. Box ma wysokość naturalną. Boxy w jednym rzędzie mają jednakową wysokość (najwyższego z nich).
- **Wyrównanie w pionie:** blok treści niższy niż 70% obszaru (poniżej ok. 431 px) wyśrodkuj w pionie względem obszaru treści. Blok wyższy trzymaj od góry (y=304). Środek geometryczny, bez korekt optycznych; osoba tworząca może sama poprosić o przesunięcie.
- **Strefy zarezerwowane:** elementy o stałej pozycji (kafelek logo, QR, portret, pasek wskaźników, stopka) mają wokół siebie min. 24 px wolnego miejsca. Treść nie wchodzi w ich strefę.
- **Za dużo treści na obszar:** wybierz wzorzec o większej pojemności, a teksty skracaj dopiero, gdy żaden się nie mieści (procedura decyzyjna, krok 3). Nie zmniejszaj odstępów poniżej skali.
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

## Model pudełkowy w Slajdach

W Claude Slides `width` i `height` obejmują padding i ramkę (potwierdzone na wyniku: pas z `width:1664px` i `padding:0 128px` miał 1664 px razem z paddingiem). Dlatego element o stałej szerokości lub wysokości nie ma paddingu ani ramki na tym samym elemencie: odstępy robią elementy wewnętrzne (przekładki `div` o stałej wysokości lub szerokości), a ramki zdjęć to tło limonkowe z wewnętrznym obrazem. Szablony w tym pliku są tak napisane, żeby wyglądały tak samo w obu modelach. Elementy z `flex:1` mogą mieć padding. Nie dopisuj paddingu do elementu ze stałym `width` lub `height`.

## Zdjęcia i wykresy

- **Zdjęcia w tle** tylko na okładce i przekładkach. Na pozostałych slajdach tylko na wyraźną prośbę osoby tworzącej prezentację i tylko z plików wystarczającej jakości (w pełnym rozmiarze slajdu min. 1920 px szerokości). Jeśli plik jest za mały, zgłoś to w raporcie i użyj gładkiego tła.
- **Wykresy i diagramy złożone nie są odrysowywane.** Wykres ze źródła wstaw jako obraz ze źródła, bez przeróbki danych i kolorów, i wpisz to do raportu. Skaluj go do największego rozmiaru, który mieści się w obszarze treści 1664×616 (z podpisem pod spodem 1664×560) z zachowaniem proporcji, i wyśrodkuj; nie zostawiaj wąskiego wykresu na środku pustego slajdu. Wyjątek: struktura procentowa o kilku wartościach (box Wykres lub wykres poziomy), gdy liczby są podane w tekście źródła i skill przepisuje je dosłownie.


---

KONIEC PLIKU (meta/wersja 2026-11-05.1)
