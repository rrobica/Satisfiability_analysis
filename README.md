# Studiu experimental asupra metodelor de rezolvare a problemei SAT

Acest proiect conține implementarea a trei algoritmi clasici pentru rezolvarea problemei satisfiabilității propoziționale (SAT): **Rezoluție**, **Davis–Putnam** și **DPLL**, precum și un sistem de testare automată pe formule generate și benchmark-uri din SATLIB.

## 📌 Conținut

- `CNF read.py` — cod pentru citirea fișierelor `.cnf` în format DIMACS;
- `Memory fix.py` — cod principal pentru rularea experimentelor și logarea rezultatelor în `.csv`;
- `sat_results_comparison_all.csv` — rezultate experimentale pe toate fișierele testate;
- `Analiza date satisfiabilitate.xlsx` — analiză vizuală (Excel) cu grafice comparative;
- `Articol Satisfiabilitate.pdf` — lucrarea științifică redactată în LaTeX, cu grafice și interpretări;

## 🧩 Exemplu abordat: Sudoku 4x4

Proiectul conține un exemplu complet în care un joc Sudoku 4x4 este transformat într-o formulă SAT în CNF, utilizat ca exemplu de referință (`running example`) în testarea și explicarea fiecărui algoritm.

## 🧪 Descriere experiment

- Formule CNF au fost testate din două surse:
  - Generare aleatorie (cu controlul numărului de clauze și variabile);
  - Fișiere reale din benchmark-ul [SATLIB](https://www.cs.ubc.ca/~hoos/SATLIB/);
- S-au măsurat:
  - Timpul de execuție;
  - Memoria folosită;
  - Rezultatul SAT / NOT SAT / TIMEOUT;
- Datele au fost exportate în `.csv` și analizate cu Excel + grafice.

## 📈 Rezultate

- DPLL este cel mai eficient dintre cei trei algoritmi testați.
- Rezoluția este completă dar ineficientă pe instanțe reale.
- Sudoku 4x4 a fost satisfiabil și a servit drept exemplu central în lucrare.
- Timeout-urile în Rezoluție au fost tratate ca `NOT SAT`.

## 📚 Bibliografie

Vezi secțiunea bibliografică din `main.tex`. Au fost folosite surse academice relevante, inclusiv:
- Handbook of Satisfiability
- GRASP, CDCL, VSIDS
- Tranziția de fază în SAT
- Sudoku to SAT encodings

## 📎 Licență

Proiect realizat ca parte a disciplinei *Metode și practici în informatică* — 2025.

---

## 🔗 Linkuri utile

- Lucrarea completă în LaTeX: [`main.tex`](main.tex)
- Vizualizare rezultate în Excel: [`Analiza date satisfiabilitate.xlsx`](Analiza%20date%20satisfiabilitate.xlsx)
- SATLIB Benchmark: https://www.cs.ubc.ca/~hoos/SATLIB/

