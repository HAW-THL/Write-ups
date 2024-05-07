# endianness [200]
## Team: cleme, woehnert, Noerten, Michael, z0

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/d009728f-0cd7-4c64-8190-b09366167d26)

- Login mit NCat.

```bash
nc titan.picoctf.net 50558
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/77a390c9-020d-4336-8e75-39b97ae72981)

- Das Wort: "vlqap" konvertieren wir jetzt mit [CyberChef](https://gchq.github.io/CyberChef/) zu Hex.

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/ff39a85c-8ae0-4079-87f4-c69307f2f18c)

```
76 6c 71 61 70
```
- Das Ergebnis ist nun unser "Big Endian".
- Diesen können wir jetzt wieder mit CyberChef zu dem "Little Endian" umwandeln, allerdings bevorzuge ich eher [save-editor](https://www.save-editor.com/tools/wse_hex.html).

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/95982343-9769-4f44-8130-d68830c4faf1)

```
70 61 71 6c 76
```
- Dieses Ergebnus ist nun unser 'Little Endian".

> Hier ist eine Grafik, die den Hinterrgundprozess erklärt
![image](https://de.wikipedia.org/wiki/Byte-Reihenfolge#/media/Datei:32bit-Endianess.svg)
