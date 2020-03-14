* __Describe what constitutes a security architecture and give some examples.__
    
    A mix of text and graphics describing a system and the realtions between different parts of it.
* __The Sherwood Applied Business Security Architecture (SABSA) consist of 5 layers and one cross layer.__
    * __Describe the different layer views and list the names of the different layers.__
        1. Business view -> Contextual Security Architecture.
            * What? - The business needs the purpose of the system.
            * Why? - The risks and threats we would like to mitigate.
            * How? - The processes in the system that needs protection.
            * Who? - The stakeholders of the subject system.
            * Wher? - The geographical topology of the system or use of the product.
            * When? - The business running hours of the system and uptime requirements etc.
        2. Architect's view -> Conceptual Security Architecture.
            * What? - The business to be protected.
            * Why? - The risks to be mitigated and the assets that needs protection.
            * How? - Protection in terms of high-level technical and management security strategies.
            * Who? - People or organizations involved in the security management and assumed trust relationships etc..
            * Wher? - Where the protection is needed in terms of security domains.
            * When? - The relevant time scope or scopes of the protection.
        3. Designer's view -> Logical Security Architexture.
            * What? - Description of the actual information to be secured.
            * Why? - The security policy that shall apply to the system.
            * How? - The actual security services (entity authentication, confidentiality protection, integrity protection etc.) in the system and how they fit together.
            * Who? - The entities (users, security administrators, auditors etc.) and their interrelationships.
            * Wher? - The security domains and inter-domain relationships (logical security domains, physical security domains, security associations).
            * When? - The security processing cycle (registration, certifications, login, session management etc.)
        4. Builder's view -> Physical Security Architecture.
            * What? - The data model and security-related data structures (tables, messages, pointers, certificates, signatures etc.).
            * Why? - Rules that drive logical decisions-making within the system.
            * How? - Security mechanisms (encryption, access control, digital signatures, virus scanning etc.) and the physical machines or modules.
            * Who? - The users, the applications that they use and the security interface.
            * Wher? - Security technology infrastructure (physical layout of the hardware, software and the communication lines).
            * When? - The time dependency in the form of execution control structures (sequences, events, lifetimes and time intervals).
        5. Tradesmans's view -> Component Security Architecture.
            * What? - Data field specifications, address specifications and similar.
            * Why? - Security standards and best practice.
            * How? - Entities/modules and tools (both hardware and software).
            * Who? - User identities, privileges, functions, actions and access control lists (ACLs).
            * Wher? - Computer processes, node addresses, and inter-process protocols.
            * When? - Security step timings and sequencing.
        6. Operator's view -> Security Service Management Architecture (Spanning over all the others).
            * What? - Ensuring the operational continuity of the system and information processing.
            * Why? - Minimize operational risks and mitigate failures and disruptions.
            * How? - Performing specialized security-related operations (user security administration, system security administration, data back-ups, security monitoring,
emergency response procedures, etc.).
            * Who? - Support to all users and their applications.
            * Wher? - Maintaining the system integrity and security on all platforms/components and networks.
            * When? - Scheduling and executing a timetable of security-related operations.
    * __Give examples of questions the different SABSA architecture views are supposed to answer__
        
        See above.
* __Which are the three different types of security services in a logical security architecture?__

    Logical functions, relations and information flows.
    * __List and explain examples of services part of the non-prevention type of security services.__
        1. Detection and Notificaiton.
        2. Recovery and Restoration.
* __Describe each of the different prevention security services in more details.__
    * __Give example of at least four different entity security services and how they contribute to security prevention.__

        Entity security is about securing each entity (component / asset) of the system.
        1. Entity unique naming.
        2. Entity registration.
        3. Entity public key certification.
        4. Entity credentials certificaiton.
        5. Directory service.
        6. Entity authorization.
        7. User authentication.
        8. Device authentication.
    * __Give example of at least four different communication security services and how they contribute to security prevention.__

        Communication security is about securing the communication between different entities.
        1. Session authentication.
        2. Message origin authenticatin.
        3. Message integrity protection.
        4. Message content confidentiality.
        5. Non repudiaiton.
        6. Message reply protection.
        7. Traffic flow confidentiality.
        8. Security measure and metrics.
        9. Security administration.
        10. User support.
        11. Physical security services.
        12. Enviromental security services.
    * __Give example of at least four different application level security services and how they contribute to security prevention.__

        Application security is about security on the application layer, data storage etc.
        1. Entity authorization.
        2. Logical access control.
        3. Audit trails.
        4. Stored data integrity protection.
        5. Stored data confidentiality.
        6. Software integrity protection.
        7. Software licensing management.
        8. System configuration protection.
        9. Data replicaiton and backup.
        10. Trusted time.
        11. User interface for security.
    * __Give example of at least four security management services and how they contribute to security prevention.__

        Pretty self explanatory (Just like the other ones, just didn't know how to dumb this one out even).
        1. Security policy management.
        2. Security traning and awareness.
        3. Security operations management.
        4. Security provisioning.
        5. Security monitoring.
        6. Security measurements and metrics.
        7. Security administration.
        8. User support.
        9. Physical security services.
        10. Enviromental security services.
* ~~__Draw a picture showing the relations between major different security services from a systems point of view.__~~
* __A logical security architecture can be created using a six steps methodology:__
    1. Identify main entities.
    2. Identify major functions in the system.
    3. Identify security domains and associations.
    4. Identify security services meeting requirements.
    5. Map security services to the functional entities.
    6. Create a graphical view of the logical architecture.
    * ~~__Describe each of the different steps__~~
    * ~~__What is the end result?__~~
    * __Give an example of a logical security architecture__
        1. Movile network security architectures (3G, 4G, 5G).
            * Complex systems with several nodes where the SIM card and the corresponding subscriber register (HLR/HSS) unit are core components.
        2. Computer security architectures with security components such as ARM Trust Zone and Intel SGX.
        3. Enterprise network security architectures with firewalls, network zones, intrusion detection entities etc..
* __What is a physical security architecture?__

    The physical security architecture is the builder's view of the system. This will covers security mechanism including user and application security, as well as platform and network infrastructure security.
* __A physical security architecture when using the SABSA include making a mapping to physical security mechanisms__

    Description of these is pretty self-explanatory given the names. They are also very similiar to the security services specified above, but it bears repeating so maybe I'll remember them better.
    * __Describe what is meant by a "Naming and registration" mechanism and give examples__
        1. Unique naming.
        2. Entity registration.
        3. Public key certification.
        4. Directory service.
    * __Describe what is meant by a "Storage and runtime" mechanism and give examples__
        1. Data confidentiality.
        2. Data integrity.
        3. Software integrity.
        4. Secure execution.
        5. Software licensing protection.
        6. Data and software replication.
    * __Describe what is meant by a "Physical security" mechanism and give examples__
        1. Physical security.
        2. Enviromental security.
        3. Personnel security.
    * __Describe what is meant by an "Authentication and session" protection mechanism and give examples__
        * Entity authentication.
        * Session authentication.
        * Message integrity.
        * Message confidentiality.
        * Message reply protection.
        * Non-repudiation.
    * __Describe what is meant by a "User interface and management" mechanism and give examples__
        * User interface security.
        * Service management.
        * Operations management.
        * Secure provisioning.
        * Security administration.
    * __Describe what is meant by a "Authorization and access control" mechanism and give examples__
        * Authorization.
        * Logical access control.
        * Audit trails.
    * __Describe what is meant by a "Monitoring and incident" mechanism and give examples__
        1. Security monitoring.
        2. Security measurements and metrics.
        3. Alarm management.
        4. Intrusion detection.
        5. Incident response.
        6. Disaster recovery.
* __What must in addition to the security mechanisms be specified in the physical security architecture?__

    The platform and network assumed for the solution.
* __Give example of platform security solution that can be used to build solutions meeting a logical security services and can be used to protect the chosen physical security  mechanism?__

    Things like ARM Trust-Zone, Intel SGX, SIM Cards and trusted boot are platform security solutions to different security vulnerabilities.
* ~~__For the SSO logical security architecture given at the lecture, perform the following:__~~
    * ~~__Identify the main physical security mechanisms needed in the corresponding physical security architecture.__~~
    * ~~__Identify the main platform security components needed to fulfill the architecture__~~
        * ~~__Suggest concrete platform security mechanisms to use for the physical realization.__~~