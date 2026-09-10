# Reanalysis of published dopaminergic vesicle proteomes

Code accompanying Fujise et al., *Journal of Cell Biology*.

This repository reproduces the proteomics panels of Figure 6, which ask whether
proteins identified in the synaptic vesicle reconstitution system are also
found on dopamine vesicles in native tissue. A fixed panel of vesicle proteins
is extracted from three published proteomic datasets and plotted as heatmaps.

No statistical tests are recomputed here. Effect sizes and significance values
are taken as published by the original authors; this code only selects, aligns
and plots them.



## Panels

|Panel|Dataset|Comparison|Statistic as published|
|-|-|-|-|
|a|Hobson et al. 2022, *eLife*|APEX2⁺ striatum vs bulk striatum|log2FC, BH-adjusted q|
|b|Paget-Blanc et al. 2022, *Nat Commun*|DA-FASS synaptosomes vs bulk synaptosomes|abundance ratio, BH-adjusted p|
|c|Asmerian et al. 2026, *Sci Adv*|VGLUT2⁺ vs VMAT2⁺ vesicles (striatal LP2 and P4)|mean log2 ratio, uncorrected two-tailed p|



## Source data

`source_data\figure5.csv` contains every value plotted in the figure, one row
per protein per comparison, with the dataset and the statistic type recorded
explicitly.



See data/README.md for the four required input files and their DOIs



## Running

```bash
pip install -r requirements.txt
jupyter notebook proteomics_reanalysis.ipynb
```

By default the notebook reads from `./data`. To point it elsewhere:

```bash
DATA_DIR=/path/to/files jupyter notebook proteomics_reanalysis.ipynb
```

## Outputs

Written to `figures/`:

* `panel_a_hobson.pdf` / `.png`
* `panel_b_pagetblanc.pdf` / `.png`
* `panel_c_asmerian.pdf` / `.png`
* `source_data_figure5.csv`

## 

## Citation

If you use this code, please cite the manuscript and the three original
datasets.



## 

