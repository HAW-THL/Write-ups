# Collaberative Development
## Team: Noerten, Michael, Nasty, Ryu


*herunterladen der challenge.zip*

wget https://artifacts.picoctf.net/c_titan/69/challenge.zip

*entpacken der Challenge.zip*

unzip challenge.zip

*anzeigen der Verzeichnisstruktur*

ls -a

*ins drop-in Verzeichnis wechseln*

cd drop-in

*git branch um die branches anzuzeigen*

┌──(kali㉿Noertbook)-[~/Pico/CollabDev/drop-in]
└─$ git branch
  feature/part-1
  feature/part-2
  feature/part-3
* main

*in den Part-3 Branch wechseln*

git switch feature/part-3

*inhalt der Part-3 Branch anschauen*

└─$ git show
commit 1308521d0d0b66df1a73e91d5d9e2d74610002e3 (HEAD -> feature/part-3)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    add part 3

diff --git a/flag.py b/flag.py
index 77d6cec..78ac69c 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,3 @@
 print("Printing the flag...")
+
+print("w0rk_e4b79efb}")

*wechseln in den part-2*

┌──(kali㉿Noertbook)-[~/Pico/CollabDev/drop-in]
└─$ git switch feature/part-2
Switched to branch 'feature/part-2'

*den Inhalt des Branches Part-2 anzeigen*

┌──(kali㉿Noertbook)-[~/Pico/CollabDev/drop-in]
└─$ git show
commit 9792a89fa347abc711f84b7208db18d164d45aca (HEAD -> feature/part-2)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    add part 2

diff --git a/flag.py b/flag.py
index 77d6cec..7ab4e25 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,3 @@
 print("Printing the flag...")
+
+print("m@k3s_th3_dr3@m_", end='')
\ No newline at end of file


*in Part-1 wechseln*

┌──(kali㉿Noertbook)-[~/Pico/CollabDev/drop-in]
└─$ git switch feature/part-1
Switched to branch 'feature/part-1'


*Inhalt von Part-1 anzeigen*

┌──(kali㉿Noertbook)-[~/Pico/CollabDev/drop-in]
└─$ git show
commit ad37f59bfdcb1e8052bf7e12e1d89a2adb315cf9 (HEAD -> feature/part-1)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    add part 1

diff --git a/flag.py b/flag.py
index 77d6cec..6e17fb3 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,2 @@
 print("Printing the flag...")
+print("picoCTF{t3@mw0rk_", end='')
\ No newline at end of file



zusammensetzen der einzelnen Print parts:

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb}
