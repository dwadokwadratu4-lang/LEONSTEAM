# HIGH VOLTAGE: LEON'S TEAM
*Zespół Leona*

Taktyczna gra symulacyjna 2.5D w rzucie izometrycznym osadzona w realiach pracy na hali, odbiorów i nadzoru nad punktami kontrolnymi (m.in. AKPiA, PLC, stanowiska i maszyny przemysłowe). Projekt pełni również rolę poglądowego prototypu (PoC) pokazującego znaczenie koordynacji zespołów, terminowości i domknięcia odbiorów.

**Autor:** Artur Wierzbicki

---

## O projekcie
Gracz wciela się w brygadzistę **Piotra**, który dowodzi zespołem niebieskich pracowników (z czerwonym akcentem logo) na terenie **trzech hal** (`01/03`, `02/03`, `03/03`). Zadaniem jest sprawne rozdzielanie ludzi do stanowisk, pilnowanie czasu pracy, odbieranie gotowych punktów na zielono oraz radzenie sobie z działaniami ekipy **Janusza** (zespół beżowy).

---

## Kluczowe mechaniki
* **Trzy hale i limit czasu:** każda hala posiada odliczanie **2,5 minuty (`02:30`)** w dół oraz kontrolę bezczynności – brak postępów lub działań na sali kończy pracę.
* **Wejście i wyjście:** zespół rozpoczyna pracę wchodząc przez wejście hali, a po zamknięciu ostatniego punktu na zielono samodzielnie kieruje się do wyjścia (po czym następuje krótka 2-sekundowa pauza przed dalszym krokiem scenariusza).
* **Stany stanowisk i postęp (`0–100%`):**
  * **Czerwony (`RED`)** – punkt oczekuje na rozpoczęcie lub został zresetowany po ingerencji ekipy Janusza.
  * **Pomarańczowy (`ORANGE`)** – przekroczony bazowy czas realizacji zadania.
  * **Zielony (`GREEN`)** – punkt odebrany przez Piotra (`FINISH` / odbiór po osiągnięciu `100%` i statusie `GOTOWE`).
* **Przejęcia i „Skok napięcia”:** zbyt długie oczekiwanie na odbiór lub działanie beżowej ekipy może doprowadzić do przejęcia pracownika. Bezpośredni kontakt Piotra z Januszem wywołuje **„Skok napięcia”**, który na kilka sekund unieruchamia Janusza i pozwala odzyskać pracownika (z ograniczeniem ponownego odzyskania kolejnego przed przydzieleniem obecnego do nowego zadania).
* **Przejścia między halami i nawigacja:** ekran przejścia między halami czeka na kliknięcie lub dotknięcie gracza. Kliknięcie tytułu w lewym górnym rogu wraca na początek z objaśnieniem, a ikona restartu odświeża bieżącą halę.

---

## Sterowanie i funkcje
* **Komputer (PC):** poruszanie (`WASD` / strzałki lub kliknięcie na planszy) oraz akcje (`Spacja` / `E` / przyciski na ekranie).
* **Telefon / ekran dotykowy:** wirtualny pad kierunkowy, przycisk akcji kontekstowej, powiększone strefy dotyku oraz układ dopasowany do orientacji pionowej i poziomej.
* **Wersje językowe:** **PL** (domyślna), **EN**, **DE** (nazwa główna pozostaje w dwóch liniach łamanych na dwukropku: `HIGH VOLTAGE:` / `LEON'S TEAM`).
* **Dźwięk i instalacja:** muzyka w tle i efekty zdarzeń generowane przez Web Audio API z przyciskiem szybkiego wyciszania (`Dźwięk`) oraz opcją instalacji jako aplikacja webowa (PWA).

---

## Technologie
* HTML5 Canvas, CSS3, Vanilla JavaScript
* Web Audio API (synteza dźwięku w przeglądarce)
* Obsługa PWA / dodawania do ekranu głównego