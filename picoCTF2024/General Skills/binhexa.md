# binhexa [75]
---
## Team: woehnert, Moritz, z0
---
![image](https://github.com/HAW-THL/Write-ups/assets/80387757/10245860-207e-49d6-8ec2-f2c0ab6968ed)

- Mit dem Kommando aus der Aufgabe landet man auf einem Netcat Server, der einen Binäroperationen rechnen lässt

```shell
nc titan.picoctf.net 62274  

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 11000001
Binary Number 2: 00111111


Question 1/6:
Operation 1: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
```

- Bei der ersten Aufgabe soll man einen Left-Shift durchführen, bei dem an das rechte Ende der Zahl eine 0 angefügt wird, das Ergebnis ist also 110000010

```shell
Enter the binary result: 110000010
Correct!

Question 2/6:
Operation 2: '&'
Perform the operation on Binary Number 1&2.
```
- Bei der zweiten Aufgabe soll man eine UND-Operation durchführen, die bitweise überprüft ob beide korrespondierenden Ziffern 1 sind. Das Ergebnis ist also 00000001

```shell
Enter the binary result: 00000001
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
```
- In der 3. Aufgabe soll eine Multiplikation durchgeführt werden. Hierfür haben wir einen Online-Rechner benutzt, das Ergebnis ist 10111101111111

```shell
Enter the binary result: 10111101111111
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
```
- In der 4. Aufgabe soll man eine Addition durchführen. Auch hierfür haben wir einen Online-Rechner benutzt. Das Ergebnis ist 100000000

```shell
Enter the binary result: 100000000
Correct!

Question 5/6:
Operation 5: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
```
- In der 5. Aufgabe soll man einen Right-Shift durchführen, dieser funktioniert wie der Left-Shift, nur nach rechts, so dass die rechteste Ziffer wegfällt. Das Ergebnis ist also 00011111

```shell
Enter the binary result: 00011111
Correct!

Question 6/6:
Operation 6: '|'
Perform the operation on Binary Number 1&2.

```
- In der 6. Aufgabe soll man die Bitwise ODER-Operation verwenden, die immer 1 ergibt, wenn bei dem jeweiligen Bit mindestens eine der Ziffern 1 ist. das Ergebnis ist also 11111111

```shell
Enter the binary result: 11111111
Correct!

Enter the results of the last operation in hexadecimal: ff
```
- Am Ende sollen wir noch das Ergebnis von Aufgabe 6 in Hexadezimal angeben. Hierfür kann man die Zahl in Viererblöcke aufteilen und in jeweils eine Hexadezimal-Ziffer konvertieren. 1111 ist die höchstmögliche Hexadezimalziffer, also f. Das Ergebnis ist also ff und bei Eingabe kriegen wir die Flag ausgegeben.

```shell
Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6ab1ad84}
```
