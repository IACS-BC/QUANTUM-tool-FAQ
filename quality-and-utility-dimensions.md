# Quality and Utility Dimensions

### Q1.- What is the difference between accuracy and precision?

A.- In short, the key difference is:

\- Accuracy is about correctness. The degree to which observations correctly describe what it was designed to measure. (Is the value factually true?) &#x20;

\- Precision is about the level of detail. The degree of approximation by which data can represent reality. (Is the value recorded with enough granularity for its purpose?)

**Example:**

\- A BMI value of 500 is an Accuracy problem. It is implausible and factually incorrect, failing the "Real-world alignment" check.

\- A BMI value of 24.5 is a Precision problem if a research study required three decimal places (e.g., 24.512). The value 24.5 may be accurate (generally correct), but it is imprecise (lacks the required level of detail) for that specific use case.

### &#x20;Q2.- What is validity?

A.- Quantum defines the validity dimension as “the degree to which representations of data in a dataset conform to the specification of a data model or data models”.

This definition ensures that data adheres to the structural, semantic, and logical constraints defined by a data model or business specification. This includes compliance with:

* Formats and data types
* Accepted code lists or value domains
* Structural rules (e.g., uniqueness, presence of required fields)
* Derivation logic
* Referential integrity with external systems
* Built-in business or domain constraints

Example 1: Ensuring compliance with HL7 FHIR standards for data exchange.\
Example 2: Verifying that ICD-10 codes in a diagnostic column are valid.\
Example 3: Validating that data entries conform to predefined care sets (e.g., clinical pathways or specialty-specific documentation templates).

### &#x20;Q3 .- What is precision?

A.- Quantum defines the precision dimension as “the degree of approximation by which data can represent reality”.

Precision is the degree of approximation by which data values can represent real-world phenomena, reflecting how closely recorded values mirror the underlying reality and whether they are captured with an appropriate level of resolution and granularity for the dataset’s intended purpose.

* Resolution describes the numerical or temporal detail of data values—such as the number of decimal places, significant figures, or timestamp intervals—ensuring small but meaningful variations are preserved and that analyses or decisions can detect critical changes.
* Granularity refers to the selection of measurement—such as choosing milligrams over grams for low-dose medications or recording blood pressure as “120/80 mmHg” rather than “normal”—so that data is neither excessively coarse nor misleadingly aggregated.

For example, you can check the ratio of records in a measurement table that use the correct unit (e.g. kilograms in BMI).

Accuracy and precision are not synonyms. Saying that "Einstein was born in the 19th century" isn't very precise, but it is accurate. Saying that "Einstein was born on September 5, 1925, at 8:35:54 PM" is very precise, but completely inaccurate.

### &#x20;Q4.- What is accuracy?

Quantum defines the accuracy dimension as “the degree to which observations correctly describe what it was designed to measure”.

In practice, accuracy assesses whether a data value correctly represents the real-world entity or fact it is intended to capture. It considers whether the information is factually correct, error-free, and can be independently verified using a reliable source or reference. High data accuracy enables real-world entities to be correctly identified and to function as intended within processes or systems.

For example, you can check the ratio of records in a measurement table that have values "out of range", and not clinicaly plausible.

Accuracy and precision are not synonyms. Saying that "Einstein was born in the 19th century" isn't very precise, but it is accurate. Saying that "Einstein was born on September 5, 1925, at 8:35:54 PM" is very precise, but completely inaccurate.



### Q5.- We have no specific report on quality checks, but we can provide it on-demand

A.- It may occur that a dimension has been assessed to some extent but without having a dedicated report to describe it, or not being publicly available. As long as you can prove somehow the assesed accuracy, you can set it as "**documented**". You may not have a structured report, but if someone (i.e. an HDAB) asks for supporting documentation regarding the accuracy checks made, you should have a way to prove/show which type of ckeck you did and how. If you cannot, then it is "**not documented**".<br>

### Q6.- What does "eligible population" mean?

The "eligible population" depends on the purpose and design of the specific dataset. If the dataset is population-based and aims to cover the entire population of a given territory, the "eligible population" is the population of that entire territory. If it is a specific registry, for example, a tumor registry, the "eligible population" will be the entire population diagnosed with a tumor in the relevant geographic area. Population coverage must be calculated based on this "eligible population." If the dataset is designed as a random sample, the "eligible population" will be the population from which the sampling is performed.

\
\
<br>
