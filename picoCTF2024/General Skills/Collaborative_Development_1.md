# Collaborative Development [75]
## Team: woehnert, Moritz, z0

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/0f177702-3439-498a-aa97-34959104ccbc)

---

- Downloade die gegebene Datei "challenge.zip":
```shell
wget https://artifacts.picoctf.net/c_titan/69/challenge.zip
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/96cd13b4-4106-4c79-a049-a3e16dbf132d)

---

- Entpacke die Zip-Datei:
```shell
unzip challenge.zip
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/4775ce17-8593-4d29-8290-6aea75378aa5)

---

- Wir schauen uns an, was im Ordner "drop-in" zu finden ist:
```shell
cd drop-in/ && ls -la
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/76a63dcc-059b-4f86-9ac9-f72c5b359406)

---

- Nun sehen wir uns alle aktuellen Branches an:
```shell
git branch -a
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/5f66f754-74b9-4f87-a2a9-3a2de41cd9a0)

---

- Es gibt drei Branches und jeder trägt einen Teil der Flag. Man könnte jetzt entweder alle Flags abrufen und einzeln aufschreiben oder alle Flags zu einer "Hauptflag" zusammen führen, um dabei mögliche Probleme auszuschließen:
```shell
git checkout feature/part-1 && cat flag.py && git checkout feature/part-2 && cat flag.py && git checkout feature/part-3 && cat flag.py
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/b41bb399-1005-496a-9c60-9b0bdd02172c)

---

```shell
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb}
```
