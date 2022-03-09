# [ΓΛΩΣΣΑ](https://gzaro.github.io/glossa)

## Χρήσιμα

- [Διερμηνευτής](https://gloglossa.gr/)
- [Σχολικό βιβλίο](http://ebooks.edu.gr/ebooks/v/pdf/8547/2560/22-0275-01_Anaptyxi-Efarmogon-se-Programmatistiko-Perivallon_G-Lykeiou-SpOikPlir_Vivlio-Mathiti/)

## Σύνταξη

- [Δομή προγράμματος](#structure)
- [Τύποι δεδομένων](#types)
- [Αριθμητικοί τελεστές και αριθμητικές συναρτήσεις](#numeric-operators-functions)
- [Συγκριτικοί τελεστές](#comparison-operators)
- [Λογικοί τελεστές](#logigal-operators)
- [Εντολές επιλογής](#selection)
- [Εντολές επανάληψης](#loops)

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

### Αριθμητικοί τελεστές και αριθμητικές συναρτήσεις {#numeric-operators-functions}

| ΑΡΙΘΜΗΤΙΚΟΣ ΤΕΛΕΣΤΗΣ | ΠΡΑΞΗ |
|---|---|
| + | Πρόσθεση |
| - | Αφαίρεση |
| * | Πολλαπλασιασμός |
| / | Διαίρεση |
| ^ | Ύψωση σε δύναμη |
| DIV | Ακέραια διαίρεση |
| MOD | υπόλοιπο ακέραιας διαίρεσης |

| ΣΥΝΑΡΤΗΣΗ | ΕΠΙΣΤΡΕΦΕΙ |
|---|---|
| ΗΜ(Χ) | Ημίτονο |
| ΣΥΝ(Χ) | Συνημίτονο |
| ΕΦ(Χ) | Εφαπτομένη |
| Τ_Ρ(Χ) | Τετραγωνική ρίζα |
| ΛΟΓ(Χ) | Φυσικός λογάριθμος |
| Ε(Χ) | e<sup>x</sup> |
| Α_Μ(Χ) | Ακέραιο μέρος του Χ |
| Α_Τ(Χ) | Απόλυτη τιμή του Χ |

~~~
! Υπολογίζει το έργο σταθερής δύναμης
! https://el.wikipedia.org/wiki/%CE%88%CF%81%CE%B3%CE%BF_(%CF%86%CF%85%CF%83%CE%B9%CE%BA%CE%AE)#%CE%A3%CF%84%CE%B1%CE%B8%CE%B5%CF%81%CE%AE_%CE%B4%CF%8D%CE%BD%CE%B1%CE%BC%CE%B7

ΠΡΟΓΡΑΜΜΑ ΥπολογισμόςΈργου
  
ΜΕΤΑΒΛΗΤΕΣ
  ΠΡΑΓΜΑΤΙΚΕΣ: F, x, θ, W
  
ΑΡΧΗ 
  ΓΡΑΨΕ 'Δώσε δύναμη Fx (σε Ν)'
  ΔΙΑΒΑΣΕ F
  
  ΓΡΑΨΕ 'Δώσε τη μετατόπιση x (σε m)'
  ΔΙΑΒΑΣΕ x
  
  ΓΡΑΨΕ 'Δώσε τη γωνία θ που σχηματίζει η F με την μετατόπιση'
  ΔΙΑΒΑΣΕ θ
  
  W <- F * x * ΣΥΝ(θ)
  
  ΓΡΑΨΕ 'Το έργο είναι ', W, ' Joule'
  
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

>Δώσε δύναμη Fx (σε Ν)
>
>1
>
>Δώσε τη μετατόπιση x (σε m)
>
>10
>
>Δώσε τη γωνία θ που σχηματίζει η F με την μετατόπιση
>
>45
>
>Το έργο είναι 7.00 Joule

### Συγκριτικοί τελεστές {#comparison-operators}

| Τελεστής | Ελεγχόμενη σχέση | Παράδειγμα |
|---|---|---|
| = | Ισότητα | Αριθμός = 0 |
| <> | Ανισότητα | ονομα1 <> 'Κώστας' |
| > | Μεγαλύτερο από | τιμή > 10000 |
| >= | Μεγαλύτερο ή ίσο | Χ + Υ >= (Α + Β) / Γ |
| < | Μικρότερο από | Β^2 - 4 * Α * Γ < 0 |
| <= | Μικρότερο ή ίσο | Βάρος <= 500 |

### Λογικοί τελεστές {#logigal-operators}

| Παράδειγμα | Αποτέλεσμα |
|---|---|
| ΟΧΙ 'Α' = 'Α' | ΨΕΥΔΗΣ |
| ΟΧΙ 1 < 0 | ΑΛΗΘΗΣ |
| 'Α' = 'Α' ΚΑΙ 1 < 0 | ΨΕΥΔΗΣ |
| 'Α' = 'Α' ΚΑΙ 1 > 0 | ΑΛΗΘΗΣ |
| 'Α' = 'Α' Ή 1 < 0 | ΑΛΗΘΗΣ |
| ΟΧΙ 'Α' = 'Α' Ή 1 > 0 ΚΑΙ 2 > 0 | ΑΛΗΘΗΣ |
| ΟΧΙ ('Α' = 'Α' Ή 1 > 0) ΚΑΙ 2 > 0 | ΨΕΥΔΗΣ |

### Εντολές επιλογής {#selection}

~~~
ΠΡΟΓΡΑΜΜΑ Ζυγός
  
ΜΕΤΑΒΛΗΤΕΣ
  ΑΚΕΡΑΙΕΣ: Αριθμός
  ΧΑΡΑΚΤΗΡΕΣ: Περιγραφή
  
ΑΡΧΗ 

  ΓΡΑΨΕ 'Δώσε έναν ακέραιο αριθμό'
  ΔΙΑΒΑΣΕ Αριθμός
  
  ΑΝ Αριθμός = 0 ΤΟΤΕ
    Περιγραφή <- 'μηδέν'
  ΑΛΛΙΩΣ_ΑΝ Αριθμός MOD 2 = 0 ΤΟΤΕ
  	Περιγραφή <- 'άρτιος'
  ΑΛΛΙΩΣ
  	Περιγραφή <- 'περιττός'
  ΤΕΛΟΣ_ΑΝ
  
  ΓΡΑΨΕ 'Ο ', Αριθμός, ' είναι ', Περιγραφή
  
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

~~~
ΠΡΟΓΡΑΜΜΑ Ζυγός
  
ΜΕΤΑΒΛΗΤΕΣ
  ΑΚΕΡΑΙΕΣ: Αριθμός
  ΧΑΡΑΚΤΗΡΕΣ: Περιγραφή
  
ΑΡΧΗ 

  ΓΡΑΨΕ 'Δώσε έναν ακέραιο αριθμό από το 0 έως το 9'
  ΔΙΑΒΑΣΕ Αριθμός
  
  ΕΠΙΛΕΞΕ αριθμός
	ΠΕΡΙΠΤΩΣΗ 0
		ΓΡΑΨΕ 'Μηδέν'
  	ΠΕΡΙΠΤΩΣΗ 1,3,5,7,9
		ΓΡΑΨΕ 'Μονός αριθμός'
  	ΠΕΡΙΠΤΩΣΗ 2,4,6,8
		ΓΡΑΨΕ 'Ζυγός'
	ΠΕΡΙΠΤΩΣΗ ΑΛΛΙΩΣ
		ΓΡΑΨΕ 'Αριθμός < 0 ή > 9 ή όχι ακέραιος'
  ΤΕΛΟΣ_ΕΠΙΛΟΓΩΝ
  
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

### Εντολές επανάληψης {#loops}

#### ΟΣΟ...ΕΠΑΝΑΛΑΒΕ

Σε αυτή, η συνθήκη που ελέγχει την επανάληψη βρίσκεται στην αρχή της επανάληψης και ο βρόχος επαναλαμβάνεται συνεχώς, όσο η συνθήκη αυτή ισχύει. Με τη δομή αυτή μπορούν να εκφραστούν όλες οι επαναλήψεις και γι’ αυτό η εντολή ΟΣΟ... ΕΠΑΝΑΛΑΒΕ είναι η σημαντικότερη από όλες τις εντολές επανάληψης.

~~~
ΠΡΟΓΡΑΜΜΑ ΆθροισμαΚαιΜέσοςΌρος

ΜΕΤΑΒΛΗΤΕΣ
  ΑΚΕΡΑΙΕΣ: Χ, Άθροισμα, Πλήθος
  ΠΡΑΓΜΑΤΙΚΕΣ: ΜΟ

ΑΡΧΗ

	Πλήθος <- 0
	Άθροισμα <- 0
	ΓΡΑΨΕ 'Δώσε Αριθμό'
	ΔΙΑΒΑΣΕ Χ
    
	ΟΣΟ Χ <> 0 ΕΠΑΝΑΛΑΒΕ
		Άθροισμα <- Άθροισμα + Χ
		Πλήθος <- Πλήθος + 1
  		ΓΡΑΨΕ 'Δώσε Αριθμό'
  		ΔΙΑΒΑΣΕ Χ
	ΤΕΛΟΣ_ΕΠΑΝΑΛΗΨΗΣ

	ΑΝ Πλήθος > 0 ΤΟΤΕ
		ΜΟ <- Άθροισμα / Πλήθος
		ΓΡΑΨΕ 'Το Άθροισμα είναι : ', Άθροισμα
		ΓΡΑΨΕ 'Ο Μέσος όρος είναι : ', ΜΟ
	ΑΛΛΙΩΣ
		ΓΡΑΨΕ 'Δεν δόθηκαν στοιχεία'
	ΤΕΛΟΣ_ΑΝ
    
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

> Δώσε Αριθμό
>
> 5
>
> Δώσε Αριθμό
>
> 10
>
> Δώσε Αριθμό
>
> 0
>
> Το Άθροισμα είναι : 15
>
> Ο Μέσος όρος είναι : 7.50

#### ΜΕΧΡΙΣ_ΟΤΟΥ

Σε αυτή οι εντολές του βρόχου εκτελούνται μέχρις ότου ικανοποιηθεί κάποια συνθήκη η οποία ελέγχεται στο τέλος της επανάληψης.

~~~
ΠΡΟΓΡΑΜΜΑ ΆθροισμαΚαιΜέσοςΌρος

ΜΕΤΑΒΛΗΤΕΣ
  ΑΚΕΡΑΙΕΣ: Χ, Άθροισμα, Πλήθος
  ΠΡΑΓΜΑΤΙΚΕΣ: ΜΟ

ΑΡΧΗ
	Χ <- 0
	Πλήθος <- 0
	Άθροισμα <- 0
    
	ΑΡΧΗ_ΕΠΑΝΑΛΗΨΗΣ
    	ΓΡΑΨΕ 'Δώσε Αριθμό'
  		ΔΙΑΒΑΣΕ Χ
		Άθροισμα <- Άθροισμα + Χ
		Πλήθος <- Πλήθος + 1
	ΜΕΧΡΙΣ_ΟΤΟΥ Χ = 0

	ΑΝ Άθροισμα > 0 ΤΟΤΕ
		ΜΟ <- Άθροισμα / (Πλήθος - 1)
		ΓΡΑΨΕ 'Το Άθροισμα είναι : ', Άθροισμα
		ΓΡΑΨΕ 'Ο Μέσος όρος είναι : ', ΜΟ
	ΑΛΛΙΩΣ
		ΓΡΑΨΕ 'Δεν δόθηκαν στοιχεία'
	ΤΕΛΟΣ_ΑΝ
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

> Δώσε Αριθμό
>
> 10
>
> Δώσε Αριθμό
>
> 20
>
> Δώσε Αριθμό
>
> 0
>
> Το Άθροισμα είναι : 30
>
> Ο Μέσος όρος είναι : 15.00

#### ΓΙΑ.. ΑΠΟ...ΜΕΧΡΙ

~~~
ΠΡΟΓΡΑΜΜΑ Περιττοί

ΜΕΤΑΒΛΗΤΕΣ
	ΑΚΕΡΑΙΕΣ:Άθροισμα, Αριθμός
    
ΑΡΧΗ
	Άθροισμα <- 0

	ΓΙΑ Αριθμός ΑΠΟ 1 ΜΕΧΡΙ 100 ΜΕ_ΒΗΜΑ 2
		Άθροισμα <- Άθροισμα + Αριθμός
	ΤΕΛΟΣ_ΕΠΑΝΑΛΗΨΗΣ
		ΓΡΑΨΕ 'Άθροισμα περιττών αριθμών είναι: ', Άθροισμα
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

> Το άθροισμα περιττών αριθμών είναι: 2500