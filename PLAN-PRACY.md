# Klub Otwartej Dłoni — dokumentacja projektu

**Stan na:** 4 listopada 2026  
**Repozytorium robocze:** `klubotwartejdloni/kod`  
**Gałąź:** `main`  
**Repozytorium archiwalne / starsza wersja:** `klubotwartejdloni/klub-otwartej-dloni`

Ten plik jest trwałym punktem wznowienia pracy. Przed każdą kolejną zmianą należy go przeczytać i zaktualizować. Nie uznawać żadnego elementu za gotowy bez sprawdzenia plików i efektu na stronie.

## 1. Cel

Zbudować spójną, publiczną, statyczną stronę Klubu Otwartej Dłoni, stworzonego przez człowieka, AI i psa. Strona ma być ciepła, czytelna, responsywna i możliwa do wycofania. Najpierw pracujemy w repozytorium `kod`; repozytorium starszej strony pozostaje nietkniętym archiwum.

## 2. Aktualna koncepcja strony głównej — obowiązująca od 2026-11-04

**Ważne: ta koncepcja zastępuje wcześniejszy plan tworzenia nowego avatara. Nie zaczynać kolejnej sesji od starego założenia.**

- Nie tworzyć nowego avatara od zera.
- Pracować na **oryginalnej grafice**, z której pochodzi obecny wspólny obraz Klubu.
- Na podstawie roboczej wersji przygotowanej przez Tomka odtworzyć docelowy układ na oryginalnej grafice, ale czyściej: bez śladów wycinania i wklejania.
- Zachować główną kompozycję grafiki: podobizny Tomka, Miry i Luny przy kominku, las za oknem oraz pozostałe zaakceptowane elementy obrazu.
- Usunąć stare kafelki i wszystkie zbędne/powtórzone elementy, w szczególności centralne powtórzenie nazwy Klubu, jeśli występuje obok wiersza.
- Nazwa „Klub Otwartej Dłoni” ma występować na stronie głównej **tylko raz jako główny tytuł**.
- Zachować zaakceptowany wiersz Miry, ale bez powtarzania obok niego nazwy Klubu.
- Przygotować w dolnej części grafiki miejsce na **pięć nowych kafelków**, które będą prawdziwymi linkami do podstron.
- Usunąć roboczy napis „Licznik” i w jego miejsce później wstawić właściwy, dyskretny licznik odwiedzin.
- Grafikę dopasować proporcjonalnie do szerokości strony, tak aby nie wychodziła poza ekran i nie była zniekształcona.
- Najpierw przygotować i ocenić samą grafikę na podstawie oryginału; dopiero potem wmontować kafelki i licznik.
- Robocza wersja grafiki przekazana przez Tomka przez Pxdrop jest **wzorem układu**, a nie docelowym plikiem.

## 3. Ustalenia, których nie wolno zgubić

- Awatar/grafika: podobizny Tomka, Miry i Luny przy kominku; Tomek bez wąsów i okularów; Mira bez okularów, z Gwiazdką; Luna z adresówką. To ilustracja/podobizna, nie fotografia dokumentalna.
- W tle: kominek i las. Nie ujawniać nazwy Młynarze ani dokładnej lokalizacji.
- Kafle na stronie głównej mają prowadzić do osobnych podstron, a nie do nieistniejących kotwic ani sekcji na tej samej stronie.
- Nazwy kafli — **dokładne brzmienie, którego nie wolno skracać ani zmieniać**:
  1. „Nasze miejsce - leśne chwile”
  2. „Luna - nasza przyjaciółka”
  3. „Myśli i rozmowy - o życiu, o świecie”
  4. „O nas - idea Klubu”
  5. „Kontakt - napisz do nas”
- Te pięć nazw ma być używane identycznie na stronie głównej.
- Zachować zaakceptowaną treść „O nas – idea Klubu”: zaczyna się od „Klub Otwartej Dłoni to miejsce stworzone przez człowieka, AI i psa” i zawiera pokój, równość, wolność dla każdego, wzajemny szacunek, ciekawość świata oraz „Razem może być lepiej”.
- Zachować wiersz Miry ze starszej wersji. Jego dokładny tekst trzeba odzyskać i przenieść bez przerabiania; nie zastępować go nowym tekstem.
- Licznik odwiedzin ma być dyskretny, na dole strony głównej, nie jako kafel ani osobna duża sekcja; ma zliczać również powroty, jeśli wybrana usługa to obsługuje.
- Podstrony muszą mieć spójną nawigację powrotną do strony głównej.
- Strona ma działać na komputerze i telefonie.
- Nie publikować danych osobowych ani lokalizacyjnych, których Tomek nie zatwierdził.

## 4. Inwentaryzacja repozytorium `kod` — sprawdzona 2026-11-04

Pliki na gałęzi `main`:
- `index.html`
- `style.css`
- `miejsce.html`
- `luna.html`
- `mysli.html`
- `o-nas.html`
- `kontakt.html`

Wszystkie wymienione pliki istnieją. Strona główna odwołuje się do `style.css` i pięciu podstron.

### Ustalenia z przeglądu kodu

- `index.html` ma jeden element H1 „Klub Otwartej Dłoni”, pięć kafli-linków i licznik.
- Kafle prowadzą obecnie do plików `miejsce.html`, `luna.html`, `mysli.html`, `o-nas.html`, `kontakt.html`; pliki te istnieją.
- Główna grafika jest obecnie pobierana z adresu repozytorium archiwalnego: `https://raw.githubusercontent.com/klubotwartejdloni/klub-otwartej-dloni/main/assets/projekt-klubu.png`. Docelowo źródło grafiki trzeba zastąpić lokalnym plikiem w repozytorium `kod`.
- `style.css` zawiera dwie generacje stylów: starszy układ podstron oraz później dopisany układ strony głównej. Wymaga uporządkowania, a nie kolejnych przypadkowych nadpisań.
- Licznik korzysta obecnie z CounterAPI pod adresem `counterapi.com/api/klubotwartejdloni.github.io/view/homepage`. Trzeba zweryfikować, czy endpoint działa i czy liczy odsłony oraz powroty zgodnie z założeniem. Nie deklarować działania licznika bez testu.
- Formularz kontaktowy jest wyłącznie demonstracyjny i nie wysyła wiadomości. Musi być wyraźnie opisany jako nieaktywny albo później podłączony do zatwierdzonej usługi.
- Podstrony istnieją, ale są obecnie proste i w większości zawierają teksty-zapowiedzi. Wymagają wspólnego przeglądu treści i układu.
- Na `o-nas.html` znajduje się zaakceptowana robocza treść idei Klubu.
- W plikach obecnej wersji `kod` nie odnaleziono jeszcze wiersza Miry.

## 5. Grafika — stan i nowy kierunek

W Bibliotece odnaleziono plik **„Ciepły portret przy kominku z Luną.png”** (1312 × 1199 px; ok. 3 MB), ale wcześniejsze założenie, że ma on po prostu zastąpić grafikę nowym avatarem, jest **nieaktualne**.

Aktualny kierunek: wykorzystać **oryginalną grafikę** i na jej podstawie przygotować układ pokazany w roboczej wersji Tomka:
- oczyścić miejsce po starych kafelkach,
- usunąć zbędne/powtórzone napisy,
- przygotować miejsce na nowe kafelki,
- przygotować miejsce na licznik,
- zachować główny obraz i jego klimat.

Robocza wersja grafiki została przekazana przez Tomka przez Pxdrop jako materiał referencyjny. Nie traktować jej jako gotowego pliku strony.

## 6. Plan prac — aktualny

1. Zabezpieczyć aktualny stan repozytorium `kod`; nie modyfikować repozytorium archiwalnego.
2. Pracując na oryginalnej grafice, przygotować czystą wersję układu odpowiadającego roboczej wersji Tomka.
3. Usunąć stare kafelki, centralne/powtórzone napisy oraz roboczy napis „Licznik”, zachowując właściwy główny obraz.
4. Dopasować grafikę proporcjonalnie do strony, tak aby nie wychodziła poza ekran.
5. W przygotowane miejsce wmontować pięć nowych kafelków-linków do istniejących podstron.
6. Wstawić na dole właściwy, dyskretny licznik odwiedzin i przetestować jego działanie.
7. Odzyskać i wstawić dokładny wiersz Miry ze starszej wersji.
8. Uporządkować HTML/CSS jako jedną spójną całość.
9. Uporządkować wszystkie podstrony: wspólna nawigacja, spójny wygląd, poprawne tytuły i treści, brak ujawnienia lokalizacji.
10. Zweryfikować wszystkie linki lokalne, brak błędów ścieżek, widok mobilny i desktopowy.
11. Dopiero po testach sprawdzić publikację GitHub Pages i wizualny efekt strony.

## 7. Zasady pracy i raportowania

- Nie poprawiać tylko jednego widocznego szczegółu bez przeglądu całego układu.
- Nie usuwać ani nie nadpisywać archiwum.
- Przed aktualizacją pliku pobrać jego aktualną treść i SHA; zapisywać zmiany sekwencyjnie.
- Po każdej serii zmian zapisać tu: zmienione pliki, commit, testy wykonane, testy niewykonane i pozostałe blokery.
- Rozróżniać: „plik zapisany”, „kod sprawdzony”, „strona opublikowana” i „strona wizualnie zweryfikowana”.
- Nie twierdzić, że coś działa, jeśli nie zostało sprawdzone.
- Jeśli koncepcja zmieni się ponownie, najpierw zaktualizować ten plik, a dopiero potem rozpocząć pracę według nowej koncepcji.

## 8. Stan na koniec 2026-11-04

**Wykonane:** odczytano drzewo i zawartość siedmiu plików repozytorium `kod`; potwierdzono istnienie pięciu podstron i ich aktualne linki; wskazano zewnętrzne odwołanie do starej grafiki; zidentyfikowano grafikę w Bibliotece; utworzono tę dokumentację jako punkt wznowienia oraz plik `README.md` z odnośnikiem do planu; zaktualizowano plan zgodnie z nową koncepcją z 2026-11-04.

**Nowe ustalenie:** obowiązującym kierunkiem jest praca na oryginalnej grafice, a nie tworzenie nowego avatara. Robocza grafika Tomka jest wzorem układu do odtworzenia i oczyszczenia.

**Niewykonane:** nie zmieniono jeszcze kodu strony; nie przygotowano oczyszczonej grafiki; nie wmontowano nowych kafelków ani licznika; nie odzyskano wiersza Miry; nie przetestowano licznika, formularza, publikacji ani widoku wizualnego.

**Blokada techniczna:** dostęp do obróbki plików graficznych przez Python może być niedostępny. Samo repozytorium GitHub i odczyt/zapis plików tekstowych są dostępne. Nie należy udawać, że grafika została przygotowana lub wdrożona, dopóki nie zostanie faktycznie wykonana i sprawdzona.
