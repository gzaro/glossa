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
- [Πίνακες](#arrays)

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
ΠΡΟΓΡΑΜΜΑ ΠεριττοίME

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

#### Ασκήσεις

* Γράψε ένα πρόγραμμα σε γλώσσα, το οποίο εμφανίζει την προπαίδεια:

~~~
1 X 1 = 1
1 X 2 = 2
1 X 3 = 3
1 X 4 = 4
1 X 5 = 5
1 X 6 = 6
1 X 7 = 7
1 X 8 = 8
1 X 9 = 9
1 X 10 = 10

2 X 1 = 2
2 X 2 = 4

...

10 X 9 = 90
10 X 10 = 100
~~~

* Γράψε ένα πρόγραμμα σε γλώσσα, το οποίο δέχεται έναν ακέραιο αριθμό από το πληκτρολόγιο και τον εμφανίζει σε δυαδική μορφή (κάθετα)

* Γράψε ένα πρόγραμμα σε γλώσσα, το οποίο δέχεται έναν ακέραιο αριθμό σε δυαδική μορφή από το πληκτρολόγιο και τον εμφανίζει σε δεκαδική μορφή

* Γράψε ένα πρόγραμμα σε γλώσσα, το οποίο δέχεται έναν ακέραιο αριθμό από το πληκτρολόγιο και ελέγχει αν είναι παλίνδρομος. Δηλαδή αν διαβάζεται το ίδιο και από τις 2 κατευθύνσεις π.χ. 1, 232, 1221.

### Πίνακες {#arrays}

Ο πίνακας είναι μία ομάδα μεταβλητών ιδίου τύπου που αναφέρονται με ένα κοινό όνομα και αποθηκεύονται σε διαδοχικές θέσεις στη μνήμη. Για την πρόσβαση σε ένα ατομικό στοιχείο του πίνακα πρέπει να γραφεί το όνομα του πίνακα ακολουθούμενο από ένα δείκτη (μεταβλητή ή σταθερά). Οι πίνακες μπορεί να είναι μονοδιάστατοι, δισδιάστατοι ή γενικότερα πολυδιάστατοι. Ο αριθμός των δεικτών καθορίζει τη διάσταση του πίνακα. Η επεξεργασία πινάκων γίνεται συνήθως με τη χρήση εντολών ΓΙΑ.

Οι τυπικές επεξεργασίες που γίνονται σε πίνακες περιλαμβάνουν την αναζήτηση, την ταξινόμηση και τη συγχώνευση πινάκων. Για αυτές τις επεξεργασίες έχουν αναπτυχθεί αρκετοί αλγόριθμοι και η μελέτη τους αποτελεί έναν από τους σημαντικούς τομείς της αλγοριθμικής.

~~~
ΠΡΟΓΡΑΜΜΑ ΆθροισμαΠίνακα

ΜΕΤΑΒΛΗΤΕΣ
	ΑΚΕΡΑΙΕΣ:i, αριθμοί[100], άθροισμα
 
ΑΡΧΗ

	ΓΙΑ i ΑΠΟ 1 ΜΕΧΡΙ 100
    	αριθμοί[i] <- i
    ΤΕΛΟΣ_ΕΠΑΝΑΛΗΨΗΣ
    
    άθροισμα <- 0
    ΓΙΑ i ΑΠΟ 1 ΜΕΧΡΙ 100
    	άθροισμα <- άθροισμα + αριθμοί[i]
    ΤΕΛΟΣ_ΕΠΑΝΑΛΗΨΗΣ
    
	ΓΡΑΨΕ '1 + 2 + 3 ... + 98 + 99 + 100 = ', άθροισμα
    
       
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

> 1 + 2 + 3 ... + 98 + 99 + 100 = 5050

#### Ασκήσεις

* Γράψε ένα πρόγραμμα που αποθηκεύει 10 αριθμούς που δέχεται από το πληκτρολόγιο, υπολόγισε τον μέσο όρο και εμφάνισε τους αριθμούς που είναι μικρότεροι από τον μέσο όρο.

* Γράψε ένα πρόγραμμα που αποθηκεύει 10 αριθμούς που δέχεται από το πληκτρολόγιο, του αποθηκεύει σε έναν πίνακα, τον ταξινομεί με αύξουσα σειρά και τον εμφανίζει ταξινομημένο.

* Γράψε ένα πρόγραμμα που συγχωνεύει δύο ταξινομημένους πίνακες σε έναν τρίτο (ταξινομημένο).

~~~
ΠΡΟΓΡΑΜΜΑ ΣυγχώνευσηΠινάκων

ΜΕΤΑΒΛΗΤΕΣ
	ΠΡΑΓΜΑΤΙΚΕΣ: πίνακας1[10], πίνακας2[10], πίνακας3[20]
	ΑΚΕΡΑΙΕΣ: i
 
ΑΡΧΗ

	πίνακας1[1] <- 3
	πίνακας1[2] <- 3.2
	πίνακας1[3] <- 4.8
	πίνακας1[4] <- 6.1
	πίνακας1[5] <- 6.3
	πίνακας1[6] <- 6.9
	πίνακας1[7] <- 7.2
	πίνακας1[8] <- 7.51
	πίνακας1[9] <- 8.1
	πίνακας1[10] <- 8.3
    
  πίνακας2[1] <- 4
	πίνακας2[2] <- 4.1
	πίνακας2[3] <- 4.7
	πίνακας2[4] <- 4.8
	πίνακας2[5] <- 6.2
	πίνακας2[6] <- 6.5
	πίνακας2[7] <- 7.1
	πίνακας2[8] <- 7.12
	πίνακας2[9] <- 7.5
	πίνακας2[10] <- 7.9

	ΓΙΑ i ΑΠΟ 1 ΜΕΧΡΙ 20
    ΓΡΑΨΕ πίνακας3[i]
  ΤΕΛΟΣ_ΕΠΑΝΑΛΗΨΗΣ
    
ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
~~~

* Γράψε ένα πρόγραμμα που εμφανίζει όλες τις τριψήφιες λέξεις που μπορούν να δημιουργηθούν από τα γράμματα Α, Β, Γ. Δηλαδή να εμφανίζει:

~~~
ΑΑΑ
ΑΑΒ
ΑΑΓ
ΑΒΑ
ΑΒΒ
ΑΒΓ
ΑΓΑ
ΑΓΒ
ΑΓΑ
ΒΑΑ
ΒΑΒ
ΒΑΓ
ΒΒΑ
ΒΒΒ
ΒΒΓ
ΒΓΑ
ΒΓΒ
ΒΓΓ
ΓΑΑ
ΓΑΒ
ΓΑΓ
ΓΒΑ
ΓΒΒ
ΓΒΓ
ΓΓΑ
ΓΓΒ
ΓΓΓ
~~~

### Υποπρογράμματα

#### Ασκήσεις

* Γράψε ένα πρόγραμμα που δέχεται δύο ακεραίους n και k και υπολογίζει τον [διωνυμικό συντελεστή](https://el.wikipedia.org/wiki/%CE%94%CE%B9%CF%89%CE%BD%CF%85%CE%BC%CE%B9%CE%BA%CF%8C%CF%82_%CF%83%CF%85%CE%BD%CF%84%CE%B5%CE%BB%CE%B5%CF%83%CF%84%CE%AE%CF%82) n! / (k! * (n - k)!)