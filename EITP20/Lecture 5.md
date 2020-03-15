* __Can you list four different principles upon which a security design should be based?__
    1. Use well proven techniques.
        * Use available standard whenever possible.
        * Use well-known, proven open source libraries.
        * Use widely accepted hardware modules and solutions.
    2. Keep complexity as low as possible.
    3. Minimize utilization of trusted components.
    4. Only develop solutions when really needed.
        * When own solutions are used, use an entire team, not a job for a single engineer.
    5. Use open designs whenever possible.
    * ~~__Give a motivation for each of the listed design principles__~~
* __Describe the process steps to perform when going from a security architecture to a design specification__
    1. Map security services to security standards.
    2. Identify design gaps.
    3. Complement with new design where needed.
    4. New design security evaluation.
    5. Document the design.
    6. Identify impl. efforts.
* __What is typical the role of unique identities in security systems?__

    Unique identities can be used as a unique key and will allow reliable authentication.
    * __Give example of three different widely used identity types?__
        1. Country identifier.
        2. Operator / Company identifier.
        3. MAC Addresses.
        4. MObile Subscription Identification Number (MSIN)
        5. ISBN number for books.
* __What is the problem from privacy perspective with using fixed identities?__

    Knowing a unique identifier will let you more easily track what it belongs to.
    * __Describe two different methods for avoiding the identity privacy problem in a system design__
        1. Randomly generated pseudonyms.
        2. Encrypted identity not visible outside trusted container boundaries.
* __What is a digital certificate and how it is used?__

    A Digital Certificate is an electronic "password" that allows a person, organizaion to exchange data securely over the Internet using the public key infrastructure (PKI).
    * __Which are the most important data fields in an X.509 certificate?__
        1. Signature algorithm identifier.
        2. Period of validity.
        3. Subject's public key info.
        4. Signature.
* __Which is the far most used authentication principle over http?__

    Basic authentication.
    * ~~__Describe the different steps in an http basic authentication__~~
    * __Under which circumstances can basic authentication be used__

        It can only be used over TLS channels.
    * __How are typically basic authentication treated at the server side and what is the main reason for using this type of storage?__

        Stored using encryption __WITH__ salt, to protect similiar, or common, passwords in case of a data leak.
* __Describe the principles behind hardware token based authentication__

    Often used as a "second" factor together with password, can be in the form of OTPs or a challenge rresponse type like Bank ID.
* __What is the rationale behind two factor authentication?__

    Two is better than one.
* __What are the main differences between:__
    * __TLS server authentication__

    Here it's the server who authenticates itself.
    * __TLS client certificate authentication__

    Here it's the client who authenticates the connection with a certificate
    * __TLS pre-share key authentication__

    Here both authenticates themselfs with a shared key
* __Explain the main principle behind an object security scheme__

    For some use-cases, object security is more suitable than secure seesions as the data is protected at intermediate buffers and at storage.
    * ~~__How does it differs from a session protection scheme like TLS or IPsec?__~~
* __What does RBAC and ABAC stand for with respect to access control systems?__

    **A**ttribute based vs **R**ole based.
    * __Explain the main differences between RBAC and ABAC__
* __What is the purpose with an access token?__

    Carry important information ot resource servers.
    * __What does a SAML assertion contain?__
        * Assertion ID.
        * Major version.
        * Minor version.
        * IssueInstant(?).
        * Issuer.
        * Conditions:
            * NotBefore.
            * NotOnOrAfter.
            * Audience Restriction.
        * Authentication statement:
            * Subject.
            * Authenticaiton instant.
            * Authentication mechanism.
        * Attribute statement:
            * Subject.
            * Asserted attributes.
        * __Digital signature__
* __How can a Hardware Security Module (HSM) assist in protection of cloud data storage?__

    The user's secret key never leaves the HSM, while the encrypted version of the secret key is retained outside the HSM by the user and is an index to the actual secret key in the HSM.
* __List a couple of widely used commercial server anti-virus tools__
    1. Bitdefender.
    2. Comodo.
    3. Avire.
    4. Kaspersky.
* __How can the security of a Docker container be enhanced beyond using default configurations?__

    By the use of AppArmor.
* __How can a Web design be made to make "clickjacking" less likely?__

    W3C UISecurity and wsc-ui.
* ~~__What is the main difference between key provisioning of a public key system compare to a symmetric key-based systems?__~~
    * ~~__What are the key issues to consider when making a public key issuing design?__~~
    * ~~__Which are the key issues to consider when making a symmetric key issuing design?__~~
* __List the three main different intrusion detection principles and explain how they work on high level__
    1. Signature based detection.
    2. Statistical anomaly-based detection.
    3. Stateful protocol analysis detection.
* __What is syslog and how is it typically used?__

    Loggin system messages.
* __What is the main risks with a debug interface (like JTAG) and how should it be treated in a product design to avoid these risks?__

    It should only be enabled within testing enviroments to prevent malicious usage.
* __Which are the three different most severe attacks threats against smart card designs and which are the typical countermeasures?__


* __Give three examples of widely used NIST security standards and what they specify?__
    1. FIPS crypto standards.
    2. Special Publications series.
    3. NISTIR (Interagancy or internal).
* __What does IETF stand for?__

    **I**nternet **E**ngineering **T**ask **F**orce.
    * __Give example of two well-knows IETF security standards and explain what they specify?__
        1. Pure protocols.
        2. Services and formats.
* __Which type of security standards are done by IEEE and 3GPP respectively?__
    * IEEE - Wireless systems.
    * 3GPP - 3G, 4G, 5G.
* ~~__What is the difference between public industry bodies and industry standards?__~~
* __What is meant by a cancellable biometric protection scheme?__

    Cancelable biometrics refers to the intentional and systematically repeatable distortion of biometric features in order to protect sensitive user-specific data.
    * ~~__Describe how to achieve a cancellable biometric matching system__~~
    * ~~__Which alternative biometrics protection approaches can be used?__~~