# swot-matrix-group-decision
Selecting and ordering elements of the swot matrix through a multicriteria and group decision-making approach


## Contents
- [Requirements](#Requirements)     
- [Methodology](#Methodology)
- [Solution](#Solution)
- [References](#References)

## Requirements

```bash
python pip install -r requirements.txt
```

## Methodology

The focus of this work is to propose a group decision-making method for sorting and selecting which elements (which we will call alternatives) of strengths, weaknesses, threats and opportunities will make up the SWOT matrix that will serve as input for defining strategies.

In order to select the most suitable set for each of the quadrants of the SWOT matrix from a large number of alternatives, it was deemed necessary to define criteria and sub-criteria that could correlate each of the lists of interest, in order to reduce the number of evaluations required by each decision-maker.

The alternatives were raised at a Strategic Planning workshop (“Diagnosis” phase) held in November/22 at Unicamp's DEPI administrative body (Executive Directorate for Integrated Planning) with a group of 27 civil servants from the body. The decision-maker will fill in the verbal evaluations of the qualitative criteria/subcriteria, using a 5-point scale (Very High, High, Medium, Low and Very Low), for each quadrant of the SWOT matrix. The model spreadsheet that was filled in by the decision-makers can be found at Assets\Decisors

With the decision matrices filled in and the weights determined, the PROMETHEE-II method was used to obtain the rankings of the lists in each quadrant, using the net flow as a parameter

For the quantitative criteria, which referred to the number of strengths and weaknesses that were related to opportunities and threats, and vice versa, the linear preference function was adopted, with thresholds at 𝑞 = 1 and 𝑝 = 4. For the other criteria, the usual preference function was chosen, as it is a more subjective, less quantified judgment, less quantifiable.

Once the individual rankings of each of the decision-makers had been obtained, according to their own assessments of the community nature of the decision, a group decision-making method was used to define the final ranking of the group of people. The Borda and Condorcet methods were used to add value to each of the alternatives in each quadrant of the SWOT matrix.

```mermaid
flowchart LR
    A[Start] --> B[Strategic Planning Workshop]
    B --> C[Define Criteria and Sub-Criteria]
    C --> D[Decision-Maker Evaluations]
    D --> E[Determine Weights]
    E --> F[Create Decision Matrices]
    F --> G[Apply PROMETHEE-II Method]
    G --> H[Preference Functions]
    H --> I[Obtain Individual Rankings]
    I --> J[Group Decision-Making]
    J --> K[Define Final Rankings]
    K --> L[End]
```

## Solution

### Ranking of "Weak Points"

| #  | Description                                                   | D1  | D2  | D3  | D4  | Borda | Condorcet | Of. 17/nov |
|----|---------------------------------------------------------------|-----|-----|-----|-----|-------|-----------|------------|
| WP1 | Lack of clarity of objectives to be achieved                  | 1   | 3   | 1   | 7   | 2     | 1         | 1          |
| WP2 | Poorly defined work processes                                 | 2   | 1   | 2   | 1   | 1     | 2         | 2          |
| WP3 | Lack of adequate information system for the current process   | 3   | 2   | 3   | 2   | 4     | 3         | 4          |
| WP4 | Deficient institutional communication                         | 4   | 7   | 4   | 9   | 6     | 4         | 5          |
| WP5 | Lack of integration between DEPI sectors                      | 5   | 4   | 7   | 6   | 3     | 6         | 9          |
| WP6 | Staff shortage                                                | 6   | 5   | 5   | 4   | 8     | 8         | 3          |
| WP7 | Few university training opportunities                         | 7   | 8   | 8   | 8   | 10    | 10        | 8          |
| WP8 | Poor internal communication between teams                     | 8   | 10  | 9   | 10  | 9     | 7         | 6          |
| WP9 | Lack of user knowledge about services provided                | 9   | 11  | 10  | 11  | 12    | 9         | 7          |
| WP10| Unclear project and venture area definition                   | 10  | 9   | 11  | 5   | 5     | 5         | 10         |
| WP11| Underutilized talents                                         | 11  | 6   | 6   | 3   | 7     | 11        | 11         |
| WP12| Delay in returning some requests                              | 12  | 12  | 12  | 13  | 13    | 12        | 13         |
| WP13| Physical separation of teams                                  | 13  | 13  | 13  | 12  | 11    | 13        | 12         |

### Ranking of "Strong Points"

| #  | Description                                                   | D1  | D2  | D3  | D4  | Borda | Condorcet | Of. 17/nov |
|----|---------------------------------------------------------------|-----|-----|-----|-----|-------|-----------|------------|
| SP1 | Committed professionals                                       | 1   | 1   | 1   | 2   | 1     | 1         | 1          |
| SP2 | Technical quality of professionals                            | 2   | 2   | 4   | 1   | 3     | 2         | 2          |
| SP3 | Incentive to new initiatives                                  | 3   | 4   | 3   | 6   | 2     | 3         | 4          |
| SP4 | Systemic view                                                 | 4   | 3   | 2   | 3   | 4     | 4         | 3          |
| SP5 | Comprehensive and disseminable knowledge                      | 5   | 5   | 5   | 4   | 6     | 5         | 5          |
| SP6 | Active role in university decision-making support             | 6   | 9   | 6   | 8   | 5     | 6         | 8          |
| SP7 | Actions impact the community                                  | 7   | 6   | 8   | 5   | 9     | 8         | 7          |
| SP8 | Autonomy and confidence in decision-making                    | 8   | 7   | 10  | 9   | 7     | 7         | 6          |
| SP9 | Clarity and detail of standardized procedures and processes   | 9   | 8   | 9   | 12  | 11    | 9         | 9          |
| SP10| Internal communication                                        | 10  | 11  | 7   | 11  | 10    | 10        | 11         |
| SP11| Coordination of DEPI with Unicamp's organizational structure  | 11  | 10  | 11  | 10  | 8     | 11        | 10         |
| SP12| Incentive for training                                        | 12  | 14  | 12  | 14  | 14    | 12        | 13         |
| SP13| Team and environment                                          | 13  | 13  | 13  | 13  | 12    | 13        | 12         |
| SP14| Good communication with users                                 | 14  | 12  | 14  | 15  | 13    | 14        | 15         |
| SP15| Good infrastructure and working conditions                    | 15  | 15  | 15  | 16  | 15    | 15        | 14         |
| SP16| Good service                                                  | 16  | 16  | 16  | 7   | 16    | 16        | 16         |

### Ranking of "Opportunities"

| #  | Description                                                   | D1  | D2  | D3  | D4  | Borda | Condorcet | Of. 17/nov |
|----|---------------------------------------------------------------|-----|-----|-----|-----|-------|-----------|------------|
| OP1 | Growth of the sustainability theme                            | 1   | 1   | 1   | 2   | 1     | 2         | 1          |
| OP2 | Resources for projects and actions                            | 2   | 2   | 6   | 4   | 3     | 1         | 2          |
| OP3 | Use of BIM technology                                         | 3   | 6   | 2   | 1   | 4     | 3         | 3          |
| OP4 | Work improvement with the use of ICT                          | 4   | 7   | 11  | 5   | 7     | 4         | 5          |
| OP5 | University events                                             | 5   | 3   | 4   | 3   | 2     | 5         | 8          |
| OP6 | Interest of external agents in new partnerships               | 6   | 4   | 7   | 7   | 6     | 6         | 7          |
| OP7 | Representation in external bodies                             | 7   | 8   | 3   | 9   | 8     | 7         | 6          |
| OP8 | Sponsorship fund, new financing for DEPI actions              | 8   | 5   | 5   | 6   | 5     | 8         | 10         |
| OP9 | Valorization and recognition of competencies                  | 9   | 11  | 10  | 11  | 10    | 9         | 11         |
| OP10| University environment innovation                             | 10  | 9   | 9   | 8   | 9     | 10        | 9          |
| OP11| Law 14.133 streamlining bidding process from 2023             | 11  | 12  | 8   | 10  | 12    | 11        | 4          |
| OP12| Legal support and security                                    | 12  | 10  | 12  | 12  | 11    | 12        | 12         |

### Ranking of "Threats"

| #  | Description                                                                                             | D1  | D2  | D3  | D4  | Borda | Condorcet | Of. 17/nov |
|----|---------------------------------------------------------------------------------------------------------|-----|-----|-----|-----|-------|-----------|------------|
| T1  | Resistance of the university community to integrated planning and management policies                  | 1   | 1   | 3   | 1   | 1     | 1         | 1          |
| T2  | Growth in demand beyond operational capacity                                                           | 2   | 12  | 1   | 8   | 2     | 2         | 2          |
| T3  | Lack of infrastructure and resistance to process automation                                            | 3   | 2   | 16  | 14  | 7     | 3         | 18         |
| T4  | HIDS: the beginning of the occupation of Fazenda Argentina will bring high demand for DEPI services    | 4   | 5   | 13  | 9   | 6     | 6         | 18         |
| T5  | Budgetary implications                                                                                 | 5   | 10  | 7   | 13  | 8     | 18        | 4          |
| T6  | Low quality of contracted companies/products/services                                                  | 6   | 6   | 11  | 5   | 4     | 4         | 3          |
| T7  | Difficulty interfacing with other technical and administrative areas of Unicamp                        | 7   | 4   | 10  | 6   | 3     | 5         | 4          |
| T8  | Intrusion of the new São Paulo state government into the university's budget autonomy                   | 8   | 11  | 17  | 3   | 10    | 18        | 18         |
| T9  | Change in the political scenario                                                                       | 9   | 8   | 14  | 7   | 9     | 7         | 18         |
| T10 | Health threats                                                                                         | 10  | 15  | 12  | 4   | 13    | 18        | 18         |
| T11 | Obstruction by the university's general counsel                                                        | 11  | 13  | 8   | 15  | 15    | 18        | 18         |
| T12 | Uncertainty in criteria and resource volume for university career progression policies                 | 12  | 18  | 5   | 11  | 14    | 18        | 18         |
| T13 | Loss of talent                                                                                         | 13  | 9   | 4   | 2   | 5     | 8         | 3          |
| T14 | Personal interests above technical decisions                                                           | 14  | 14  | 2   | 10  | 11    | 18        | 18         |
| T15 | Deterioration of Unicamp's built heritage                                                              | 15  | 7   | 6   | 12  | 12    | 18        | 18         |
| T16 | Vulnerability of automated systems can cause data leaks                                                | 16  | 17  | 18  | 16  | 17    | 18        | 18         |
| T17 | Unpreparedness to work on inclusion can cause internal conflicts                                       | 17  | 3   | 9   | 17  | 16    | 18        | 18         |
| T18 | Repeal or relaxation of existing legislation                                                           | 18  | 16  | 15  | 18  | 18    | 18        | 18         |

For all the quadrants, shown above, it can be seen that the Borda and Condorcet methods are very close, but when compared to the results of the simple vote carried out to sort and select the items by the group on 17/11/22, the relationship is very different.

Regarding the simple voting method, it is necessary to consider some factors that may explain the discrepancy:

- The simple voting was conducted by 27 people, while the proposed method was carried out with a sample of four people from this group, and it cannot be stated that these participants represent the diversity of opinion within the group.

- In the simple voting, each participant could vote for up to three alternatives from the internal environment and three alternatives from the external environment during the workshop (a task completed in around 15 minutes). Consequently, there is no thorough analysis of each item, possibly resulting in votes based on pre-established preferences (which consider more personal interests).

- Since the simple voting is open, everyone has access to the alternatives with the most votes. This can lead participants to align their votes with the majority to avoid "wasting" their vote, resulting in some items receiving many votes while many other items receive none.

Finally, in the case of the “Threat” alternatives, the Condorcet method was able to sort up to the 8th element, with the other items tied in the next position. The Borda method therefore proved to be a better alternative for this case, as it was possible to sort all the cases.

### Final swot matrix

![Final_swot_matrix](Assets/Images/Final_swot_matrix.jpg)

The practical application of the proposed method was evaluated through real-world implementation. The individual weightings and rankings were carried out by staff members actively involved in the process, using alternatives from an actual case within a department of Unicamp that is currently developing its Strategic Planning. This approach generated valuable feedback on both the material and the method, indicating the feasibility of applying this methodology on a larger scale. The practical insights and improvements suggested by participants reinforce the method's relevance and applicability, confirming its potential for effective strategic decision-making in real organizational contexts.

## References

[1] Alptekín, N. (2013) Integration of SWOT Analysis and TOPSIS Method In Strategic Decision
Making Process. Anadolu University Faculty of Business Administration, Turkey.

[2] Atvars, T. D. Z; Serafim, M. (2020) Gestão estratégica Planes: planejamento estratégico –
Universidade Estadual de Campinas – UNICAMP 2021-2025 - Campinas, SP: UNICAMP/CGU;
BCCL, 2020.

[3] Ishizaka, A.; Nemery, P. (2013) Multi-Criteria Decision Analysis: Methods and Software. 1° Ed.
John Wiley & Sons, Ltd: New Delhi, India.

[4] Kangas, J. ; Pesonen, M.; Kurttila, M.; Kajanus, M., (2001) A'WOT: INTEGRATING THE AHP
WITH SWOT ANALYSIS. Finnish Forest Research Institute Kannus Research Station.

[5] Toni, J. (2021) Reflexões sobre o Planejamento Estratégico no Setor Público / Jackson de Toni. –
Brasília: Enap.

[6] Živkovic’, Z.; Nikoli’c, D.; Savic’, M; Djordjevic’, P.; Mihajlovic’, I. (2017) Prioritizing
Strategic Goals in Higher Education Organizations by Using a
SWOT–PROMETHEE/GAIA–GDSS Model. Engineering Management Department, University
of Belgrade, Technical Faculty in Bor - DOI: 10.1007/s10726-017-9533-y