# VoberMs
VoberMs to przeglądarkowe narzędzie stworzone w celu ułatwienia pracy nad serwerem, czyli wizualnego rozmieszczania obiektów 3D (takich jak Moby i Voby) na trójwymiarowej mapie. Aplikacja wykorzystuje bibliotekę Three.js do renderowania sceny 3D i zapewnia interfejs użytkownika do zarządzania obiektami.

## Główne Funkcje

*   **Wizualizacja 3D:** Ładuje i wyświetla model mapy w formacie GLB.
*   **Ładowanie Modeli:** Wczytuje definicje dostępnych obiektów (Mobów i Vobów) z plików JSON.
*   **Umieszczanie Obiektów:**
    *   **Przeciągnij i Upuść:** Modele można przeciągać z panelu bocznego bezpośrednio na mapę.
    *   **Przeglądarka Modeli:** Wizualna przeglądarka z podglądami modeli umożliwia wyszukiwanie i wybieranie obiektów do umieszczenia.
*   **Edycja Obiektów:**
    *   **Gizmo (TransformControls):** Interaktywne manipulatory (strzałki, łuki) do precyzyjnego przesuwania i obracania obiektów w przestrzeni 3D.
    *   **Panel Edytora Pozycji:** Panel wyświetlający i pozwalający na edycję współrzędnych (w systemie gry) oraz rotacji wybranego obiektu, zsynchronizowany z Gizmo.
    *   **Menu Kontekstowe:** Szybki dostęp do akcji (Edytuj, Przesuń, Kopiuj, Usuń) po kliknięciu prawym przyciskiem myszy na obiekcie.
*   **Współrzędne Gry:** Narzędzie operuje na współrzędnych używanych w grze, zapewniając funkcje konwersji do/z systemu współrzędnych Three.js. Bieżące współrzędne kursora są wyświetlane na ekranie.
*   **Wydajność:** Wykorzystuje `InstancedMesh` do renderowania wielu kopii tego samego modelu, co znacząco poprawia wydajność przy dużej liczbie obiektów.
*   **Import/Export:**
    *   **Statyczne Voby Mapy:** Możliwość importowania predefiniowanych obiektów mapy.
    *   **Stan Użytkownika:** Możliwość eksportowania i importowania stanu wszystkich obiektów umieszczonych przez użytkownika do/z pliku tekstowego (format `addMob("Nazwa", X, Y, Z, RotY)`).
*   **Widoczność Etykiet:** Opcje kontrolowania widoczności etykiet z nazwami obiektów (globalnie lub dla poszczególnych typów modeli).
*   **Tryb Podglądu Gry:** Uproszczony tryb pierwszej osoby pozwalający "przejść się" po mapie z umieszczonymi obiektami, sterowany klawiszami W/A/S/D.
*   **Pomoc:** Wbudowane okno pomocy opisujące podstawowe sterowanie i funkcje.

## Użycie / Uruchomienie

Narzędzie jest aplikacją webową działającą w całości po stronie przeglądarki.

1.  **Pobierz/Sklonuj:** Pobierz pliki projektu.
2.  **Otwórz `index.html`:** Otwórz plik `index.html` w nowoczesnej przeglądarce internetowej wspierającej moduły ES6 (np. Chrome, Firefox, Edge).

## Technologie

*   JavaScript (ES Modules)
*   [Three.js](https://threejs.org/) (Biblioteka 3D)
*   HTML5
*   CSS3
