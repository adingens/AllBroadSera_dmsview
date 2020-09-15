# Mutational antigenic profiling of broad sera (purified IgG) responses 

Adam S. Dingens, Jesse D. Bloom, in collaboration to Florian Klein's group

# Brief description
We used mutational antigenic profiling with BG505.T332N libraries to map how all mutations to Env affect neutralization of purified IgG from numerous patients with broad serum responses. 

# Brief interpretation
For many sera, there is a clear dominant neutralizing epitope **to BG505**. This is oftentimes a characterized bnAb epitope. 

- IDF147 and IDC0136 target the apex bnAb epitope.
- IDC208, IDC0396, IDF0337, IDC0245, IDC0191 and IDC403 targets the N322 glycan epitope, but with residue level specificity differing, as expected. Interestingly, IDF141 targets the V3 loop and 156 glycan but not the N332 glycan).
- IDF065 targets the C3/V5 epitope often elicited with trimer immunization.  
- IDF033 targets CD4bs, specifically the N276 glycan.
- Other sera are noisier; we cannot currently disentangle if this is due to targeting very conserved sites (such as the CD4bs, as we know for IDC561)ß, multiple sites, or technical noise in the assay. 

# Description of selection statistics

[This page](https://jbloomlab.github.io/dms_tools2/diffsel.html) documents the differential selection statsitics we use to analyze these data.

The most useful statistics to examne are the positive_diffsel (at the site level) and the positive differential selection (at the mutation level). 

The site-metrics (dot plot) include:

- **positive diffsel**: The sum of all positive differential selection values at a site. This gives a sense to the total amount of escape/selective pressure at each site.
- **negative diffsel**: The sum of all negative differential selection values at a site. This gives a sense for mutations that are depleted, rather than enriched, during serum selection relative to a non-selected control library. It is intriguing that many of these potential serum sensitizing mutations cluster and are consistent across sera.
- **max diffsel**: The value of the largest effect mutation (largest mutation differential selection) at each site. This gives a sense of the maximal effect of any mutation at each site.
- **min diffsel**: The value of the smallest effect mutation (smalled mutation differential selection) at each site.
- **abs diffsel**: The absolute value of all mutation differential selection values at each site.

The mutation-metrics (logoplot) include

- **diffsel**: All mutation differential selection values, including negative values, are plotted.
- **pos diffsel**: Only the mutations with positive differential selection values.

# Sample meta data
Each sera was run a different number of times. In the table below, we have the each replicate for each sera (or mAb). More detailed data exists in the analysis repo. 
1-18 and 2-12, mAbs isolated from patient IDC0561, are also included here.
QA013-2282dpi is sera at 2282 days post infection from QA013 (Julie Overbaugh), and QA013-2 is a mAb isolated from that patient. These samples would likely not be included in any publication on this cohort, but are included here for reference. 


- **sera** is the sera / purified IgG /  mAb studied. The number of times it appears below is the number of replicates performed. I **have not** extensively pruned noisy replicates from this data. 
- **concentration-replicate** indicates the IgG (or mAb) concentration used during selection, as well as the viral library replicate for that experiment. 
- **percent infectivity** is the percent of the viral library that survived sera selection and entered cells in that experiment. 

| sera          | concentration-replicate | percent infectivity |
|---------------|-------------------------|---------------------|
| 118           | 4ug-rep2d               | 0.5177235           |
| 118           | 8ug-rep2d               | 0.0167766           |
| 118           | 4ug-rep3d               | 0.5181678           |
| 118           | 8ug-rep3d               | 0.0673469           |
| 212           | 8ug-rep3e               | 0.6214775           |
| 212           | 10ug-rep1v2a            | 0.2501396           |
| 212           | 7ug-rep1v2a             | 0.7341482           |
| 212           | 6ug-rep1v2b             | 3.4943168           |
| IDC0136       | 5500ug-rep1v2b          | 13.6000955          |
| IDC0136       | 7000ug-rep1v2b          | 6.2973304           |
| IDC0136       | 8500ug-rep1v2b          | 4.126587            |
| IDC0191       | 6000ug-rep3v2a          | 0.0491656           |
| IDC0245       | 8000ug-rep3v2a          | 0.1750749           |
| IDC0337       | 4000ug-rep1v2b          | 10.200934           |
| IDC0337       | 4500ug-rep1v2b          | 9.1161243           |
| IDC0337       | 6000ug-rep1v2b          | 5.9009668           |
| IDC0396       | 9000ug-rep3v2a          | 0.3733771           |
| IDC0513       | 5000ug-rep3v2a          | 0.097499            |
| IDC0518       | 8000ug-rep3v2a          | 6.0662594           |
| IDC0546       | 8500ug-rep3v2a          | 1.1035201           |
| IDC208        | 6000ug-rep1v2b          | 6.8418903           |
| IDC208        | 5000ug-rep1v2b          | 10.3580829          |
| IDC208        | 4000ug-rep1v2b          | 15.0961614          |
| IDC403        | 7500ug-rep1v2b          | 0.0893057           |
| IDC403        | 6000ug-rep1v2b          | 0.1969129           |
| IDC403        | 8500ug-rep1v2b          | 0.0359057           |
| IDC561        | 2500ug-rep3e            | 2.3229919           |
| IDC561        | 3000ug-rep1v2a          | 0.2478397           |
| IDC561        | 3500ug-rep1v2a          | 0.181995            |
| IDC561        | 2800ug-rep1v2b          | 0.7366521           |
| IDC561        | 2200ug-rep1v2b          | 1.2112296           |
| IDF033        | 1400ug-rep3v2a          | 0.1389969           |
| IDF033        | 1800ug-rep3v2a          | 0.0730342           |
| IDF065        | 1400ug-rep3v2a          | 0.7029193           |
| IDF141        | 6000ug-rep3v2a          | 0.0234801           |
| IDF147        | 5300ug-rep3v2a          | 0.4490444           |
| QA013-2       | 2ug-rep2                | 3.2488              |
| QA013-2       | 4ug-rep2                | 0.2637              |
| QA013-2       | 4ug-rep3                | 0.1661              |
| QA013-2282dpi | d7-5-rep3e              | 0.0388446           |
| QA013-2282dpi | d10-rep1v2a             | 0.0316654           |
| QA013-2282dpi | d15-rep1v2a             | 0.1444478           |
| QA013-2282dpi | d40-rep1v2b             | 47.0668784          |
| QA013-2282dpi | d25-rep1v2b             | 27.8700662          |

