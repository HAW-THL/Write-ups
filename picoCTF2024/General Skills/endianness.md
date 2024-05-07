# endianness [200]
## Team: cleme, woehnert, Noerten, Michael, z0

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/d009728f-0cd7-4c64-8190-b09366167d26)

- Login mit NCat.

```
nc titan.picoctf.net 65351
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/4c44322b-b4d6-4ba9-a282-221b101ec460)

- Das Wort: "oyqci" konvertieren wir jetzt mit [CyberChef](https://gchq.github.io/CyberChef/) zu Hex.

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/8376a717-4bb9-46ae-87df-629659e142d6)

```
6f 79 71 63 69
```
- Das Ergebnis ist nun unser "Big Endian".
- Diesen können wir jetzt wieder mit CyberChef zu dem "Little Endian" umwandeln, allerdings bevorzuge ich eher [save-editor](https://www.save-editor.com/tools/wse_hex.html).

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/30454a29-3422-49fc-add9-df2c9aacbaeb)

```
69 63 71 79 6f
```
- Dieses Ergebnis ist nun unser 'Little Endian".

> Hier ist eine Grafik, die den Hinterrgundprozess erklärt

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/74078ce7-7d82-42d4-bcdf-398062de5ca4)

- Nun geben wir unsere Ergebnisse ein.

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/6263976c-a267-4969-a5f4-eab044162ac3)

```
picoCTF{3ndi4n_sw4p_su33ess_25c5f083}
```
