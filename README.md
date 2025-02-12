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

 ![](screenshot/1.png)
 
Για να γίνει η εισαγωγή του στο σύστημα πρέπει πρώτα να εγγραφεί.

![](screenshot/2.png)

![](screenshot/3.png)

Ο πρώτος χρήστης που κάνει εγγραφή ανήκει στην κατηγορία Admin-Διαχειριστής.

Στον χρήστη που ανοίκει στην κατηγορία admin, υπάρχει ένα βασικό menu πλοήγης το οποίο επιτρέπει την εκτέλεση των διαιωμάτων που προαναφέρθηκαν προηγουμένως.
Σαν πρώτη εικόνα δέχεται ενα μήνυμα καλωσορίσματος:

![](screenshot/4.png)

## 1. Λειτουργία Διαχειριστή

### Insert New Movie 

Επλέγουμε να εισάγουμε μια ταινία με την συμπλήρωση των στοιχείων title(τίτλος) , year of release(έτος κυκλοφορίας) , description(περιγραφή) , screening datetimes(ημερομηνίες και ώρες προβολής). 

![](screenshot/5.png)

Σε περίπτωση που θέλουμε να προσθέσουμε παραπάνω ημερομηνίες και ώρες προβολής πατάμε το κουμπί "add extra hours/day " και αφού τελειώσουμε με τις επιλογές της εισαγωγής επιλέγουμε το submit.

Eαν πρόκειται για εισαγωγή μιας ταινίας με μοναδικό τίτλο και έτος κυκλοφορίας, εμφανίζεται στην οθόνη του επισκέπτη το μήνυμα:

** **This movie has been succesfully inserted!!**

Εαν εισάγει μια ταινία που υπάρχει με τον ίδιο τίτλο και έτος κυκλοφορίας, εμφανίζεται στην θόνη του επισκέπτη το μήνυμα:

** **This movie already exists! Try Again!**

## Delete a Movie

Πληκτρολογούμε τη ταινία που θέλουμε να διαγράψουμε. 

![](screenshot/6.png)

Σε περίπτωση που η ταινία υπάρχει και γίνεται μοναδική , εμφανίζεται το μήνυμα:

** **The Movie has been succesfully deleted!!**

(Εαν υπάρχουν πολλαπλές ταινίες με το ίδιο όνομα , διαγράφεται αυτή με το παλαιότερο έτος κυκλοφορίας και εμφανίζεται το ίδιο μήνυμα)

Εαν δεν υπάρχει τέτοια ταινία εμφανίζεται το μήνυμα :

** **There is no such movie.Try again!!**

## Update a Movie

![](screenshot/7.png)

Για να ανανεώσουμε κάποιο πεδίο μιας ταινίας εισάγουμε τα μοναδικά στοιχεία της ταινίας και επιλέγουμε το πεδίο  που θέλουμε να ανανεώσουμε:

- Title(τίτλος)

![](screenshot/8.png)

Σε επιτυχή ανανέωση τίτλου εμφανίζεται το μήνυμα: ** **Movie Title has been succesfully updated.**

- Year(έτος κυκλοφορίας)

![](screenshot/00.png)

Σε επιτυχή ανανέωση έτους κυκλοφορίας εμφανίζεται το μήνυμα: ** **Movie Year has been succesfully updated.**

- Description(περιγραφή)

![](screenshot/10.png)

Σε επιτυχή ανανέωση της περιγραφής εμφανίζεται το μήνυμα: ** **Movie Description has been succesfully updated.**

- Screening Datetime(ημερομηνίες και ώρες προβολής)

Στην συγκεκριμένη επιλογή, εμφανίζεται στν διαχειριστή το παρακάτω μενού , αφού τον έχει εισάγει σε ενα περιβάλλον καλωσορίσματος .

![](screenshot/11.png)

### Add New Screening Datetime

![](screenshot/12.png)

Σε επιτυχή ανανέωση της λίστας με τις ημερομηνίες και τις ώρες προβολής εμφανίζεται το μήνυμα: 

** **Your screening datetime has been added.**

### Delete a movie screening datetime 

![](screenshot/13.png)

Επιλέγουμε την προβολή που θέλουμε , και την διαγράφουμε


### Update a Screening Datetime 

![](screenshot/14.png)

Επιλέγουμε απο το μενού την προβολή που θέλουμε να τροποποιήσουμε και γράφουμε -ακολουθώντας **AΥΣΤΗΡΑ** τους σχετικούς κανόνες-  την νεα ημερομηνία και ώρα προβολής.

Σε επιτυχή ανανέωση της προβολής εμφανίζεται το μήνυμα: 

** **Your Screening datetime has been succesfully updated.**

## Add admin 

![](screenshot/15.png)

 Ψάχνουμε κάποιον χρήστη με βάση το email του .
 
 Σε επιτυχή ανανέωση του χρήστη εμφανίζεται το μήνυμα:
 
 ** **The user with the e-mail {} has been upgrated as an Administrator!!**

## Log out
 Πάντα φυσικά υπάρχει και η επιλογή του Log out , το οποίο μας επιστρέφει στην αρχική σελίδα Login-Register

## Λειτουργία απλού Χρήστη

Η πλοήγηση του χρήστη γίνεται επίσης με βάση ένα μενού επιλογών.

![](screenshot/16.png)

### Search Movie 

Πληκτρολογούμε την ταινία που μας ενδιαφέρει και πατάμε κλίκ σε αυτήν για περισσότερες πληροφορίες .

![](screenshot/17.png)

Σε περίτωση που δεν υπάρχει κάποια ταινία με αυτό το όνομα εμφανίζεται το παρακάτω μήνυμα:

** **There is no {} Movie in the System**

Διαλέγουμε προβολή και τον αριθμό των θέσεων που θέλουμε να κάνουμε κράτηση.

![](screenshot/18.png)

Σε περίπτωση επιτυχούς κράτησης εμφανίζεται το ο παρακάτω μήνυμα

** **Your ticket reservation is complete**



## View History
Για την προβολή των ταινιών που έχει παρακολουθήσει κάποιος χρήστης 

# Εγκατάσταση και εκτέλεση εργασίας 

1) Κατέβασμα εφαρμογής 

Επιλέγονται το Download zip  στην επιλογή Clone μπορείτε να κατεβάσετε ολόκληρο το Repository, το οποίο περιέχει εναν φάκελο με το όνομα InfoCinemas και αυτό το αρχείο README.

2) Εγκατάσταση Docker 

Για την εγκατάσταση του Docker (εαν δεν το έχετε ήδη εγκατεστημένο)  ακολουθήστε τις παρακάτω εντολές στο Terminal του υπολογιστή σας:
sudo apt-get update

sudo apt install -y apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - 

sudo add-apt-repository -y "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt-get update6.sudo apt install docker-ce

3) Εγκατάσταση του Docker Compose 

sudo apt install -y docker-compose

Αφού έχετε εγκαταστήσει επιτυχώς τα παραπάνω, συνεχίζεται με την εκτέλεσή του:

1) Κάνετε extract το zip φάκελο που κατεβάσατε 
2) Στο terminal γράφουμε : 

sudo docker-compose up -d 

Όταν ολοκληρωθεί επιτυχώς η διαδικασία, άνοιγεται ΑΥΣΤΗΡΑ τον browser  Chrome και πληκτρολογώντας localhost:9000 μπορείτε πλέον να χρησιμοποιήσετε την εφαρμογή . 








