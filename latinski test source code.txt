import random

GREEN = "\033[92m"
RED = "\033[91m"
BLUE = "\033[94m"
YELLOW = "\033[93m"
PURPLE = "\033[95m"
RESET = "\033[0m"



print("=====Latinski kviz=====")

reci_latinski = {
    # I. Imperija
    "Danubius": ("dunav", "Dunav"),
    "fluvius": ("reka", "Reka"),
    "magnus": ("velik", "Velik"),
    "Rhenus": ("rajna", "Rajna"),
    "quoque": ("takođe", "Takođe"),
    "Tiberis": ("tibar", "Tibar"),
    "sed": ("ali", "Ali"),
    "parvus": ("mali", "Mali"),
    "ubi": ("gde", "Gde"),
    "insula": ("ostrvo", "Ostrvo"),
    "Creta": ("krit", "Krit"),
    "Graeci": ("grci", "Grci"),
    "multas insulas": ("mnoga ostrva", "Mnoga ostrva"),
    "habent": ("imaju", "Imaju"),
    "amant": ("vole", "Vole"),
    "populus Romanus": ("rimski narod", "Rimski narod"),
    "imperium": ("imperija", "Imperija"),
    "terra": ("zemlja", "Zemlja"),
    "Illyricum": ("ilirik", "Ilirik"),
    "Romani": ("rimljani", "Rimljani"),
    "tenent": ("drze", "Drze"),
    "habitant": ("zive", "Zive"),
    "prope": ("blizu", "Blizu"),
    "Graecia": ("grcka", "Grcka"),
    "oppidum": ("grad", "Grad"),
    "Moesia": ("mezija", "Mezija"),
    "Naissus": ("nis", "Nis"),
    "patria": ("otadzbina", "Otadzbina"),

    # II. Apud grammaticum
    "grammaticus": ("ucitelj", "Ucitelj"),
    "Lanuvium": ("lanuvij", "Lanuvij"),
    "habeo habere": ("imam", "Imam"),
    "forum": ("forum", "Forum", "trg", "Trg"),
    "ibi": ("tamo", "Tamo"),
    "discipulos": ("ucenike", "Ucenike"),
    "discipula -ae f": ("ucenica", "Ucenica"),
    "doceo docere": ("poducavati", "Poducavati"),
    "puer": ("decak", "Decak"),
    "puella -ae f": ("devojcica", "Devojcica"),
    "cotidie": ("svakog dana", "Svakog dana"),
    "apud": ("kod", "Kod"),
    "rotunda": ("okruglo", "Okruglo"),
    "plena": ("puna", "Puna"),
    "aqua -ae f": ("voda", "Voda"),
    "ad": ("za", "Za"),
    "vita -ae f": ("zivot", "Zivot"),
    "itaque": ("stoga", "Stoga"),
    "semper": ("uvek", "Uvek"),
    "iucunda": ("prijatna", "Prijatna"),
    "tum": ("tada", "Tada"),
    "interrogat": ("pita", "Pita"),
    "timeo timere": ("plasiti se", "Plasiti se"),
    "-ne?": ("li?", "Li?"),
    "ait": ("kaze", "Kaze"),
    "tu": ("ti", "Ti"),
    "bene": ("dobro", "Dobro"),
    "respondeo respondere": ("odgovoriti", "Odgovoriti"),
    "bona": ("dobra", "Dobra"),
    "cum": ("sa", "Sa"),
    "ambulo": ("hodam", "Hodam"),
    "nam": ("naime", "Naime"),
    "mihi": ("meni", "Meni", "mi", "Mi"),
    "placeo placere": ("svidjati se", "Svidjati se"),
    "umbra -ae f": ("hladovina", "Hladovina", "senka", "Senka"),
    "post": ("posle", "Posle"),
    "copia -ae f": ("obilje", "Obilje"),
    "variarum": ("raznih", "Raznih"),
    "de": ("o", "O"),
    "satis": ("dosta", "Dosta"),
    "nunc": ("sad", "Sad"),
    "quando?": ("kada?", "Kada?"),
    "caelum": ("nebo", "Nebo"),
    "video videre": ("videti", "Videti"),
    "noctu": ("nocu", "Nocu"),
    "luceo lucere": ("sijati", "Sijati"),
    "stella -ae f": ("zvezda", "Zvezda"),
    "pulchra": ("lepa", "Lepa"),
    "autem": ("pak", "Pak"),
    "cur?": ("zasto?", "Zasto?"),
    "aliquando": ("nekad", "Nekad"),
    "taceo tacere": ("cutati", "Cutati"),
    "obscurat": ("pomraci", "Pomraci"),
    "nec": ("ni", "Ni"),
    "verbum": ("rec", "Rec"),
    "fabula -ae f": ("prica", "Prica"),
    "saepe": ("cesto", "Cesto"),
    "rideo ridere": ("smejati se", "Smejati se"),
    "male": ("lose", "Lose"),
"forma -ae f": ("oblik", "Oblik"),
"bestia -ae f": ("zivotinja", "Zivotinja"),
"herba -ae f": ("biljka", "Biljka"),
"pluvia -ae f": ("kisa", "Kisa"),
"silva -ae f": ("suma", "Suma"),
"bibliotheca -ae f": ("biblioteka", "Biblioteka"),
"fabula -ae f": ("prica", "Prica"),
"provincia -ae f": ("provincija", "Provincija")

}


score = 0
tacan = 0

#rec = random.choice(list(reci_latinski.keys()))

#correct_anwser = reci_latinski[rec]

#input("Sta znaci ova rec? " + rec + " ")

while score < 10:
    rec = random.choice(list(reci_latinski.keys()))

    print(BLUE + "Prevedi: ", rec + RESET)
    answer = input(PURPLE + "Rec je: " + RESET).strip().lower()
    correct_answer = reci_latinski[rec]

    if answer in [x.lower() for x in correct_answer]:
        print("Tacno!")
        score += 1
        tacan += 1
    else:
        print(RED + "Netacno!" + RESET)
        print(YELLOW + "Tacan odgovor je bio: ", correct_answer[0] + RESET)
        score += 1




print(YELLOW + "Bravo, zavrsio si kviz sa:", tacan, "/10 poena!" + RESET)




















