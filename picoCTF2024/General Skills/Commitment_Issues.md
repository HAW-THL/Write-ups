# Commitment Issues [50]
## Team: patry, Noerten, z0

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/b9e80ad7-b42e-4698-b5d4-18ca6519aa82)

- Download die gegebene Datei "challenge.zip":
```
wget https://artifacts.picoctf.net/c_titan/75/challenge.zip
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/2c33340d-d6c8-4cf4-837a-09a91447e706)

- Entpacke die Zip-Datei:
```
unzip challenge.zip
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/354c2f88-817f-4ce7-b573-7307e9983ecf)

- Wir schauen uns an, was im Ordner "drop-in" zu finden ist:
```
cd drop-in/ && ls -la
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/7b468c16-84de-452b-ae5c-02ca115c7604)

- Nun schauen wir uns die "message.txt" an:
```
cat message.txt
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/048ec8d6-03a5-4aae-8303-f89664de13fe)

- Mit dem Inhalt der "message.txt" können wir noch nichts anfangen, daher schauen wir uns zu nächst, die Logs, des versteckten Ordner ".git" an:
```
git log
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/f71b20be-4c7b-49a5-9d3e-43ffb6548a38)

- Hier sehen wir, welche vorherigen Commits gemacht wurden. Eine davon zeigt "create flag" mit der ID "6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2".

- Mit "Checkout" können wir vergangene Commits mit den IDs wechseln:

```
git checkout 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/69e83290-fd62-41bb-af39-5d4a4b2b32af)

- Um die Flag zu finden, schauen wir uns nun noch einmal die "message.txt" an:

```
cat message.txt
```

![image](https://github.com/HAW-THL/Write-ups/assets/90260119/4cc50399-9336-422c-8c1e-ecb35cfa48e3)

```
picoCTF{s@n1t1z3_9539be6b}
```
