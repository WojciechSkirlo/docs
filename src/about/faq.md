# Często zadawane pytania

## Kto zarządza Vue?

Vue jest niezależnym, tworzonym przez społeczność projektem. Został stworzony przez [Evana You](https://twitter.com/youyuxi) w roku 2014 jako osobisty projekt. Dziś jest aktywnie nadzorowany przez [ludzi pracujących w pełnym wymiarze czasowym oraz ochotników z całego świata](/about/team), na których czele stoi Evan jako lider projektu. Możesz się dowiedzieć więcej o historii Vue w tym [filmie](https://www.youtube.com/watch?v=OrxmtDw4pVI).

Rozwój Vue jest przede wszystkim utrzymywany przez sponsoring, a od 2016 jesteśmy finansowo samowystarczalni. Jeśli ty lub twoja firma czerpie korzyści z używania Vue, rozważ [sponsorowanie nas](/sponsor/), aby wesprzeć rozwój Vue!

## Jaka jest różnica między Vue 2 a Vue 3?

Vue 3 jest aktualną i ostatnią główną wersją Vue. Zawiera ona nowe funkcjonalności, które nie są obecne w Vue 2, takie jak Teleport, Suspense oraz wielokrotny główny element w szablonie. Zawiera również niekompatybilne wstecznie z Vue 2 zmiany. Pełne informacje dostępne są w [przewodniku po migracji na Vue 3](https://v3-migration.vuejs.org/).

Pomimo różnic, większość API Vue jest identyczna między obiema głównymi wersjami, zatem większość twojej wiedzy o Vue 2 będzie aktualna w Vue 3. W szczególności, Composition API początkowo był dostępny jedynie w Vue 3, ale został przeportowany na Vue 2 i jest dostępny w [Vue 2.7](https://github.com/vuejs/vue/blob/main/CHANGELOG.md#270-2022-07-01).

Ogólnie rzecz biorąc, Vue 3 zapewnia mniejszy rozmiar plików wyjściowych, lepszą wydajność, skalowalność, a także wsparcie dla TypeScript oraz IDE. Jeżeli już teraz zaczynasz nowy projekt, zalecanym wyborem jest Vue 3. Obecnie istnieje tylko kilka powodów, dla których miałbyś rozważyć użycie Vue 2:

- Potrzebujesz wsparcia dla IE11. Vue 3 sięga do nowoczesnych funkcjonalności JavaScript i nie wspiera IE11.

- Wciąż czekasz na wydanie stabilnych, kompatybilnych z Vue 3 ważnych projektów ekosystemu, takich jak Nuxt lub Vuetify. Jest to zrozumiałe, jeśli nie chcesz używać wersji beta oprogramowania. Jednakże dostępne są już stabilne biblioteki komponentów dostępne dla Vue 3, takie jak [Quasar](https://quasar.dev/), [Naive UI](https://www.naiveui.com/) i [Element Plus](https://element-plus.org/).

Jeżeli masz zamiar migrować istniejącą aplikację opartą o Vue 2 na Vue 3, zapoznaj się z [przewodnikiem po migracji](https://v3-migration.vuejs.org/).

Vue 2.7, wydany w lipcu 2022 roku, jest ostatecznym, mniej ważnym wydaniem Vue 2. Vue 2 jest obecnie w fazie konserwacji: nie będzie otrzymywać już żadnych nowych funkcjonalności, ale będzie otrzymywać poprawy krytycznych błędów oraz bezpieczeństwa przez 18 miesięcy od daty wydania wersji 2.7. Oznacza to, że **Vue 2 osiągnie koniec życia wraz z końcem roku 2023**. Uważamy, że zapewni to wystarczająco czasu dla większości ekosystemu, aby dokonał migracji na Vue 3. Rozumiemy również, że istnieją firmy lub projekty, które nie są w stanie tego uczynić, jednocześnie nadal potrzebując spełnienia wymogów bezpieczeństwa oraz zgodności. Planujemy zapewnić rozszerzone wsparcie dla Vue 2 dla takich przypadków - jeżeli twoja firma spodziewa się używać Vue 2 po roku 2023, wybiegnij w przyszłość i zgłoś [tutaj](https://airtable.com/shrj37Zf4ZIfrxFzh) swoje zainteresowanie.

## Jakiej licencji używa Vue?

Vue is darmowym i otwartozródłowym projektem udostępnionym na [licencji MIT](https://opensource.org/licenses/MIT).

## Jakie przeglądarki obsługuje Vue?

Najnowsza wersja Vue (3.x) wspiera jedynie [przeglądarki z wsparciem dla ES2015](https://caniuse.com/es6). Wyklucza to IE11. Vue 3.x używa funkcjonalności ES2015, które nie mogą być przeportowane w przestarzałych przeglądarkach, zatem jeżeli potrzebujesz takie wspierać, musisz skorzystać z Vue 2.x.

## Czy Vue jest niezawodny?

Vue jest dojrzałym i przetestowanym w boju frameworkiem. Jest jednym z najszerzej używanych frameworków JavaScriptowych w środowiskach produkcyjnych przez ponad 1.5 miliona użytkowników oraz jest pobierany prawie 10 milionów razy na miesiąc na npm.

Vue jest używany na produkcji przez uznane marki o różnym charakterze, takie jak Wikimedia Foundation, NASA, Apple, Google, Microsoft, GitLab, Zoom, Tencent, Weibo, Bilibili, Kuaishou i nie tylko.

## Czy Vue jest szybki?

Vue 3 jest jednym z najszybszych frontendowych frameworków głównego nurtu i z łatwością obsługuje większość przypadków użycia internetowych aplikacji, bez konieczności dokonywania manualnych optymalizacji.

W testach obciążeniowych takich jak [js-framework-benchmark](https://rawgit.com/krausest/js-framework-benchmark/master/webdriver-ts-results/table.html), Vue skromnym marginesem osiąga lepsze wyniki od Reacta i Angulara. W benchmarku idzie również łeb w łeb z niektórymi z najszybszych frameworków nieużywających wirtualnego DOM na poziomie produkcyjnym.

Zauważ, że syntetyczne benchmarki, takie jak powyżej skupiają się na wydajności czystego renderowania z dedykowanymi optymalizacjami i mogą nie być w pełni reprezentatywne w porównaniu do rzeczywistych rezultatów. Jeżeli zależy ci na wydajności ładowania strony, możesz dokonać jej audytu przy użyciu [WebPageTest](https://www.webpagetest.org/lighthouse) lub [PageSpeed Insights](https://pagespeed.web.dev/). Strona ta jest napisana w Vue, z pre-renderowaniem w trybie SSG, pełną hydracją strony oraz nawigacją po stronie klienta w trybie SPA. Ma 100 punktów w wydajności na emulowanym Moto G4 z czterokrotnym obniżeniem taktowania procesora przy sieci 4G o niskiej prędkości.

Możesz dowiedzieć się więcej o tym, jak Vue automatycznie optymalizuje wydajność w czasie rzeczywistych w szczególnie wymagających przypadkach w zakładce [Przewodnik po Optymalizacji](/guide/best-practices/performance.html).

## Czy Vue jest lekki?

Gdy używasz z narzędzi do budowania, część API Vue jest ["tree-shakable"](https://developer.mozilla.org/en-US/docs/Glossary/Tree_shaking). Na przykład, jeżeli nie używasz wbudowanego komponentu `<Transition>`, nie zostanie on uwzględniony w kodzie produkcyjnym.

Aplikacja Vue będąca implementacją hello world, która używa minimalnego API waży jedynie około **16kb** uwzględniając minifikację oraz kompresję brotli. Rzeczywisty rozmiar aplikacji zależy od ilości użytych opcjonalnych funkcjonalności frameworka. W mało prawdopodobnym przypadku, gdzie aplikacja używa każdą funkcjonalność zapewnioną przez Vue, całkowity jej rozmiar wynosi około **27kb**.

Gdy używasz Vue bez narzędzia do budowania, nie tylko tracisz tree-shaking, ale musisz również uwzględnić kompilator szablonów w przeglądarce, co powoduje wzrost rozmiaru aplikacji do około **41kb**. Zatem, jeżeli używasz Vue głównie dla progresywnego ulepszania aplikacji bez jej budowania, rozważ użycie [petite-vue](https://github.com/vuejs/petite-vue) (jedynie **6kb**).

Niektóre frameworki, takie jak Svelte, używają innej strategii kompilacji, która zwraca szczególnie lekki kod wynikowy w scenariuszu z pojedynczym komponentem. Jednakże, [nasze badania](https://github.com/yyx990803/vue-svelte-size-analysis) pokazują, że różnica w rozmiarach mocno zależy od ilości komponentów w aplikacji. Podczas gdy Vue ma większy rozmiar podstawowy, tworzy mniej kodu na komponent. W rzeczywistych scenariuszach, aplikacja Vue może być lżejsza.

## Czy Vue jest skalowalny?

Tak. Pomimo powszechnego błędnego przekonania, że Vue nadaje się tylko do prostych przypadków, Vue doskonale radzi sobie z dużymi aplikacjami:

- [Single-File Components](/guide/scaling-up/sfc) zapewniają zmodularyzowany model rozwoju aplikacji pozwalający na rozwój jej rożnych części w izolacji.

- [Composition API](/guide/reusability/composables) zapewnia pierwszorzędną integrację z TypeScript oraz włącza wzorce organizacji, wyodrębniania oraz ponownego używania skomplikowanej logiki.

- [Kompleksowe narzędzia](/guide/scaling-up/tooling.html) zapewniają płynny rozwój aplikacji wraz z jej skalowaniem.

- Niższy próg wejścia oraz znakomita dokumentacja przekładają się na niższe koszty wdrożenia oraz szkolenia dla nowych programistów.

## Jak mogę pomóc w rozwoju Vue?

Doceniamy twoje zainteresowanie! Sprawdź nasz [Przewodnik dla społeczności](/about/community-guide.html).

## Czy powinienem użyć Options API czy Composition API?

Jeżeli jesteś początkujący w Vue, zapewniamy wysokopoziomowe [porównanie](/guide/introduction.html#which-to-choose) pomiędzy obiema opcjami.

Jeżeli już wcześniej używałeś Options API i obecnie testujesz Composition API, sprawdź [FAQ](/guide/extras/composition-api-faq).

## Czy w Vue powinienem użyć JavaScript czy TypeScript?

While Vue itself is implemented in TypeScript and provides first-class TypeScript support, it does not enforce an opinion on whether you should use TypeScript as a user.

TypeScript support is an important consideration when new features are added to Vue. APIs that are designed with TypeScript in mind are typically easier for IDEs and linters to understand, even if you aren't using TypeScript yourself. Everybody wins. Vue APIs are also designed to work the same way in both JavaScript and TypeScript as much as possible.

Adopting TypeScript involves a trade-off between onboarding complexity and long-term maintainability gains. Whether such a trade-off can be justified can vary depending on your team's background and project scale, but Vue isn't really an influencing factor in making that decision.

Podczas gdy Vue jest napisany w TypeScript oraz zapewnia z nim pierwszorzędną integrację, nie wymusza na tobie tego, czy powinieneś go używać jako użytkownik.

Wsparcie dla TypeScript jest ważnym punktem do rozważenia podczas dodawania nowych funkcjonalności do Vue. API, które są zaprojektowane z myślą o TypeScript są zazwyczaj łatwiejsze do zrozumienia przez IDE i lintery, nawet jeśli samemu go nie używasz. Każdy wygrywa. API Vue jest również zaprojektowane z myślą o działaniu zarówno w JavaScript i TypeScript w takim samym stopniu, jak tylko to możliwe.

Przyjęcie TypeScript wiąże się z kompromisem między złożonością onboardingu a długoterminowymi korzyściami w zakresie utrzymywania kodu. To, czy taki kompromis może być uzasadniony, może się różnić w zależności od doświadczenia zespołu i skali projektu, ale Vue nie jest tak naprawdę czynnikiem wpływającym na podjęcie tej decyzji.

## Jak Vue wypada w porównaniu z Web Components?

Vue zostało stworzone zanim Web Components były dostępne natywnie, a niektóre aspekty Vue (takie jak sloty) zostały zainspirowane Web Components.

Specyfikacja Web Components jest stosunkowo niskopoziomowa, ponieważ skupia się na definiowaniu elementów niestandardowych. Jako framework, Vue rozwiązuje dodatkowe problemy wyższego rzędu, takie jak wydajne renderowanie DOM, reaktywne zarządzanie stanem aplikacji, narzędzia, routing po stronie klienta i renderowanie po stronie serwera.

Vue w pełni obsługuje też przetwarzanie lub eksportowanie do natywnych elementów niestandardowych – więcej informacji znajdziesz w [Przewodniku po Vue i Web Components](/guide/extras/web-components).

<!-- ## TODO How does Vue compare to React? -->

<!-- ## TODO How does Vue compare to Angular? -->
