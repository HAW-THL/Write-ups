# dont-you-love-banners [300]
## Team: cleme, woehert, Noerten, z0

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/7ce9fdda-eb17-48bc-a8cb-f1335fca8011)

- Login in den ersten Server mit NetCat.
```
nc tethys.picoctf.net 61371
```
![image](https://github.com/HAW-THL/Write-ups/assets/90260119/9b740f26-350d-47a7-9249-c846b9076bd2)

- Hier sehen wir zweierlei: die SSH-Version und etwas, was auf ein Passwort hinweist, welches wir für den nächsten Server brauchen.

- Jetzt logen wir uns in den zweiten Server ein.
```
nc tethys.picoctf.net 58476
```
![image](https://github.com/HAW-THL/Write-ups/assets/90260119/cd451afd-1c8d-44bc-ad94-5a5e365bded3)

- Hier beantworten wir die Fragen und sind in der Shell.

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/175214fd-d64b-46c8-9993-2ec25cc0764c)

- Zu erst schauen wir mit "ls" und sehen "banner" das ist der Banner vom Anfang und "text" welcher ausgibt "keep digging".
- Danach suchen wir im Elternverzeichnis.
- Nach ein bisschen "digging" finden wir das root Verzeichnis, in dem wir zwei Datein "flag.txt" und "script.py" finden. 

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/2d0c4ead-89ea-4c55-a80a-366b95a7b434)

- Leider können wir die "flag.txt" nicht lesen aber "script.py" führt das selbe Programm aus, wie wenn man sich auf den Server verbindet.
- Das Banner ist das selbe, wie im "player" Verzeichnis.

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/f883b697-49da-4c8e-b196-24deefdd8dc7)

- Nun können wir zurück ins "player" Verzeichnis gehen und das originale Banner löschen.
- Danach erstellen wir einen [Symlink](https://en.wikipedia.org/wiki/Symbolic_link) von der Flagge, im "player" Verzeichnis, die wir "banner" nennen.
```
ln -s /root/flag.txt banner
```
> Dieser Befehl erstellt einen symbolischen Link namens "banner" im aktuellen Verzeichnis, der auf die Datei "/root/flag.txt" verweist. Symbolische Links sind Verknüpfungen zu Dateien oder Verzeichnissen, die auf andere Dateien oder Verzeichnisse verweisen. In diesem Fall würde der symbolische Link "banner" auf die Datei "/root/flag.txt" zeigen.

- Jetzt können wir uns erneut mit dem Server verbinden, sodass wir bei der Verbindung mit dem Server nicht das eigentliche Banner, sondern die Flagge lesen.

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/3648bf51-1c7c-4914-8e60-a7138843cfc8)

```
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_218ef5d6}
```
