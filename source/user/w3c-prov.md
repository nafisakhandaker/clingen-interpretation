---
title: W3C-Prov
description: Relationship/mapping of our model to the recommendations o the W3C-PROV working group
model: interpretation

---

[W3C-Prov](https://www.w3.org/TR/prov-overview/) is a specification for defining the provenance of objects. That is, given an object, this framework provides a standard way to say:

* who generated (created) the object
* when they generated it
* what type of activity was used to generate it
* which other objects were used in the generation

W3C-Prov is composed of three types: *Entity*, *Activity*, and *Agent*.  **Entities** are simply the things in the model.  In the interpretation model, the entities are:

* An interpretation (e.g. An allele is pathogenic for a given condition)
* An Assessed Criteria (e.g. PP2 for a given allele and condition provides supporting evidence of pathogenicity)
* Evidence Statements (e.g. a population frequency of an allele, segregation data, prevalence of a condition)
* Evidence Sources (e.g., Publications, database records)

Entities have provenance; each was generated by a particular *Activity*. **Activities** are an action that lasted for a particular time range, which used some entities to generate other entities.  In the interpretation model, the activities correspond to those listed above:

* Evidence capture, which uses Evidence Sources to generate Evidence Statements
* Criteria Assessment, which uses Evidence Statements to generate AssessedCriteria
* GenerateInterpretation which uses AssessedCriteria to generate Interpretations

**Agents** are associated with *Activities* and *Entities*, and answer the question of who performed the activity.  *Agents* may be individuals, but may also be groups, such as an expert panel, or a software agent, such as one that automatically loads evidence from a source.
