# **InfoCinemas**

Πρόκειται για το πληροφοριακό σύστημα ενός κινηματογράφου μέσα απο το οποίο θα μπορούν να δράσου τόσο οι χρήστες όσο και οι διαχειριστές.
Συγκεκριμένα:

Οι **Διαχειριστές(admin)** έχουν την δυαντότητα να εκτέλεσουν τις παρακάτω λειτουργίες :

- Εισαγωγή νέας ταινίας (με την εισαγωγή των στοιχείων:Τίτλος, Έτος Κυκλοφορίας, Σύντομη Περιγραφή, Ημέρες και ώρες προβόλης).
- Διαγραφή ταινίας με βάση τον τίτλο της (Σε περίπτωση συνωνυμίας διαγράφεται η ταινία με την παλαιότητη χρονιά κυκλοφορίας).
- Ενημέρωση υπάρχουσας ταινίας
 - Ως προς τον **τίτλο**.
 - Ως προς το **έτος κυκλοφορίας**.
 - Ως προς την **περιγραφή** της.
 - Ως προς τις **ημέρες και ώρες προβολής** της.
- Δημιουργία ενός απλού χρήστη σε Διαχειριστή.

Οι **απλοί χρήστες(users)** έχουν την δυνατότηα να εκτελέσουν τις παρακάτω λειτουργίες:

- Αναζήτηση ταινίας.
- Εμφάνιση πληροφοριών ταινίας (τίτλος ,έτος κυκλοφορίας ,σύντομη περιγραφή ,ημέρες και ώρες προβολής).
- Αγορά εισητηρίου για προβολή ταινίας.
- Εμφάνση ιστορικού των ταινιών που έχει δεί.

Για να εκτελέσουμε τις παραπάνω λειτουργίες χρειαζόμαστε δυο βάσεις , μια για να αποθηκέυουμε τις ταινίες, Movies 
και μία για τους χρήστες(απλοί και διαχειριστές) Users.

**Movies**:

- title
- year
- description
- screening[]

**Users**:

- name
- e-mail
- password
- movies_seen[]
- category

## Λειτουργία 

Αρχικά εμφανίζεται στον επισκέπτη μια σελίδα στην οποία καλείται να επιλέξει ανάμεση στην εγγραφή(register) και την εισαγωγή(login).
 
Για να γίνει η εισαγωγή του στο σύστημα πρέπει πρώτα να εγγραφεί.

Ο πρώτος χρήστης που κάνει εγγραφή ανήκει στην κατηγορία Admin-Διαχειριστής.

Στον χρήστη που ανοίκει στην κατηγορία admin, υπάρχει ένα βασικό menu πλοήγης το οποίο επιτρέπει την εκτέλεση των διαιωμάτων που προαναφέρθηκαν προηγουμένως.
Σαν πρώτη εικόνα δέχεται ενα μήνυμα καλωσορίσματος:
#
### Insert New Movie 

Επλέγουμε να εισάγουμε μια ταινία με την συμπλήρωση των στοιχείων title(τίτλος) , year of release(έτος κυκλοφορίας) , description(περιγραφή) , screening datetimes(ημερομηνίες και ώρες προβολής). 

Σε περίπτωση που θέλουμε να προσθέσουμε παραπάνω ημερομηνίες και ώρες προβολής πατάμε το κουμπί "add extra hours/day " και αφού τελειώσουμε με τις επιλογές της εισαγωγής επιλέγουμε το submit.





