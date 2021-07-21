This FHIR resources library supports the needs of realm-specific cancer pathology reporting implementation guides. It does not provide any use case or scenario specific content or additional guidance on how to use these artifacts, but serves as a source for a standard set of profiles for reuse in multiple use case specific implementation guides focusing on the exchange of cancer pathology information. Implementation details such as how and when to use a given artifact, value set definitions, etc. will be supplied in these guides.

### Scope
This guide defines 6 FHIR profiles:
* Pathology Bundle (derived from FHIR R4 Bundle)
* Pathology MessageHeader (derived from FHIR R4 MessageHeader)
* Pathology DiagnosticReport (derived from FHIR R4 DiagnosticReport)
* Pathology Specimen (derived from FHIR R4 Specimen)
* Pathology NextOfKin (derived from FHIR R4 RelatedPerson)
* Pathology-Related PractitionerRoles (derived from FHIR R4 PractitionerRole)

This guide defines 2 value sets:
* US Public Health MessageTypes
* Pathology Related PractitionerRoles ValueSet 	

This guide defines 2 code systems:
* US Public Health Message Type Code System
* Pathology Related PractitionerRoles CodeSystem 	

### Dependencies
This IG is conformant to the base [FHIR R4](https://www.hl7.org/fhir/) specification.

### Audience
The audience for this resource includes architects and developers of clinical and pathology laboratory health record systems and standards, as well as cancer registry. Business analysts and policy managers can also benefit from a basic understanding of the use of this cancer pathology data standard to support data flows from pathology laboratories.

### Acknowledgements
This library of FHIR resources was developed and produced through the efforts of Health Level Seven (HL7).

This library of FHIR resources was developed and produced through the efforts of Health Level Seven (HL7). The editors appreciate the support of all volunteers and staff associated with the creation of this document and the sponsorship of the following Work Groups: Orders & Observations, Vocabulary Work Group, Clinical Quality Information, Clinical Interoperability Council, Public Health, and Structured Documents. This guide would not have been possible without the support of the following organizations:
* Centers for Disease Control and Prevention (CDC)
* North American Association of Central Cancer Registries (NAACCR)
* College of American Pathologists (CAP)
* Service-Oriented Architecture (SOA) Work Group
* Lantana Consulting Group

