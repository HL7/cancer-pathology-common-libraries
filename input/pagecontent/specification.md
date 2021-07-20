This IG is conformant to the base FHIR R4 specification.

### Actors
* Message bundle sender
* Message bundle receiver

### FHIR Paradigm Supported by This IG
* Messaging Bundle

### Resources and Profiles
#### Resource Profiles
This specification defines the following profiles:
* Pathology Bundle
* Pathology MessageHeader 
* Pathology DiagnosticReport 
* Pathology Specimen 
* Pathology NextOfKin 
* Pathology-Related PractitionerRoles 

#### Extensions
This implementation guide defines no new extensions.

### Claiming Conformance to This Specification
To claim conformance to this specification, servers SHALL:
* Be able to populate all profile data elements that have a minimum cardinality >= 1 and/or flagged as Must Support as defined by that profile’s StructureDefinition.
* Conform to this IG’s Server Capability Statement expectations for that profile’s type.

Details on profiles and extensions present in this specification are available on the [Artifact Index](artifacts.html#profiles) page.

### Must Support and Missing Data
Systems claiming to conform to a profile SHALL support the elements in a profile as defined below. This guide adopts the following definitions of MustSupport for all direct transactions between the Sending and Receiving Systems.

**All Sending Systems** Sending Systems are defined as Provider Systems and applications.
* As part of the sending of a Pathology Bundle, the Sender SHALL be capable of including all elements defined in the profiles that have a MustSupport flag and SHALL populate all elements with a MustSupport flag if the information exists.
* In situations where information on a particular data element is not present, the Sender SHALL NOT include the data element in the resource instance if the cardinality is 0..n.
* If the information does not exist and the cardinality of the element is >= 1..*, the Sender SHALL use the dataAbsentReason extension where it is defined. **Note: **populating the element with the value set absent reason or using the dataAbsent Reason SHOULD be handled by the Sending System and not require provider action.

**All Receiving Systems** Receiving Systems are defined as Provider Systems and applications receiving transactions from the Sending System.
* The Receiving System SHALL be capable of processing resource instances containing required and allowed data elements without generating an error or causing the application to fail.
* Receiving Systems SHOULD be capable of processing (display, store, etc.) the data elements based on the utility of the specific element to the receiver.
* When receiving a Pathology Bundle from the Sender, the Receiving System SHALL interpret missing data elements within resource instances as data not present in the Sending System.
* Receiving Systems SHALL be able to process resource instances containing data elements asserting missing information without generating an error or causing the application to fail.

### Privacy and Security
Systems implementing this guide are expected to follow the general [FHIR Security](https://www.hl7.org/fhir/security.html) guidelines, as well as all additionally applicable public and private laws and policies. 
