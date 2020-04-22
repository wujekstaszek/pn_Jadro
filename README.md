# Jadra systemu Linux - projekt by Aleksander Morgała
Prosty menadżer zadań w systemie linux

Polecenie:

Napisanie programu wyświetlającego podstawowe informację (PID, opis/nazwa procesu) na temat każdego z procesów
w systemie i umożliwiającego zatrzymanie, zabicie, forkowanie i uruchamianie procesów.
W ramach przyśpieszenia pracy zostanie udostępniona dokumentacja dot. odpowiednich systemcallów.

Napisany program powinien:
- Przy braku argumentu wyświetlić wszystkie procesy działające w systemie.(./a.out)
Dla każdego procesu powinno zostać wypisane: 
UserID,
ProcessID,
Priorytet(nice),
nazwa
 
- Po podaniu parametru -fork utworzyć kopię programu i wypisać swój PID(./a.out -fork) - kopia powinna wypisać swój pid oraz pid swojego rodzica.

- Po podaniu parametru -close <PID> zamknąć "łagodnie" program o podanym PID(./a.out -close 10).

Język do wyboru spośród c oraz c++.
Pomoce:
Prezentacja w formie filmu - https://www.youtube.com/watch?v=9qwW-VgKIz0,
dokumentu z przykładami - https://docs.google.com/presentation/d/1YeJ5b1pAGjtTjwa-GGi6QJ-iH_nfDCF3rQteCrKx0rE

Informację o procesach czytamy z specjalnego folderu /proc w którym znajdują się wszystkie procesy z naszego systemu. Informację o poszczególnych procesach znajdują się w plikach stat i status(to samo co stat ale opisane).

Listowanie wszystkich folderów w c - https://en.wikibooks.org/wiki/C_Programming/POSIX_Reference/dirent.h
priorytet i jego odczytywanie - http://man7.org/linux/man-pages/man2/setpriority.2.html
fork - http://man7.org/linux/man-pages/man2/fork.2.html
getpid, getparentpid - http://man7.org/linux/man-pages/man2/getpid.2.html
wysyłanie sygnału do procesu - http://man7.org/linux/man-pages/man2/kill.2.html
Tablica sygnałów które można wysłać - http://man7.org/linux/man-pages/man7/signal.7.html
Sprwadzenie priorytetu processu - http://man7.org/linux/man-pages/man2/getpriority.2.html