# Quality and Utility Dimensions

### What is the difference between accuracy and precision?

In short, the key difference is:

\- Accuracy is about correctness. The degree to which observations correctly describe what it was designed to measure. (Is the value factually true?) &#x20;

\- Precision is about the level of detail. The degree of approximation by which data can represent reality. (Is the value recorded with enough granularity for its purpose?)

**Example:**

\- A BMI value of 500 is an Accuracy problem. It is implausible and factually incorrect, failing the "Real-world alignment" check.

\- A BMI value of 24.5 is a Precision problem if a research study required three decimal places (e.g., 24.512). The value 24.5 may be accurate (generally correct), but it is imprecise (lacks the required level of detail) for that specific use case.

### &#x20;What is validity?

Quantum defines the validity dimension as “the degree to which representations of data in a dataset conform to the specification of a data model or data models”.

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

<br>
