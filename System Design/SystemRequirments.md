# Software Requirements Specification (SRS)

## 1. Introduction
**Purpose**:    
    This document specifies the requirements for the ElderAid software and hardware system, which is designed to provide a comprehensive solution for elderly care and support. 
**Scope**:  
    The system will read information form multiple sensory devices then depending on certain logic stored in the microprocessor, it issues actions to help and support the elderly person in moments of need.   
**Definitions, Acronyms, and Abbreviations**:   
    CRM - Customer Relationship Management. 
**References**: 
    [Link to related document]  
**Overview**:   
    This document includes the overall description, specific requirements, and appendices.  

## 2. Overall Description
**Product Perspective**:    
    The elderAid system consist of a sensory device portable by the user which monitors it's state, wirelessly connected to a microprocessor unit, that can send for aid i cases of need.   
**Product Functions**:  
    track the movements of user, monitor sound and emergency click, send for help from the caretaker, call emergency services.  
**User Characteristics**:   
    elderly people, people with special-needs.  
**Constraints**:    
    must use microprocessor.    
**Assumptions and Dependencies**:   
    ---

## 3. Specific Requirements
### Functional Requirements
**Use Case 1**: read motion of the user
- **Description**: the portable part of the system is constantly recording the mouvement of the user.
- **Steps**: read mouvement, if user wonders away from where he supposed to be notify care taker, if user drops on the floor contact emergency services and notify care taker, if user not moving for a prolonged time notify care taker.
- **Acceptance Criteria**: Successful movement identification read an abnormal behavious of the user the sends for help.

**Use Case 2**: read the sound of user
- **Description**:the portable part of the system is constantly recording the sound of the user.
- **Steps**: read sound trough microphone,if user is crying and weeping from pain or a stranger's voice notify caretaker.
- **Acceptance Criteria**: successful sound identification read abnormal sounds of user and notify caretaker.

**Use Case 3**: prompt emergency button
- **Description**:the portable part of the system contains a push button if clicked more than once overides the rest of the sensors an immediatly notify the caretaker and emergency services.
- **Steps**: button is pushed 2 or more time, declare emergency status and notify care takers.
- **Acceptance Criteria**: successful interpertation of clicks to send for help

**Use Case 2**: send SMS note
- **Description**:the control unit of the system sends notification via SMS.
- **Steps**: get user status, notify caretaker via SMS.
- **Acceptance Criteria**: recieved message at the caretaker phone.

**Use Case 2**: calling emergency services
- **Description**:the control unit of the system is able to issue an automatic voice call to emergency services.
- **Steps**: get user status, make phone call to emergency services.
- **Acceptance Criteria**: recieved call at the emergency phone line.

### Non-Functional Requirements
**Performance Requirements**: The system must be able to efficiently and quickly identify an emergency situation.
**Usability Requirements**: The system should be intuitive and easy to use, portability.
**Reliability Requirements**: System uptime must be 99.9%.

### External Interface Requirements
**User Interfaces**: ?
**Hardware Interfaces**: ?
**Software Interfaces**: ?
**Communication Interfaces**: ?


## 6. Appendices
**Appendix A**: Glossary of terms.
**Appendix B**: Data flow diagrams.
**Appendix C**: Sample data.

## 7. Index
- User login: 3.1
- Add new customer: 3.2
- Customer Data Management: 4.1
- Reporting: 4.2
