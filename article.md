## It’s COMPASlicated: The Messy Relationship between RAI Datasets and Algorithmic Fairness Benchmarks


## Data Biases and Errors in Pretrial RAIs

Fairness in machine learning papers follow the following method, fixed joint distribution.
(X, A, Y ) ∼ D

where Y is a label, A is protected attribute and X covariates. D is distribution.

Bias in Y - recidivism during pretrial or failure to appear (FTA) -> label bias due to construct invalidity and measurement bias
Construct invalidity: pretrial detention is done to prevent only pretrial flight and violent crimes, FTA e re-arrest não há informação.
Measurement bias: re-arrest might miss the desired target for re-offense. It is correlated to protected attribute, different practical policing and bias arrests.
Models for FTA often describe predicting "flight risk", but includes all  non-appearance motives(no transportation, no one to take care of the children). Causing a bias for class and race. 
Due to FTA being a binary outcome, using this attribute for predictions will result in Bias results


Bias in A - group-level attributes used for disparity assessment ['sex','race',etc.]. Even when the protected attribute information appears, it is ofted under noisy measurement processes. COMPAS race categories lack Native Hawaiian or Other Pacific Islander, and redefine Hispanic as race instead of ethnicity.
Solution:  proxy measures (distribution of race by geographic location) are considered noisy misclassifications of the protected attribute., removing them might reduce the bias.


Bias in X - Many covariates used in pretrial are low dimensional summaries of criminal history, such as past arrests or convictions. These measures inherit the biases of the local law enforcement. Black man were arrested more times for trivial things! 
COMPAS question "Is there much crime in your neighborhood" allows racialized meanings of crime.
Noise in covariates leads to statistical inconsistency and group-specific bias.


Data processing that is done by no CS researcher hides ethically complicated decisions.    
"Should past convictions for crimes that are no longer illegal be included in the dataset(number of past convictions)?"

Issues with the distribution of the data - Data is collected downstream of previous decisions; increasing the number of prior charges or direct endogeneity, via differential policing. Introducing selection bias.


## Limits of Algorithmic Fairness in RAI Outputs for Real-World Outcomes

RAIs part of a network which involvs human and institutional discretion. Even if the algorithmic fairness if an intended goal, achieving real-world fairness is on another level of difficulty due to how actors interpret and apply RAI predictions.

Judges sometimes ignore or override RAI recommendations, possibly causing the undermine of the tool's fairness, especially when racial bias in decisions is observed.

Judges deviate from RAI recommendations more for Black defendants than for white ones.

Thresholds for risk levels can vary, caused by jurisdictions, creating inconsistencies in outcomes.

Fair algorihthms cannot ensure equitable results due to human misuse or inconsistent application of it.


## Normative Values Embedded in Use of RAI Datasets

Researchers must enter an ethical debate on values like fairness, justice, equality nad power which involves grappling with assumptions tied to crime and justice.

Key areas: 
    - chosen tasks 
    - outcomes

Ofter inherit implicit values from previous benchmarks taking risk reduction through incarceration over alternatives like rehabilitation, causing harm to individuals and communities.

Statisticall fairness objectives introduce limitations since algorithmic fairness measures may fail to align with broader social ideals of fairness, which are dynamic and context-dependent.

## Established Norms in Fields Engaged in Criminal Justice Work

Dataset Creation Process:
- Data Collection:  
    - Data access has to be taken into account, so the problem of collecting data is troublesome.
    - The administrative records that contain CJ-related data (covariates and outcomes) are stored across multiple systems and agencies with varying identifiers, granularity, and accuracy, requiring intricate record linkage.
    - Management systems are usually outdated, requiring manual data entry and cleaning, which can introduce errors.
    - Interviews add another layer of complexity and potential bias.

- Standards:
    - Key Metrics: 
        - Discrimination: Measures how effectively an instrument distinguishes between individuals who do or do not experience the outcome of interest.
        - Calibration: Measures how well the predicted probabilities align with the observed outcomes.

- Language Guidelines
    - Evolving Terminology: Language use in criminal justice research is shifting to emphasize humanity and avoid dehumanizing terms.
    - Guides and Standards: Recommendations are available from resources like APA Standards for Bias-Free Language and domain-specific publications.
    - Impact on Fairness: Using respectful and current language helps prevent marginalization and aligns with fairness objectives in AI/ML research.

## Mismatch Between AI Fairness Practices and Criminal Justice Research

Focus on Methods Papers.

Datasets are treated as benchmarks for performance rather than as sources for understanding the social context of the data. 

Performance measures take precedence over meaningful analysis or interpretation of the dataset.

Misleading conclusions arise from lack of understanding the social or operational context of the data (e.g., "high-risk" predictions misinterpreted as desirable outcomes).

Align incentives to focus on meaningful engagement with CJ goals.

Collaborate with domain experts to understand data contexts.

Recognize the distinction between scientific and methods contributions.

Challenge the overuse of flawed datasets like COMPAS by emphasizing better, context-aware benchmarks.

## Call To Arms

What Researchers Should Avoid
Using CJ-Related Datasets for General Fairness Benchmarks:

Avoid treating datasets like COMPAS as generic real-world examples to evaluate fairness measures. Such datasets require domain-specific interpretation, and misusing them risks misleading conclusions about CJ issues.

CJ datasets are context-sensitive, varying across jurisdictions, legal systems, and data collection methods. Broad or oversimplified conclusions undermine the complexities of the domain and can be politically contentious.

Clearly articulate modeling assumptions, limitations, and real-world consequences of deploying such systems.

Use simulations or alternate benchmarks where appropriate, and reviewers should encourage this over inappropriate real-world dataset use.

Identify implicit value positions, biases, and contested assumptions embedded in fairness interventions and their measures.

Assess standard metrics (e.g., AUC scores) critically, as they may not reflect disparities across demographics or thresholds.

Develop and adopt new measures (e.g., predictive multiplicity) that reveal nuanced model behaviors and disparities.