To replicate the data found in "Population genetics of transposable element load: a mechanistic account of observed overdispersion", Smith et al.

For Drosophila data:
- Unzip the TEPopGen.zip
- All relevant source files, code, and output contained in the Drosophila folder
- You only need to run the MakeTESummaries_Dros.ipynb notebook


For Mimulus data:
- Unzip the TEPopGen.zip
- Within the 'Mimulus' folder:
  - All relevant data, code, and output contained in this folder
  - First run 'A_DoAnalysis.m' in MATLAB
  - Then run 'Output4Python.m' - this will output the relevant files to run:
  - MakeTESummaries_Mim.ipynb

The author of this code, RD Smith, apologizes that part of the data processing is in MATLAB and the other part is in Python.  This project has been in the works for some time, during which, said author switched preferences.

Please contact rdsmith@wm.edu with any questions related to this code. 

---
Below is a more detailed description of the files in each folder:

- Mimulus
  - CurrentData_v3.csv: The raw count data used to estimate TE abundances.  The samples (plant IDs) are along the columns, the features (genes and TEs) are along the rows.
  - EstNum.csv: A file containing only numerical data - these are the estimated copy numbers for Genes and TEs (features are along the columns, samples are along the rows)
  - idxTE.csv: A list of boolean values indicating which rows in EstNum.csv are TEs
  - Names.txt: The row lables for EstNum.csv (Gene / TE names)
  - PlantNames.txt: The column labels for EstNum.csv (individial plant IDs)
  - TENameMap.csv: A list of TE family names, and which type of TE they are ("type" is one of: DNA, LTR, LINE, SINE. "paste" is one of: DNA, RNA)
  - MGut_TE_SummmaryByVVV.csv (where VVV is one of: Element, Family, Type, Paste).  These are the final output tables from MakeTESummaries_Mim.ipynb which are used throughout the manuscript.

- Drosophila
  - Supp_table5.tsv: Supplement S5 from: Cridland, Julie M., et al. "Abundance and distribution of transposable elements in two Drosophila QTL mapping resources." Molecular biology and evolution 30.10 (2013): 2311-2327.  DOI: http://dx.doi.org/10.1093/molbev/mst129
  - TENameMap.csv: TE names from the above file, parsed into "type", "family", "name" (least specific to most specific)
  - DMel_TE_SummaryByVVV.csv (where VVV is one of: Type, Family, Name).  These are the final output tables from MakeTESummaries.ipynb which are used throughout the manuscript.
