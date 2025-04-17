# Rapid Risk Assessment for DevOps Software Projects

## 1. General Project Information
- What is the name of the application or service?
- Who owns the application (team/contact)?
- What is the business purpose of the application?
- What environments does this application run in? (Dev, QA, Staging, Prod)
- What is the deployment frequency (daily, weekly, etc.)?
- What is the release cadence (manual or automated)?
- Who are the primary users (internal, external, partners)?

## 2. Data Classification and Sensitivity
- Does the application process or store sensitive data? (PII, PCI, PHI, secrets, etc.)
- What is the highest classification of data handled? (Public, Internal, Confidential, Restricted)
- Are there any data residency or compliance requirements (GDPR, HIPAA, etc.)?

## 3. Threat Modeling and Architecture
- Has a threat model been created for this application?
- Are trust boundaries and data flows documented?
- Are third-party services or APIs involved? If so, are they trusted?
- Are known attack vectors mitigated (e.g., OWASP Top 10)?
- Are legacy or unsupported components in use?

## 4. CI/CD Pipeline Security
- What CI/CD tools are used (GitLab CI, Jenkins, GitHub Actions, etc.)?
- Are builds and deployments fully automated?
- Are secrets stored securely (e.g., Vault, KMS, Secrets Manager)?
- Are CI/CD runners or agents hardened and isolated?
- Are SBOMs (Software Bill of Materials) generated and validated?
- Are build artifacts signed and verified before deployment?

## 5. Source Code Security
- Is source code managed in a secure version control system?
- Is multi-factor authentication (MFA) enforced for repository access?
- Are code reviews or merge approvals required?
- Is static application security testing (SAST) integrated into the pipeline?
- Are secrets scanned in code repositories?

## 6. Open Source & Dependency Management
- Are open-source dependencies used?
- Is software composition analysis (SCA) performed?
- Are vulnerabilities in dependencies tracked and patched regularly?
- Are transitive dependencies evaluated for risk?

## 7. Container and Image Security
- Are containers used in the build or runtime environment?
- Are base images sourced from trusted registries?
- Are images scanned for vulnerabilities before deployment?
- Are containers signed (e.g., using Cosign)?
- Is there a process to update and rebuild base images regularly?

## 8. Infrastructure and IaC
- Is infrastructure defined as code (e.g., Terraform, CloudFormation)?
- Is infrastructure code scanned for misconfigurations (Checkov, tfsec)?
- Are least privilege IAM roles enforced in cloud environments?
- Are environment variables or secrets exposed via IaC?

## 9. Runtime and Operations
- Is runtime monitoring in place for security events?
- Are logs collected, normalized, and retained?
- Is anomaly or intrusion detection configured?
- Are unauthorized changes in production flagged?
- Is egress traffic controlled and monitored?

## 10. Access Controls and Identity
- Is access to environments role-based and audited?
- Are developers restricted from accessing production systems?
- Are service accounts rotated and scoped with least privilege?
- Is single sign-on (SSO) and MFA implemented?

## 11. Vulnerability and Patch Management
- How often are vulnerabilities scanned in runtime environments?
- Is there a defined SLA for patching critical vulnerabilities?
- Are automated patching or notification systems used?

## 12. Incident Response and Recovery
- Is there an incident response plan in place?
- Are security alerts triaged and responded to in a timely manner?
- Is there an automated rollback mechanism for failed deployments?
- Are backups encrypted and regularly tested?

## 13. Compliance and Audit
- Are there internal or external compliance requirements?
- Is audit logging enabled across all environments?
- Are controls mapped to frameworks like NIST, ISO, CIS, or SOC 2?

## 14. AI/ML Usage (If Applicable)
- Does the application incorporate AI/ML models?
- Are training datasets validated for poisoning risks?
- Are AI model artifacts signed and versioned?
- Are there defenses against adversarial inputs or model extraction?

## 15. Emerging Risk Considerations
- Are risks from GenAI, LLMs, or shadow IT considered?
- Are developers trained on secure DevOps practices?
- Is there a supply chain risk management process in place?

---

**Date of Assessment:** YYYY-MM-DD  
**Conducted By:** [Assessor Name / Team]  
**Review Frequency:** [e.g., Quarterly, Per Release]
