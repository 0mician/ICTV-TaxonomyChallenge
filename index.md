# Why do we need a computational taxonomy?

There is a consensus that viruses are so diverse that no single
taxonomic method can be used to classify them all (Simmonds et
al. PLoS Biology 2023). Since its inception, the
[ICTV](https://ictv/global) has been seeking the expertise of the
global virology community to classify viruses in accordance with their
domain-specific knowledge. This has generated a patchwork of methods
that, ideally, capture the features of different viral lineages and
generate meaningful taxa that are in agreement with biology. These
methods are formalized in taxonomy proposals (TaxoProps) written by
experts and ratified by the ICTV. These documents describe how viruses
within each taxon shall be classified, and include specific
demarcation criteria. The TaxoProps are available as Word documents on
the [ICTV website](https://ictv.global/files/proposal/approved).</a>

As metagenomics is rapidly expanding our view of the virosphere, we
are looking to make sense of the sequences we discover. The number and
diversity of sequences found in viromics datasets is staggering and
make their taxonomic classification a daunting task that one would
ideally automate. There is currently no ICTV-approved method to
approach this question. While the solution will likely not be trivial,
we have to face this challenge to keep up with the growth of viruses
that we aim to classify. The ICTV Taxonomy Challenge is our first 
attempt at assessing the different computational tools that are 
available for virus taxonomy. 

# The methodology

For the challenge, we have collected XXX viral sequences that experts
have classified into the various ranks of the ICTV taxonomy. These
sequences are available as a multi-fasta file (see below).  We ask you
to classify these sequences using your pipeline and submit your
results to us for validation. Importantly, we ask that your pipeline
is reproducible and that you make available the necessary code and
environment to run it. Multiple strategies exist, such as the creation
of virtual environments (venv, conda) or containers (Singularity,
Docker) and the pipeline should be made available via a git repository
(Github, Bitbucket). The results of your classification will be
evaluated on multiple metrics, including reproducability, speed,
accuracy at different ranks, for different types of viruses,
etc. After the challenge has been closed, we envision writing a report
of the community's finding and believe this will inform current
efforts within the ICTV.

# The dataset

The challenge sequences are available in a fasta file here.  Every
sequence in the file is a different virus contig or genome fragment
with unknown accuracy and unknown completeness. The idea is that these
sequences might have resulted from a metagenomics experiment, and your
challenge is to classify them into ICTV-approved taxa.  We ask that
your pipeline returns a tab-separated values (.tsv) file with XXX rows
representing the contigs and 31 columns as listed below. Fields can be
left empty if no annotation is available at a certain rank. If your
tool provides a score for a given prediction it may be added, but the
score fields may also be left empty. We have provided a .csv template
for you to use here.

* SequenceID
* Realm (-viria)
* Realm_score
* Subrealm (-vira)
* Subrealm_score
* Kingdom (-virae)
* Kingdom_score
* Subkingdom (-virites)
* Subkingdom_score
* Phylum (-viricota)
* Phylum_score
* Subphylum (-viricotina)
* Subphylum_score
* Class (-viricetes)
* Class_score
* Subclass (-viricetidae)
* Subclass_score
* Order (-virales)
* Order_score
* Suborder (-virineae)
* Suborder_score
* Family (-viridae)
* Family_score
* Subfamily (-virinae)
* Subfamily_score
* Genus (-virus)
* Genus_score
* Subgenus (-virus)
* Subgenus_score
* Species (binomial)
* Species_score

<div class="table-wrapper">
<table>
  <thead>
    <tr>
      <th>SequenceID</th>
      <th>Realm</th>
      <th>Realm_score</th>
      <th>Subrealm</th>
      <th>Subrealm_score</th>
      <th>Kingom</th>
      <th>Kingom_score</th>
      <th>...</th>
      <!-- ... Add more header columns as needed -->
      <th>Genus</th>
      <th>Genus_score</th>
      <th>Subgenus</th>
      <th>Subgenus_score</th>
      <th>Species</th>
      <th>Species_score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ICTVTaxoChallenge_XXXXX</td>
      <td>Varidnaviria</td>
      <td>0.77</td>
      <td></td>
      <td></td>
      <td>Bamfordvirae</td>
      <td>0.54</td>
      <td>...</td>
      <!-- ... Add more cells for each row as needed -->
      <td>Mimivirus</td>
      <td>0.92</td>
      <td></td>
      <td></td>
      <td>Mimivirus lagoaense</td>
      <td>0.92</td>
    </tr>
    <!-- Add more rows as needed -->
  </tbody>
</table>

<!--|SequenceID|Realm|Realm_score|Subrealm|Subrealm_score|Kingom|Kingom_score|...|Genus|Genus_score|Subgenus|Subgenus_score|Species|Species_score|
|:---------|:----|:----------|:-------|:-------------|:-----|:-----------|:--|:----|:----------|:-------|:-------------|:------|:------------|
|ICTVTaxoChallenge_XXXXX|Varidnaviria|0.77|||Bamfordvirae|0.54|...|Mimivirus|0.92|||Mimivirus lagoaense|0.92|-->

</div>

# How can you send your results?

Our preference would be that you let us know by email where we can
find your repository when you are done with the analysis. The
repository should have a "results" folder where the predictions can be
found as a .tsv file according to the template we provided. The README
of your repository should provide the necessary instructions to
reproduce the results as well as a brief description of the
methodology used for the classification. If you should prefer to leave
your repository private until the end of the challenge, you can invite
"0mician" and "ICTV-VBEG" to your repository when ready.

The deadline for submitting the results is under consideration and
will be announced here when we kickoff the challenge.

# References

* Peter Simmonds, Evelien M. Adriaenssens, F. Murilo Zerbini, Nicola
  G.A. Abrescia, Pakorn Aiewsakun, Poliane Alfenas-Zerbini, Yiming
  Bao, Jakub Barylski, Christian Drosten, Siobain Duffy, W. Paul
  Duprex, Bas E. Dutilh, Santiago F. Elena, María Laura García, Sandra
  Junglen, Aris Katzourakis, Eugene V. Koonin, Mart Krupovic, Jens
  H. Kuhn, Amy J. Lambert, Elliot J. Lefkowitz, Małgorzata Łobocka,
  Cédric Lood, Jennifer Mahony, Jan P. Meier-Kolthoff, Arcady
  R. Mushegian, Hanna M. Oksanen, Minna M. Poranen, Alejandro
  Reyes-Muñoz, David L. Robertson, Simon Roux, Luisa Rubino, Sead
  Sabanadzovic, Stuart Siddell, Tim Skern, Donald B. Smith, Matthew
  B. Sullivan, Nobuhiro Suzuki, Dann Turner, Koenraad Van Doorslaer,
  Anne-Mieke Vandamme, Arvind Varsani, and Nikos Vasilakis (2023),
  Four principles to establish a universal virus taxonomy, <i>PLoS
  Biology</i> <b>21</b>: e3001922, doi:
  [10.1371/journal.pbio.3001922](https://doi.org/10.1371/journal.pbio.3001922)
