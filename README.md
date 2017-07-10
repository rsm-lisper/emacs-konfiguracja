![warning lisp](http://lisper.pl/gfx/lisplogo_warning_128.png)

# emacs-konfiguracja
ponieważ emacs to rewelacyjny (z wielu powodów) wielofunkcyjny edytor i środowisko pracy, ale niestety domyślna konfiguracja jest oszałamiająco uboga.

## jak działa konfiguracja w emacs'ie?
emacs dla konfiguracji jak większość aplikacji w lispie nie stosuje odrębnej składni dla konfiguracji. konfigurację stanowi kod, który po wczytaniu emacs'a jest uruchamiany. tak więc konfiguracja to tak na prawdę zmiany na działającej aplikacji. co za tym idzie możemy je robić w każdej chwili i możemy dowolnie przekonfigurować emacs'a w trakcie pracy.

emacs wczytuje konfigurację z pliku `~/.emacs` lub jeśli taki nie istnieje wczytuje z `~/.emacs.d/init.el`. z mojego doświadczenia plik `~/.emacs` jest wygodny, gdy całość konfiguracji swobodnie mieści się w pojedynczym pliku. niestety gdy konfiguracja rośnie i zaczynają pojawiać się warianty (do domu, pracy etc), pojedynczy plik staje się ograniczający i wtedy wygodniej jest przenieść się z konfiguracją do podkatalogu w którym emacs trzyma różne swoje rzeczy `~/.emacs.d/`, do pliku `init.el`.

ja zastosowałem tutaj tą drugą wersję. sekcje rzadziej używane są w podkatalogu `init/` i można je wedle potrzeby wczytać ręcznie lub odkomentować ich wczytywanie w pliku z konfiguracją główną `init.el`.

## instalacja
- sklonować repozytorium do domowego katalogu emacs'a:
```shell
cd ~/.emacs.d
git clone  .
```
- ustawić niezbędne dane w pliku `init.el`

## zawartość
 - `init.el` - zawiera podstawową konfigurację, tu także wczytywane są ew dodatkowe sekcje z katalogu `init/`
 - `init/15-misc.el` - drobiazgi z którymi jeszcze nie wiem co zrobić
 - `init/90-ruby.el` - większość rzeczy związanych z obsługą ruby jest średnio stabilna, wolę więc mieć to osobno i użyć jeżeli będę potrzebował

## materiały w sieci:
- gnu emacs manual - the emacs initialization file:
https://www.gnu.org/software/emacs/manual/html_node/emacs/Init-File.html

### inne konfiguracje prywatne:
przykłady konfiguracji różnych ludzi są w przypadku emacs'a bezcennym źródło wiedzy i pomysłów!
- darren smith - simple emacs configuration:
http://homepages.inf.ed.ac.uk/s0243221/emacs/
- aaron bedra's emacs 24 configuration:
http://aaronbedra.com/emacs.d/
