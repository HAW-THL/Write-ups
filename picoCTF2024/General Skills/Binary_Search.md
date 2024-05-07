# Binary Search [100]
## Team: woehnert, Noerten, Michael, z0

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/42a3b3a7-d753-48cd-a046-2f50f6c7b090)

- Login mit SSH:
```bash
ssh -p 52760 ctf-player@atlas.picoctf.net
```
- Passwort eingeben:
```
84b12bae
```

- Fingerprint mit "Yes" akzeptieren.

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/f145c332-bd36-46a3-a082-6638444ebb0e)

- 500
> Immer mit 500 starten, da es die Hälfte von 1 und 1000 ist.

- 750
> Damit wir den größt möglichen Bereich eingrenzen können, tasten wir uns mit 750 ran.

- 600
> 750 ist zu hoch, 600 zu niedrig.

- 650
> höher als 600 aber niedriger als 650.

- 625
> Hälfte nehmen um wieder den größt möglichen Bereich zu testen.

- 615
> bei 615 Glück gehabt.

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/7a2fdf2f-a3d5-4c9e-818f-94f4d0fad8a1)

```
picoCTF{g00d_gu355_2e90d29b}
```
