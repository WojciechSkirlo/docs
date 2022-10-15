---
outline: deep
---

<script setup>
import { onMounted } from 'vue'

let version = $ref()

onMounted(async () => {
  const res = await fetch('https://api.github.com/repos/vuejs/core/releases?per_page=1')
  version = (await res.json())[0].name
})
</script>

# Wydania

<p v-if="version">
Aktualna najnowsza stabilna wersja Vue to <strong>{{ version }}</strong>.
</p>
<p v-else>
Sprawdzanie najnowszej wersji...
</p>

Pełny wykaz zmian w poprzednich wydaniach jest dostępny na [GitHub](https://github.com/vuejs/core/blob/main/CHANGELOG.md).

## Cykl wydawania

Vue nie ma ustalonego cyklu wydawania.

- Poprawki są wydawane w miarę potrzeb.

- Mniejsze wydania zawsze zawierają nowe funkcje, z typowym odstępem czasowym 3~6 miesięcy. Mniejsze wydania zawsze przechodzą przez fazę beta przed wydaniem.

- Duże wydania są ogłaszane z wyprzedzeniem i przechodzą fazę wczesnej dyskusji oraz fazę przedpremierową alfa/beta.

## Przypadki brzegowe wersjonowania semantycznego

Wydania Vue oparte są na [wersjonowaniu semantycznym](https://semver.org/) z kilkoma przypadkami brzegowymi.

### Definicje TypeScript

Możemy dostarczyć niekompatybilne wstecznie zmiany w definicjach TypeScript pomiędzy **mniej ważnymi** wersjami, ponieważ:

1. Czasem TypeScript sam w sobie dostarcza niekompatybilne wstecznie zmiany pomiędzy mniej ważnymi wersjami i możemy zaaktualizować typy w celu wsparcia nowszych wersji TypeScript.

2. Okazjonalnie możemy dopasować funkcjonalności, które dostępne są w nowszych wersjach TypeScript, podnosząc przy tym wymaganą do działania minimalną wersję TypeScript.

Jeżeli używasz TypeScript, możesz użyć zakresu semver będącego na obecnej, mniej ważnej wersji i manualnie dokonać jej aktualizacji przy nowym wydaniu mniej ważnej wersji Vue.


## Kompatybilność skompilowanego kodu z starszym środowiskiem uruchomieniowym

Nowsza **mniej ważna** wersja kompilatora Vue może stworzyć kod, który jest niekomaptybilny z środowiskiem uruchomieniowym Vue w starszej, mniej ważnej wersji. Przykładowo, kod stworzony przez kompilator Vue 3.2 może nie być w pełni kompatybilny, jeżeli zostanie uruchomiony w środowisku uruchomieniowym Vue 3.1.

Niedopasowanie wersji może zdarzyć się tylko w przypadku, gdy dostarczasz prekompilowany kod komponentu Vue jako paczka, a użytkownik używa go w projekcie używającym starszej wersji Vue. W konsekwencji, twoja paczka może potrzebować dokładnego zadeklarowania minimalnej, wymaganej, mniej ważnje wersji Vue.

## Wydania przedpremierowe

Mniej ważne wydania zazwyczaj przechodzą przez nieustaloną liczbę wydań wersji beta. Ważne wersje przechodzą przez fazy alpha oraz beta.

Wydania przedpremierowe są przeznaczone dla integracji / testowania stabilności oraz dla wczesnych adoptujących, aby udostępnić feedback dla niestabilnych funkcjonalności. Nie używaj wydań przedpremierowych w trybie produkcyjnym. Każde wydanie przedpremierowe jest uznawane za niestabilne i może przynieść niekompatybilne wstecznie zmiany pomiędzy wersjami, zatem zawsze przypinaj dokładne wersje gdy używasz przedpremierowych wydań.

## Przestarzałość

Możemy od czasu do czasu uznać funkcjonalności za przestarzałe takie, które mają nowe, lepsze zastępstwo w mniej ważnych wydaniach. Takie funkcjonalności bedą dalej działać i zostaną usunięte w następnym, głównym wydaniu po osiągnięciu statusu przestarzałego.

## RFC

Nowe funkcjonalności ze znacznym wpływem na API oraz ważne zmiany wprowadzane do Vue przechodzą przez proces **Request for Comments** (RFC). Proces ten ma na celu zapewnienie spójnej i kontrolowanej ścieżki dla nowych funkcjonalności w celu dodania ich do frameworka, a także do dania użytkownikow możliwości do uczestniczenia i oferowania feedbacku w procesie designowania.

Proces RFC jest przeprowadzany w repozytorium [vuejs/rfcs](https://github.com/vuejs/rfcs) na GitHub.

## Eksperymentalne funkcjonalności

Niektóre funkcjonalności są dostarczanie i dokumentowane w stabilnej wersji Vue, ale oznaczone jako eksperymentalne. Eksperymentalne funkcjonalności są zazwyczaj takimi, które mają powiązane RFC z większością rozwiązanych problemów dotyczących designu na papierze, ale wciąż z brakującym feedbackiem z przypadków rzeczywistego użycia.

Celem eksperymentalnych funkcjonalności jest pozwolenie użytkownikom na dostarczenie feedbacku dla nich poprzez testowanie w trybie produkcyjnym, bez konieczności używania niestabilnej wersji Vue. Eksperymentalne funkcjonalności są uważane za niestabilne i powinny być używanie jedynie w kontrolowany sposób z świadomością, że mogą one się zmienić pomiędzy dowolnymi wydaniami.
