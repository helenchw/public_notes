# Data Loss Protection

Data loss protection (DLP) is the policies to ensure data that are *in-use*, *at-rest*, or *in-transit*, within an organization is trackable and protected.
It is a combination of technology solutions and standardized organization practices (e.g., staff training, policy enforcement).
It is also referred to as "data leakage prevention" and "data loss prevention".
Below is the ideal DLP defined by IBM in a blog post.

> Ideally, an organization’s data loss prevention solution is able to monitor all data in use, in motion and at rest for the entire variety of software in use.

Hence, the high-level goals would be ensuring the following within an organization

- Identification sensitive data for protection
- Confidentiality and integrity of data
- Monitoring of data movement and access, e.g., via audit logs
- Timely anomaly detection of data movement and access

Typical sources of threats would be (i) extrusion by outsiders, (ii) insiders , and (iii) unintended exposure.

DLP solutions can be deployed at (i) networks, (ii) endpoints (e.g., end-user devices), and (iii) data stroage repositories, to enable anomaly detection, e.g., with the help of machine learning or artificial intelligence.

Below is an example table of what DLP solutions can be employed at the data storage repositories according to Huawei IP Encyclopedia.

|   | Storage-side DLP |
|---|---|
| Service requirements | Non-compliant storage audit, sensitive data asset distribution statistics, and sensitive file backup & isolation |
| Key technologies | Shared directory data discovery, nested data discovery, file type filtering, and offline file scanning |
| Deployment modes | Off-line deployment at storage devices |

In particular, public-facing generative AI solutions may also be a point of data loss/leakage, as the AI agent may disclose classified training data to users under unintended conditions.

## References

- Fortinet. "What Is Data Loss Prevention (DLP)?". Accessed on Jan 17, 2025. https://www.fortinet.com/resources/cyberglossary/dlp.
- Huawei. "What Is Data Loss Prevention (DLP)?". September 2021. https://info.support.huawei.com/info-finder/encyclopedia/en/DLP.html.
- IBM. "What is data loss prevention (DLP)?". August 2024. https://www.ibm.com/think/topics/data-loss-prevention.
- IBM. "What is data leakage?". September 2024. https://www.ibm.com/think/topics/data-leakage
