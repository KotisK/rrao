# **RRAO**

RRAO: An Ontology for the Representation of Knowledge for Reoffending Risk Assessment

## **Overview**

The **Reoffending Risk Assessment Ontology (RRAO)** is a formal and reusable ontology designed to model knowledge related to **reoffending risk and recidivism**. Developed as part of the **FAIR-PReSONS project**, RRAO enables unbiased representation of data concerning criminal offenses, penalties, judicial decisions, and socio-demographic factors influencing reoffending.

This ontology supports **semantic integration** of heterogeneous legal and correctional datasets.

---

## **Ontology Documentation**

For a full ontology documentation, see [https://w3id.org/rrao](https://w3id.org/rrao).

---

## **Key Features**
- Alignment with international standard **International Classification of Crime for Statistical Purposes (ICCS)**.
- Extending ODRL and linking to EuroVoc

---

## **LLM Assisted Development**
LLMs were utilized for scaffolding a kick-off ontology and leveraged in the step for bias assessment. LLM models (Gemini, Claude 3.5 and GPT4-ο) were prompt with the zero-shot method. Examples of the prompts and responses can be found on the **[LLM experiments](LLM%20experiments)** directory.

## **SPARQL Query Example**
What are the demographic and socio-economic characteristics of an imprisoned person?
```sparql
PREFIX rrao: <http://w3id.org/rrao#>
SELECT DISTINCT ?age ?sex ?educationLevel
?reportedOccupation ?occupationCategory ?maritalStatus
WHERE {
    ?person a rrao:imprisoned .
    ?person rrao:generalRegisterNumber "123" ;
    rrao:ageGroup ?age ;
    rrao:sex ?sex ;
    rrao:levelOfEducation ?educationLevel ;
    rrao:reportedOccupation ?reportedOccupation ;
    rrao:reportedOccupationCategory ?occupationCategory;
    rrao:maritalStatus ?maritalStatus .
}
```

SPARQL examples can be found in the **queries/** directory.

---

## **License**
This ontology is released under the **Creative Commons 0  (CC0)** license.

---

## **Contact & Support** 
📧 **Email**: [sotiris@aegean.gr](mailto:sotiris@aegean.gr)

📌 **Project Page**: [https://fair-presons.aegean.gr/](https://fair-presons.aegean.gr/)

