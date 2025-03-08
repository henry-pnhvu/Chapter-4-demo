# **SANS and USANS Data Analysis Scripts**

This repository contains Python scripts demonstrating the procedures detailed in Sections **4.1** and **4.2** of Chapter 4—**Improvement of (U)SANS Data Analysis**—from the PhD thesis:

**"Nano-Scale Sorption of Methane and Water in Aerogels as Analogues of Geological Porous Media: Contrast-Matching SANS Experiments and Advanced Data Analysis"**  
by *Phung Nhu Hao Vu*.

## **Requirements**
- The scripts are written in Python and require a Python interpreter.
- They were developed and tested on **Spyder for Windows**, which can be downloaded [here](https://github.com/spyder-ide/spyder/releases).

## **Running the Scripts**

Download the appropriate ZIP file corresponding to each thesis chapter:

### **4.1 Combining SANS Quokka Report Files**
- The script **`combine_Quokka_report.py`** (Section 4.1) is located in the `Combine Report Script` folder within:  
  **`4.1 - Combining Quokka Report Files.zip`**
- The individual report files are stored in the `Quokka Report Files` folder.
- Running `combine_Quokka_report.py` generates a combined report file:  
  **`Combined_Quokka_Report.xml`** (saved in `Combine Report Script`).

---

### 4.2 Join and Bin SAS Data
The ZIP file `4.2 - Join and Bin SAS data.zip` contains the following folders:
- **01. Quokka SANS Outputs** – ASCII files output from Quokka for a set of CM SANS experiments under different uniaxial stress values.
- **02. Kookaburra USANS Outputs – Desmeared** – Corresponding Kookaburra data.
- **03. Analysed Result** – Processed data and analysis results.
- **04. Python Analysis Scripts** – Scripts for combining and binning SAS data:

#### (i) `aa_get_raw_data.py` – Extracting and Structuring Data
- Corresponds to *"Rewriting and Rearranging the Untrimmed, Unaligned SANS Segments"* in the thesis.
- Extracts, groups, and rewrites SANS and USANS segments into a uniform format.
- Outputs:
  - Rewritten files → `03. Analysed Result/01. Data Unanalysed`
  - Plots of segmented SAS data → `03. Analysed Result/aa. Figures Raw Data`

#### (ii) `bb_join_SAS_data.py` – Aligning Data
- Corresponds to *"Alignment Procedure"* in the thesis.
- Reads data from `03. Analysed Result/01. Data Unanalysed` and aligns them.
- Outputs:
  - Aligned and combined SAS data → `03. Analysed Result/02. Data Joined`
  - Alignment factor (written in headers of data files in `03. Analysed Result/01. Data Unanalysed`)
  - Aligned data plots → `03. Analysed Result/bb. Figures Aligned Data`

#### (iii) `cc_bin_SAS_data.py` – Binning Data
- Corresponds to *"Binning (U)SANS Data"* in the thesis.
- Reads data from `03. Analysed Result/02. Data Joined` and reduces point density, spacing them evenly in logQ space.
- Outputs:
  - Binned data → `03. Analysed Result/02. Data Binned`
  - Comparison plots (binned vs. combined data) → `03. Analysed Result/cc. Figure Combined Data vs. Binned Data`
- Reads data from `03. Analysed Result/02. Data Joined` and reduces point density, spacing them evenly in logQ space.
- **Outputs:**
  - Binned data → `03. Analysed Result/02. Data Binned`
  - Comparison plots (binned vs. combined data) → `03. Analysed Result/cc. Figure Combined Data vs. Binned Data`
