# [Debatisse et al., 2024](https://link-url-here.org)

## Associated scripts and files
In this study, we developped a Python script to analyze the information content of randomized libraries at the 2 arms of the recombination site recognized by the integrase of mv4.
This analysis uses multiple packages, some of which are not built-in Python packages.

#### data files
Read counts per heptamers for each randomized bank are provided as *.tsv files organized according to the format:
#Sequence \t before \t after \t nt1 \t nt2 \t nt3 \t nt4 \t nt5 \t nt6 \t nt7

The terms before and after refer to the recombination event with mv4 integrase.

#### Script
mv4armsPasticity.ipynb is a Jupyter Notebook that takes read counts data from one of the 4 data files and computes the information content at each of the seven positions of the mv4 integrase binding sites (B, B', C and C'). Inter-dependencies between pairs of positions were estimated by constructing contingency tables between pairs of nucleotides existing at each pairs of positions. Departure from a purely random association between nucleotides at each pair of position was estimated using Cramer's V. Cramer's V constitutes an effect size and can be interpreted as such, taking into consideration the degree of freedom.

## Ackowlegements
We used the python package [seqlogo](https://github.com/betteridiot/seqlogo) to generate sequence logos produced in the figures of this manuscript.
We also used the Pandas library:
McKinney, W., & others. (2010). Data structures for statistical computing in python. In Proceedings of the 9th Python in Science Conference ([Vol. 445, pp. 51–56](https://conference.scipy.org/proceedings/scipy2010/pdfs/mckinney.pdf))
