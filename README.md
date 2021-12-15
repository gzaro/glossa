# ΓΛΩΣΣΑ

## Χρήσιμα

- [Διερμηνευτής](https://gloglossa.gr/)
- [Σχολικό βιβλίο](http://ebooks.edu.gr/ebooks/v/pdf/8547/2560/22-0275-01_Anaptyxi-Efarmogon-se-Programmatistiko-Perivallon_G-Lykeiou-SpOikPlir_Vivlio-Mathiti/)

## Σύνταξη

- [Δομή προγράμματος](#structure)
- [Τύποι δεδομένων](#types)
- [Αριθμητικοί τελεστές](#numeric-operators)
- [Αριθμητικές συναρτήσεις](#numeric-functions)

### Δομή προγράμματος {#structure}

Η πρώτη εντολή κάθε προγράμματος είναι υποχρεωτικά η επικεφαλίδα του προγράμματος, η οποία είναι η λέξη ΠΡΟΓΡΑΜΜΑ ακολουθούμενη από το όνομα του προγράμματος.

Στη συνέχεια ακολουθεί το τμήμα δήλωσης των σταθερών του προγράμματος, αν βέβαια το πρόγραμμά μας χρησιμοποιεί σταθερές.

Αμέσως μετά είναι το τμήμα δήλωσης μεταβλητών, όπου δηλώνονται υποχρεωτικά τα ονόματα όλων των μεταβλητών καθώς και ο τύπος τους. Ακολουθεί το κύριο μέρος του προγράμματος, που περιλαμβάνει όλες τις εκτελέσιμες εντολές. Οι εντολές αυτές περιλαμβάνονται υποχρεωτικά ανάμεσα στις λέξεις ΑΡΧΗ και ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ.

Αν ο πρώτος χαρακτήρας είναι το θαυμαστικό (!), σημαίνει ότι αυτή η γραμμή περιέχει σχόλια και όχι εκτελέσιμες εντολές.

~~~
! Αυτό το πρόγραμμα υπολογίζει την περίμετρο ενός κύκλου

ΠΡΟΓΡΑΜΜΑ ΠερίμετροςΚύκλου

ΣΤΑΘΕΡΕΣ
  π = 3.14
  
ΜΕΤΑΒΛΗΤΕΣ
  ΠΡΑΓΜΑΤΙΚΕΣ: Ακτίνα
  
! Οι κενές γραμμές και τα σχόλια δεν επηρεάζουν την εκτέλεση
  
ΑΡΧΗ 

  ΓΡΑΨΕ 'Δώσε την ακτίνα'
  ΔΙΑΒΑΣΕ Ακτίνα
  
  ΓΡΑΨΕ 'Η περίμετρος του κύκλου είναι ', 2 * π * Ακτίνα
  
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

> Δώσε την ακτίνα
>
> 1.5
>
> Η περίμετρος του κύκλου είναι 9.42

### Τύποι δεδομένων {#types}

Οι τύποι δεδομένων που υποστηρίζει η ΓΛΩΣΣΑ είναι οι αριθμητικοί, που περιλαμβάνουν τους ακέραιους και τους πραγματικούς αριθμούς, οι χαρακτήρες και τέλος οι λογικοί.

**Ακέραιος τύπος**. Ο τύπος αυτός περιλαμβάνει τους ακέραιους που είναι γνωστοί από τα μαθηματικά. Οι ακέραιοι μπορούν να είναι θετικοί, αρνητικοί ή μηδέν. Παραδείγματα ακεραίων είναι οι αριθμοί 1, 3409, 0, -980.

**Πραγματικός τύπος**. Ο τύπος αυτός περιλαμβάνει τους πραγματικούς αριθμούς που γνωρίζουμε από τα μαθηματικά. Οι αριθμοί 3.14159, 2.71828, -112.45, 0.45 είναι πραγματικοί αριθμοί. Και οι πραγματικοί αριθμοί μπορούν να είναι θετικοί, αρνητικοί ή μηδέν.

**Χαρακτήρας**. Ο τύπος αυτός αναφέρεται τόσο σε ένα χαρακτήρα όσο και μία σειρά χαρακτήρων. Τα δεδομένα αυτού του τύπου μπορούν να περιέχουν οποιονδήποτε χαρακτήρα παράγεται από το πληκτρολόγιο. Παραδείγματα χαρακτήρων είναι 'Κ', 'Κώστας', 'σήμερα είναι Τετάρτη', 'Τα πολλαπλάσια του 15 είναι'. Οι χαρακτήρες πρέπει υποχρεωτικά να βρίσκονται μέσα σε απλά εισαγωγικά, ' '. Τα δεδομένα αυτού του τύπου, επειδή περιέχουν τόσο αλφαβητικούς όσο και αριθμητικούς χαρακτήρες, ονομάζονται συχνά αλφαριθμητικά.

**Λογικός**. Αυτός ο τύπος δέχεται μόνο δύο τιμές: ΑΛΗΘΗΣ και ΨΕΥΔΗΣ. Οι τιμές αντιπροσωπεύουν αληθείς ή ψευδείς συνθήκες.

~~~
ΠΡΟΓΡΑΜΜΑ ΔοκιμήΤύπωνΔεδομένων
  
ΜΕΤΑΒΛΗΤΕΣ
  ΑΚΕΡΑΙΕΣ: χ
  ΠΡΑΓΜΑΤΙΚΕΣ: ψ
  ΧΑΡΑΚΤΗΡΕΣ: μήνυμα
  ΛΟΓΙΚΕΣ: χ_μεγαλύτερος
  
ΑΡΧΗ 

  ΓΡΑΨΕ 'Δώσε χ'
  ΔΙΑΒΑΣΕ χ
  
  ΓΡΑΨΕ 'Δώσε ψ'
  ΔΙΑΒΑΣΕ ψ
  
  χ_μεγαλύτερος <- χ > ψ
  
  μήνυμα <- 'Η πρόταση χ > ψ είναι '
  
  ΑΝ χ_μεγαλύτερος ΤΟΤΕ
  	ΓΡΑΨΕ μήνυμα, 'ΑΛΗΘΗΣ'
  ΑΛΛΙΩΣ
  	ΓΡΑΨΕ μήνυμα, 'ΨΕΥΔΗΣ'
  ΤΕΛΟΣ_ΑΝ
  
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

> Δώσε χ
>
> 1
>
> Δώσε ψ
>
> 0.9
>
> Η πρόταση χ > ψ είναι ΑΛΗΘΗΣ

### Αριθμητικοί τελεστές {#numeric-operators}

| ΑΡΙΘΜΗΤΙΚΟΣ ΤΕΛΕΣΤΗΣ | ΠΡΑΞΗ |
|---|---|
| + | Πρόσθεση |
| - | Αφαίρεση |
| * | Πολλαπλασιασμός |
| / | Διαίρεση |
| ^ | Ύψωση σε δύναμη |
| DIV | Ακέραια διαίρεση |
| MOD | υπόλοιπο ακέραιας διαίρεσης |

### Αριθμητικές συναρτήσεις {#numeric-functions}

| ΣΥΝΤΑΞΗ | ΕΠΙΣΤΡΕΦΕΙ |
|---|---|
| ΗΜ(Χ) | Ημίτονο |
| ΣΥΝ(Χ) | Συνημίτονο |
| ΕΦ(Χ) | Εφαπτομένη |
| Τ_Ρ(Χ) | Τετραγωνική ρίζα |
| ΛΟΓ(Χ) | Φυσικός λογάριθμος |
| Ε(Χ) | e<sup>x</sup> |
| Α_Μ(Χ) | Ακέραιο μέρος του Χ |
| Α_Τ(Χ) | Απόλυτη τιμή του Χ |
