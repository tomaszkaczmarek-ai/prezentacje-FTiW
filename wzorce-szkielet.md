# Wzorce: szkielet slajdu

meta/wersja: **2026-11-05.1**

Szkielet: rama slajdu treści, nagłówek, stopka, okładka, przekładka. Tokeny (kolory, wymiary, typografia, odstępy, model pudełkowy) są w pliku indeksu `prezentacje-v1.md`.

Zastępuj `[[rola]]` i `{pole}`. Twarda spacja w HTML to `&#160;` (tylko encje numeryczne). Nie zmieniaj struktury, kolejności ani odstępów w szablonie, zmieniaj tylko pola. Brak pasującego wzorca: zgłoś w raporcie, nie improwizuj.

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

Kiedy: początek nowej części prezentacji (rozdział), zwykle co kilka slajdów. Pola: numer części (dwie cyfry), tytuł (max 2 linie), podtytuł (opcjonalny, 1 linia), zdjęcie pełnoekranowe, logo, numer strony. Zdjęcie z pliku użytkownika (sekcja „Zdjęcia i wykresy”); bez zdjęcia użyj gładkiego tła tlo/okladka. Zdjęcie jest przykryte równą ciemną warstwą (tlo/przekladka), która wycisza jego szczegóły, a tekst leży na karcie szklanej. Dzięki temu przekładka wyraźnie różni się od okładki (ciemny gradient z lewej, ramka). Bez smug światła.

```html
<section id="divider" style="background:[[tlo/okladka]]">
<img src="{zdjęcie}" alt="{opis}" style="position:absolute;top:0;left:0;width:1920px;height:1080px;object-fit:cover">
<div style="position:absolute;top:0;left:0;width:1920px;height:1080px;display:flex;flex-direction:column;background:[[tlo/przekladka]]"></div>
<div style="position:absolute;top:330px;left:128px;width:1100px;display:flex;flex-direction:column;align-items:center;background:[[tlo/kolumna-funduszu]];border-radius:40px"><div style="height:48px"></div><div style="width:988px;display:flex;flex-direction:column;gap:16px">
<p style="font-size:96px;font-weight:700;line-height:1.1;color:[[akcent/glowny]]">{nn}</p>
<div style="width:120px;height:4px;background:[[akcent/glowny]]"></div>
<h1 style="font-size:56px;font-weight:700;line-height:1.1;color:[[tekst/tytul]]">{tytuł}</h1>
<p style="font-size:32px;line-height:1.3;color:[[tekst/podstawowy]]">{podtytuł}</p>
</div><div style="height:48px"></div></div>
<img src="{logo}" alt="Logo" style="position:absolute;left:128px;bottom:64px;width:274px;height:20px;object-fit:contain">
<p style="position:absolute;right:128px;bottom:64px;width:200px;font-size:24px;line-height:1.2;text-align:right;color:[[tekst/podstawowy]]">{nn strony}</p>
<aside>Wersja design systemu: {meta/wersja}</aside>
</section>
```

Pojemność tytułu: 2 linie po ok. 31 znaków (56 px pogrubiony, szerokość 988 px w karcie), do ok. 60 znaków łącznie; dłuższy skróć i wpisz do raportu. Podtytuł: 1 linia do ok. 55 znaków. Karta ma wysokość naturalną (ok. 420 px przy tytule 2-liniowym i podtytule).

### Stopka z pasem

Kiedy: układy z paskiem wskaźników (pas stopki idzie zaraz za tłem smug, przed treścią). Pas, potem logo i numer jak w „Stopka slajdu”.

```html
<div style="position:absolute;left:0px;top:964px;width:1920px;height:116px;background:[[tlo/stopka-pas]]"></div>
```

---

KONIEC PLIKU (meta/wersja 2026-11-05.1)
