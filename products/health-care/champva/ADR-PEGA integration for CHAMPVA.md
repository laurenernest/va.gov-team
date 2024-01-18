
# Decision record - PEGA Integration for IVC Forms

## Status

Draft

## Context

Currently, the IVC forms team does not have an integration point for our pending forms. Our understanding is that PEGA will serve as a document management system for IVC indefinitely, and that some forms will be transmitted to VES (Veterans Enrollment System) in addition to PEGA. PEGA is expected to be prepared to accept form 10-10d and form 10-7959c in January of 2024. VES is not expected to be available to our team until workflows are built in 2025.

We're working to gather more details about how specifically we will submit forms and supporting documents to PEGA. This could involve a few different approaches:
1. Sending documents to an s3 bucket managed by the IVC Forms team. Risks include a large effort around document management that the team may not be equipped to bear, and an inability to provide a high confidence response back to applicants to give assurance that their documents have been received and are moving forward in the application process. 
2. Sending documents to an s3 bucket managed by IVC/PEGA. This would remove the IVC Forms team from ongoing document management (storage, retention, etc.) and provide higher confidence handoffs for confirmation of application receipt.
3. Sending documents directly to PEGA via an API. This would provide the highest confidence for successful submission. This option would also require additional effort from the PEGA team.

### What options were considered?

The benefits API was considered and has been ruled out due to a lack of business process integration between VBA (Veterans Benefits Administration) and VHA (Veterans Health Administration), along with the time, effort, and expense in building these integrations. The VHA currently doesn't use CMP (Central Mail Portal), which the VBA uses, and the estimate from the VBA to build an integration to handle forms like 10-10d was 3 months.

We also explored using an API to submit directly to VES, similar to the pattern used for forms like 10-10EZ that are also within VHA. If this were technically feasible, it would bypass multiple business processes (eligibility, claims, etc.) that need to remain intact to successfully serve CHAMPVA customers. Notably, some forms will never get sent to VES (even if the workflow went to VES, the documents would stay in PEGA). 

Box was ruled out early on due to security concerns.

## Decision

(The following assumes we will have the option to implement either option 2 or 3 above. As of this writing we don't consider option 1 viable.)

Moving forward, the IVC Forms team will:
- Proceed with the assumption that PDF form submissions will be sent to PEGA once a workflow becomes available for a given form
- Assume that there is a future state where form submissions will be sent to a RESTful API in addition to PEGA
- Remain open to changes in the architectural landscape that may help us and our stakeholders streamline IVC processes

## Consequences

### What are the risks of this decision?

### How do we reverse this decision?
