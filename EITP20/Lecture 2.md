## Lecture 2

* __List three different typical security threats to an IT system?__
    1. Spoofing.
    2. Tampering.
    3. Repudiation.
    4. Information Disclosure.
    5. Denial of Service.
    6. Elavation of Privilege.
* __What is the first step in an attack tree threat analysis process?__

    A attack tree threat analysis starts with a *good* system description.
* ~~__Make an attack tree based analysis of a BankID system__~~
* __List three well established threat assessment methodologies__
    1. Attack tree.
    2. Microsoft (STRIDE).
    3. MITRE (TARA).
* __Spell out the acronym STRIDE__

    __S__poofing __T__ampering __R__epudiation __I__nformation disclosure __D__enial of Service __E__levation of Privilege.
    * ~~__Explain the meaning of the six different concepts in STRIDE__~~        
    * ~~__Give examples of attacks for the six different concepts in STRIDE__~~
* __Which are the three basic steps in STRIDE?__
    1. Identify main entities in the system.
    2. Identify main entities interactions.
    3. Per entity, make STRIDE analysis on the following:
        * Process
        * External entity
        * Data flow
        * Data store
* __Which are the two main activities in a MITRE TARA security analysis__
    1. Perform CTSA and store the results in a TTP.
    2. Perform CRRA and store the results in a countermeasure catalogue.
    * __Which are the main input sources to these two analysis activities?__
        1. Common Attack Pattern Enumeration and Classification (CAPEC).
        2. Common Weakness Enumeration (CWE).
        3. Common Vulnerability Enumeration (CVE).
    * __The output of these two activities are stored in special databases. What is the name of these two databases?__
        1. Tactics, Techniques, and Procedures (TTP) catalogue.
        2. Countermeasure catalogue.
* __Describe briefly the different steps performed during a TARA CTSA__
    1. Establish assessment scope.
        * Identify the assets subject to the analysis, usually important components in the system, and give each an id.
        * Identify the range of TTP to be considered:
            * Limit the scope of the *type* of attacks that shall be considered in the system, i.e. cyber, physical, electronic, etc...
        * Identify the type of adversary that are considered in the analysis
            * Different type of adversaries can for instace be: external, internal, and trusted insiders.
    2. Identify candidate TTP.
        * Identify weaknesses and potential attacks are identified. MITRE offers three publicly available resources to identify candidates:
            1. Common Attack Pattern Enumeration and Classification (CAPEC).
                * Database describing different attacks including potential mitigations (allowing a common language and classification of attacks).
                * Most useful in an early design case!
            2. Common Weakness Enumeration (CWE).
                * Database describing software weakness (allowing a common language enumeration)
                * To be used when lots of the design has been settled!
            3. Common Vulnerability Enumeration (CVE).
                * Database of known software vulnerabilities (applicable to particular SW packages).
                * Useful once impl. choices already are made!
    3. Eliminate implausible TTPs.

        Initial list of TTP candidates is typically to wide, a process eliminating TTPs not applicable to the considered system is needed.
        Possible reason for exluding TTPs might be:
            * The target system does not include a component need for the TTP to apply, SQL injection requires an SQL database for example.
            * A system might already have gone through an assessment which eliminates possible TTPs etc.
    4. ~~Apply scoring model.~~
    5. ~~Construct the threat matrix.~~
* __Spell out the acronyms CAPEC, CWE and CVE__
    1. __C__ommon __A__ttack __P__attern __E__numeration and __C__lassification
    2. __C__ommon __W__eakness __E__numeration
    3. __C__ommon __V__ulnerability __E__numeration
    * __What does CAPEC contain and how it is used in a TARA analysis?__
        * Database describing different attacks including potential mitigations (allowing a common language and classification of attacks).
        * Most useful in an early design case!
    * __What does CWE contain and how it is used in a TARA analysis?__
        * Database describing software weakness (allowing a common language enumeration)
        * To be used when lots of the design has been settled!
    * __What does CVE contain and how it is used in a TARA analysis?__
        * Database of known software vulnerabilities (applicable to particular SW packages).
        * Useful once impl. choices already are made!
* __Describe briefly the different steps performed during a TARA CRRA__
    1. Selects which TTPs to mitigate.
        * Focus only on the highest scoring TTPs in the threat matrix.
        * Focus on the cyber assets that have the highest aggregated susceptibility (which might not be exacly those having the highest score in the matrix).
        * Focusing only on high value cyber assets.
        * etc...
    2. Identify plausible countermeasures.
        *  The MITRE CAPEC database is also a source for identifying potential countermeasures.
    3. Assess countermeasures merits.
        * Score countermeasures on things like the type of mitigation and effectiveness.
    4. ~~Identify an "optimal" countermeasure solution.~~
    5. Prepare recommendations.
        * The final recomendations is the actual requirements list and should include the following:
            1. The action, device, procedure or technique recommended, i.e., what countermeasure to apply.
            2. The reason the countermeasure is required, i.e., the TTPs that it mitigates.
            3. The implication or effect if the countermeasure is not applied, i.e., the potential impact to mission capability resulting from compromising asset.
* __Where can one find TTP mitigation solutions?__

    Countermeasures can for example be found in the MITRE CAPEC database.
* __Which are the four different mitigation types?__
    1. Neutralize.
    2. Detect.
    3. Limit.
    4. Recover.
* __Which are the steps used to obtain a final ranking table for countermeasures?__
    * Several different approaches for final selection are possible:
        * Atleast one highly effective countermeasure must be selected for each TPP.
        * Less effective countermeasures may be combined to satisfy the previous condition.
        * A detected countermeasure is required to TTPs that have no neatralize countermeasure.
    * Prepare a list of solutions together with the associated costs.
* ~~__How do one select final TARA recommendations based on a countermeasure ranking table?__~~
* __Which are the three mandatory parts of a TARA TTP recommendation?__
    1. The action, device, procedure or technique recommended, i.e., what countermeasure to apply.
    2. The reason the countermeasure is required, i.e., the TTPs that it mitigates.
    3. The implication or effect if the countermeasure is not applied, i.e., the potential impact to mission capability resulting from compromising asset.
* __Which are the different input sources to the security requirements derivation process?__
    1. Open source.
    2. Classified sources.
* __Which are the main outputs from the attack tree, the STRIDE and the TARA process respectively which are used to derive high-level security requirements?__
    * Attack tree gives you a look of high level attack goals, and possible vulnerabilities to achieve them.
    * STRIDE is meant to help people identify typical attacks on software systems, and will help identify key system elements which will lead to STRIDE tables as output.
    * TARA will give TTPs as output from CTSA, and also a threat matrix. CRRA will establish countermeasures and together output another matrix.
* __Give example of high level security requirements for a Bank ID system__
* __Give example of low level security requirements  for a Bank ID system__
* __Describe a four step approach for security requirements identification and documentation__
    1. Establish goals.
    2. Connect vulnerabilities to goals.
    3. Find countermeasures for vulnerabilities.
    4. Document and present your findings.