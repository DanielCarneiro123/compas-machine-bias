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
Solution:  proxy measures (distribution of race by geographic location) 


Bias in X - Many covariates used in pretrial are low dimensional summaries of criminal history, such as past arrests or convictions. These measures inherit the biases of the local law enforcement. Black man were arrested more times for trivial things! 
COMPAS question "Is there much crime in your neighborhood" allows racialized meanings of crime.
Noise in covariates leads to statistical inconsistency and group-specific bias.


Data processing that is done by no CS researcher hides ethically complicated decisions.    
"Should past convictions for crimes that are no longer illegal be included in the dataset(number of past convictions)?"

Issues with the distribution of the data - Data is collected downstream of previous decisions; increasing the number of prior charges or direct endogeneity, via differential policing. Introducing selection bias.


## Limits of Algorithmic Fairness in RAI Outputs for Real-World Outcomes

RAIs are not standalone systems but parts of complex socio-technical networks involving human and institutional discretion. While algorithmic fairness is often a design goal, achieving real-world fairness is challenging because multiple actors interpret and apply RAI predictions differently. Judges frequently exercise their discretion, sometimes ignoring or overriding RAI recommendations, which can undermine the tool’s fairness, especially when racial bias in decisions is observed—studies have shown that judges may deviate from RAI recommendations more for Black defendants than for white ones. Moreover, jurisdictions can set varying thresholds for risk levels, which creates inconsistencies in outcomes across locations. This is notable in COMPAS, where critiques centered around the racial disparities in its risk scores and the potential for bias, highlighting how RAIs might perpetuate inequalities when local authorities adapt or disregard the algorithm’s guidelines. Ultimately, human judgment in interpreting and applying RAI outputs significantly affects the fairness of outcomes, as even the fairest algorithm cannot ensure equitable results if misused or inconsistently applied.


## Normative Values Embedded in Use of RAI Datasets

Researchers developing RAIs for the criminal legal system engage in more than just technical work on fair algorithms; they enter a broader ethical debate on values like fairness, justice, equality, and power. This work inherently involves grappling with normative assumptions tied to crime and justice. Key areas of concern include the chosen tasks and outcomes: these often inherit implicit values from previous benchmarks, prioritizing risk reduction through incarceration over alternatives like rehabilitation, which can perpetuate harm to individuals and communities. The use of statistical fairness objectives introduces limitations since algorithmic fairness measures may fail to align with broader social ideals of fairness, which are dynamic and context-dependent. Researchers must consider whether their chosen fairness metrics truly address social inequities or merely reflect the biases of existing systems. Real-world impact considerations in RAI research implicitly support certain criminal justice reforms, such as decarceration, decriminalization, or bail reform, each of which reflects distinct values and theories about justice and change. 