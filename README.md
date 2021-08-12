# Escherichia-coli-k12-Genome-Analysis

# Download and install anaconda(version 3 recommended)

### Add channels

```
conda config --add channels conda-forge

conda config --add channels bioconda

conda config --add channels daler

conda config --add channels defaults
```

### Download the Analysis pipeline

```
git clone https://github.com/deyar4/Escherichia-coli-k12-Genome-Analysis.git
```

### Change directory to the dowloaded folder

```
cd Escherichia-coli-k12-Genome-Analysis
```

### Create conda environment.Packages are listed in the environment.yaml file. 

```
conda env create -f environment.yaml
```

### Download the polishing tool pilon

```
mkdir apps

wget https://github.com/broadinstitute/pilon/releases/download/v1.23/pilon-1.23.jar -O apps/pilon.jar
```

### Activate the analysis environment
```
source activate Escherichia-coli-k12-Genome-Analysis
```

### Add permission to all scripts
```
chmod +x *.{py,sh,pl}
```

### Install python packages using pip
```
pip install -r pip-requirements.txt
```

### Step 1: Download data. 
```
https://www.ebi.ac.uk/ena/browser/view/ERX008638?show=reads
```

### Step 2: Perform QC on the raw reads
```
./qc_raw_reads.sh
```
### Step 3: Trim reads using sickle
```
./trim_reads.sh
```
### Step 4: Perform QC on the trimmed reads

``` ./qc_trimmed_reads.sh```
