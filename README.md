# ALICE nuclear modification factor masterclass

Honours project, University of Cape Town / iThemba LABS (2026).
Aadam Abdullah, supervised by Assoc. Prof. Zinhle Buthelezi, Dr Bharati Naik and Dr Siegfried Fortsch.

The project measures the nuclear modification factor $R_{AA}$ and the central-to-peripheral ratio $R_{CP}$ of charged particles in Pb–Pb collisions at $\sqrt{s_{NN}}$ = 2.76 TeV (ALICE, LHC10h) for use in a masterclass. As an extension, it reconstructs the J/ψ in pp and p–Pb data from the ALICE J/ψ masterclass.

It has two parts:

| | What it is | How to use it |
|---|---|---|
| **Browser tool** | A single web page that takes high-school learners through the analysis step by step | Open **https://aadam-a.github.io/alice-raa-masterclass/**, or download `index.html` and open it in any browser (works offline) |
| **Jupyter notebook** | The full analysis: centrality classes, $p_T$ spectra, $R_{AA}$, $R_{CP}$, comparison with ALICE, uncertainties, J/ψ | `ALICE_RAA_Masterclass.ipynb`, see below |

## Running the notebook

1. Install Python 3.10 or newer, then the packages:
   ```
   pip install -r requirements.txt
   ```
2. Download the two data sets that are too large for this repository and put them next to the notebook:
   - **`track_info.pkl`** (Pb–Pb tracks, 139 MB): from the [Releases page](https://github.com/aadam-a/alice-raa-masterclass/releases) of this repository.
   - **`JpsiMasterclass/`** (J/ψ events, needed for Part C only): clone the J/ψ masterclass into this folder:
     ```
     git clone https://github.com/zwound40/JpsiMasterclass.git
     ```
3. Start Jupyter and run all cells:
   ```
   jupyter notebook ALICE_RAA_Masterclass.ipynb
   ```
   The plots are saved in `figures/`.

The folder should then look like this:
```
alice-raa-masterclass/
├── ALICE_RAA_Masterclass.ipynb
├── ALICE_RAA_Tools.py
├── event_information.csv
├── pp_reference.dat
├── PP_2760GeV_BaseLine.root
├── track_info.pkl              <- downloaded
├── JpsiMasterclass/            <- cloned
└── index.html             <- the browser tool
```

## Data and credits

- Pb–Pb events and tracks, and the pp reference spectrum: the ALICE $R_{AA}$ masterclass, https://github.com/dmuhlhei/ALICE_MC_RAA
- J/ψ events and the original analysis program (`masterclass.C`): the ALICE J/ψ masterclass, https://github.com/zwound40/JpsiMasterclass
- $\langle N_{coll}\rangle$ uncertainties: ALICE, Phys. Rev. C 88 (2013) 044909
- Published $R_{AA}$ used for comparison: ALICE, Phys. Lett. B 720 (2013) 52

The data were recorded by the ALICE Collaboration at CERN. The masterclass samples are preselected and not corrected for detector efficiency, so the results illustrate the method and do not replace ALICE's publications.
