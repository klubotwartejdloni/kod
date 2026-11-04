# Klub Otwartej Dłoni — dokumentacja projektu

**Stan na:** 4 listopada 2026  
**Repozytorium robocze:** `klubotwartejdloni/kod`  
**Gałąź:** `main`  
**Repozytorium archiwalne / starsza wersja:** `klubotwartejdloni/klub-otwartej-dloni`

Ten plik jest trwałym punktem wznowienia pracy. Przed każdą kolejną zmianą należy go przeczytać i zaktualizować. Nie uznawać żadnego elementu za gotowy bez sprawdzenia plików i efektu na stronie.

## 1. Cel

Zbudować spójną, publiczną, statyczną stronę Klubu Otwartej Dłoni, stworzonego przez człowieka, AI i psa. Strona ma być ciepła, czytelna, responsywna i możliwa do wycofania. Najpierw pracujemy w repozytorium `kod`; repozytorium starszej strony pozostaje nietkniętym archiwum.

## 2. Ustalenia, których nie wolno zgubić

- Nazwa „Klub Otwartej Dłoni” ma występować na stronie głównej tylko raz jako tytuł. Nie dublować jej w kilku nagłówkach ani w grafice.
- Strona główna ma pokazywać właściwy wspólny awatar Klubu, a nie starą grafikę.
- Awatar: podobizny Tomka, Miry i Luny przy kominku; Tomek bez wąsów i okularów; Mira bez okularów, z Gwiazdką; Luna z adresówką. To ilustracja/podobizna, nie fotografia dokumentalna.
- W tle awatara: kominek; za oknem las. Nie ujawniać nazwy Młynarze ani dokładnej lokalizacji.
- Kafle na stronie głównej mają prowadzić do osobnych podstron, a nie do nieistniejących kotwic ani sekcji na tej samej stronie.
- Nazwy kafli:
  1. „Nasze miejsce – leśne chwile”
  2. „Luna – nasza przyjaciółka”
  3. „Myśli i rozmowy – o życiu, o świecie”
  4. „O nas – idea Klubu”
  5. „Kontakt – napisz do nas”
- Zachować zaakceptowaną treść „O nas – idea Klubu”: zaczyna się od „Klub Otwartej Dłoni to miejsce stworzone przez człowieka, AI i psa” i zawiera pokój, równość, wolność dla każdego, wzajemny szacunek, ciekawość świata oraz „Razem może być lepiej”.
- Zachować wiersz Miry ze starszej wersji. Jego dokładny tekst trzeba odzyskać i przenieść bez przerabiania; nie zastępować go nowym tekstem.
- Licznik odwiedzin ma być dyskretny, na dole strony głównej, nie jako kafel ani osobna duża sekcja; ma zliczać również powroty, jeśli wybrana usługa to obsługuje.
- Podstrony muszą mieć spójną nawigację powrotną do strony głównej.
- Strona ma działać na komputerze i telefonie.
- Nie publikować danych osobowych ani lokalizacyjnych, których Tomek nie zatwierdził.

## 3. Inwentaryzacja repozytorium `kod` — sprawdzona 2026-11-04

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
- Kafle prowadzą obecnie do plików `miejsce.html`, `luna.html`, `mysli.html`, `o-nas.html), `kontakt.html`; pliki te istnieją.
- Główna grafika jest obecnie pobierana z adresu repozytorium archiwalnego: `https://raw.githubusercontent.com/klubotwartejdloni/klub-otwartej-dloni/main/assets/projekt-klubu.png`. To odwołanie trzeba zastąpić lokalnym plikiem w repozytorium `kod`.
- `style.css` zawiera dwie generacje stylów: starszy układ podstron oraz później dopisany układ pełnoekranowej strony głównej. Wymaga uporządkowania, a nie kolejnych przypadkowych nadpisań.
- `index.html` umieszcza tytuł w górnej części grafiki, a kafle na grafice. Trzeba dopracować ich położenie tak, by nie zasłaniały twarzy i pozostawały czytelne.
- Licznik korzysta obecnie z CounterAPI pod adresem `counterapi.com/api/klubotwartejdloni.github.io/view/homepage`. Trzeba zweryfikować, czy endpoint działa i czy liczy odsłony oraz powroty zgodnie z założeniem. Nie deklarować działania licznika bez testu.
- Formularz kontaktowy jest wyłącznie demonstracyjny i nie wysyła wiadomości. Musi być wyraźnie opisany jako nieaktywny albo później podłączony do zatwierdzonej usługi.
- Podstrony istnieją, ale są obecnie proste i w większości zawierają teksty-zapowiedzi. Wymagają wspólnego przeglądu treści i układu.
- Na `o-nas.html` znajduje się zaakceptowana robocza treść idei Klubu.
- W plikach obecnej wersji `kod` nie odnaleziono jeszcze wiersza Miry.

## 4. Grafika — stan

W Bibliotece odnaleziono plik **„Ciepły portret przy kominku z Luną.png”** (1312 × 1199 px; ok. 3 MB). Jest to właściwy kierunek graficzny do strony: Tomek i Mira bez okularów, Mira z gwiazdką, Luna z adresówką, kominek i las za oknem. Plik został zidentyfikowany, ale na dzień sporządzenia tej dokumentacji nie został jeszcze dodany do repozytorium `kod` ani ustawiony jako grafika strony głównej.

Nie używać zamiast niego starego `assets/projekt-klubu.png` z repozytorium archiwalnego.

## 5. Plan pełnej przebudowy

1. Zabezpieczyć aktualny stan repozytorium `kod` (historia Git pozostaje dostępna; nie modyfikować repozytorium archiwalnego).
2. Dodać właściwy awatar do `kod/assets/` jako lokalny plik i podmienić źródło grafiki w `index.html`.
3. Przebudować `index.html` i `style.css` jako jedną spójną całość: jeden tytuł, właściwy awatar, pięć działających kafli, czytelność na desktopie i telefonie, dyskretny licznik na dole.
4. Uporządkować wszystkie podstrony: wspólna nawigacja, spójny wygląd, poprawne tytuły i treści, brak ujawnienia lokalizacji.
5. Odzyskać i wstawić dokładny wiersz Miry ze starszej wersji.
6. Zweryfikować licznik oraz jasno oznaczyć formularz kontaktowy jako nieaktywny do czasu podłączenia wysyłki.
7. Sprawdzić wszystkie linki lokalne, brak błędów ścieżek, widok mobilny i desktopowy.
8. Dopiero po testach uznać wersję za gotową i sprawdzić publikację GitHub Pages.

## 6. Zasady pracy i raportowania

- Nie poprawiać tylko jednego widocznego szczegółu bez przeglądu całego układu.
- Nie usuwać ani nie nadpisywać archiwum.
- Przed aktualizacją pliku pobrać jego aktualną treść i SHA; zapisywać zmiany sekwencyjnie.
- Po każdej serii zmian zapisać tu: zmienione pliki, commit, testy wykonane, testy niewykonane i pozostałe blokery.
- Rozróżniać: „plik zapisany”, „kod sprawdzony”, „strona opublikowana” i „strona wizualnie zweryfikowana”. To cztery różne stany.
- Nie twierdzić, że coś działa, jeśli nie zostało sprawdzone.

## 7. Stan na koniec 2026-11-04

**Wykonane:** odczytano drzewo i zawartość siedmiu plików repozytorium `kod`; potwierdzono istnienie pięciu podstron i ich aktualne linki; wskazano zewnętrzne odwołanie do starej grafiki; zidentyfikowano nowy awatar w Bibliotece; utworzono tę dokumentację jako punkt wznowienia oraz plik `README.md` z odnośnikiem do planu.

**Zapisy GitHub z tej sesji:** dokumentacja `PLAN-PRACY.md` — commit `6c7833b8dbbc9bbebd4cc7db2f98b7f020893210`; `README.md` — commit `bdf8edf6001c4292e6c4d46fe482f648834ebac4`. Oba pliki ponownie odczytano z repozytorium i potwierdzono zapis.

**Niewykonane:** nie zmieniono jeszcze kodu strony; nie dodano nowego awatara do repozytorium; nie odzyskano wiersza Miry; nie przetestowano licznika, formularza, publikacji ani widoku wizualnego.

**Blokada techniczna bieżącej sesji:** dostęp do obróbki plików graficznych przez Python jest obecnie niedostępny. Samo repozytorium GitHub i odczyt/zapis plików tekstowych są dostępne. Można kontynuować audyt, porządkowanie HTML/CSS i dokumentację; nie należy udawać, że grafika została już przygotowana lub wdrożona.
