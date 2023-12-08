# iProtDNA-SAGE
# Project tree
- data<br>
  - PDNA-316_label.fasta<br>
  - PDNA-316_sequence.fasta<br>
  - PDNA-335_label.fasta<br>
  - PDNA-335_sequence.fasta<br>
  - PDNA-41_label.fasta<br>
  - PDNA-41_sequence.fasta<br>
  - PDNA-52_label.fasta<br>
  - PDNA-52_sequence.fasta<br>
  - PDNA-543_label.fasta<br>
  - PDNA-543_sequence.fasta<br>
- Dataset.py<br>
- distance_matrix.py<br>
- esm2.py<br>
- esmfold.py<br>
- evaluate.py<br>
- Focal_Loss.py<br>
- graphsage.py<br>
- k-folder_cross-validation.py<br>
- SAGE_classifier.py<br>
- README.md<br>
# Requirements
- torch=2.0.0+cu118<br>
- torch-geometric=2.3.0<br>
- torch-scatter=2.1.1+pt20cu118<br>
- torch-sparse=0.6.17+pt20cu118<br>
- torchvision=0.15.1+cu118<br>
- scikit-learn<br>
- scipy=1.10.1<br>
- PyGCL=0.1.2<br>
- dgl=1.0.0<br>
- biopython<br>
- numpy<br>
- tqdm<br>
# If you want to reproduce our model, follow the steps below to run the script.
1. Use the pre-trained ESMFold_v1 model to predict the protein structure and save the structure as a PDB file. You can run the following script.<br>
&bull;`esmfold.py`
2. Get DNA sequence data and saves the representation of each residue as a CSV file. You can run the following script.<br>
&bull;`esm2.py`
3. Calculate the distance matrix between each amino acid residue on a given protein chain and save the result as a CSV file. You can run the following script.<br>
&bull;`distance_matrix.py`
4. Data Processing. You can run the following script.<br>
&bull;`Dataset.py`
5. Use SAGE model for training and evaluate the performance of the model on a test set. You can run the following script.<br>
&bull;`SAGE_classifier.py`
6. Evaluate the performance of the SAGE model on the DNA sequence classification task by cross-validation and calculate the performance metrics of the model. You can run the following script.<br>
&bull;`k-folder_cross-validation.py`

