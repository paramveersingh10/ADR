-----
**Architectural Decisions**

**Prepared By** 

**paramveer Singh**

**Requested By**

**Nick Hamnett, Instructor,**

**SAIT (Southern Alberta Institute of Technology)**

**10 October 2023**

**ADR 1: Mobile Application Type**

**Title:**

Choice of Application Development Approach

**Status:**

Accepted

**Context:**

To ensure a seamless user experience and widespread adoption across both iOS and Android users within the university, a development approach must be chosen that caters to both platforms efficiently.

**Decision:**

**We will Create a Hybrid App. They possess the capability to utilize device functionalities and provide an user experience across platforms.**

**Consequences:**

- **Easier**:
  - Development speed is faster due to a unified codebase.
  - Immediate updates can be pushed to both platforms simultaneously.
- **More Difficult**:
  - Addressing platform-specific quirks or optimizing performance may sometimes require added effort or platform-specific code.
-----
**ADR 2: UI Framework**

**Title:**

Selection of Cross-Platform UI Framework

**Status:**

Accepted

**Context:**

The ideal UI framework should offer tools to create intuitive, responsive, and native-like interfaces for both Android and iOS without the need to write platform-specific code.

**Decision:**

Adopt **Flutter**. Flutter, backed by Google, allows developers to create natively compiled applications for mobile from a single codebase. It's based on the Dart language and provides its own widgets that guarantee consistent behavior across platforms.

**Consequences:**

- **Easier**:
  - Rapid prototyping with hot-reload.
  - High-quality UIs with a comprehensive widget set.
- **More Difficult**:
  - The team may need training if unfamiliar with Dart.
-----
**ADR 3: Backend Language**

**Title:**

Backend Development Language

**Status:**

Accepted

**Context:**

The backend should be robust enough to handle potentially thousands of simultaneous connections, efficiently serve data, and process real-time updates.

**Decision:**

opt for **Node.js**. It's a runtime that lets you run JavaScript on the server-side. With its non-blocking I/O model, it's efficient and lightweight, making it perfect for data-intensive real-time apps.

**Consequences:**

- **Easier**:
  - Integration with a vast npm ecosystem.
  - Supports WebSocket’s for real-time communication.
- **More Difficult**:
  - Ensuring proper structuring to maintain performance during peak loads.
-----
**ADR 4: Authentication and Permissions**

**Title:**

User Authentication Mechanism

**Status:**

Accepted

**Context:**

Ensuring only authorized individuals can access the app, and once inside, can only access features and data they're permitted to.

**Decision:**

**Integrate with the Active Directory system. It offers mechanisms, for authentication and authorization as a framework, for other associated services.**

**Consequences:**

- **Easier**:
  - Seamless integration with university's existing IT infrastructure.
  - Robust and tested role-based access management.
- **More Difficult**:
  - Addressing potential synchronization issues between AD and the app.
-----
**ADR 5: Data Storage**

**Title:**

Database Selection for App Data

**Status:**

Accepted

**Context:**

Storing data in a way that it's easily retrievable, scalable, and ensures the security and privacy of sensitive information.

**Decision:**

Adopt **MongoDB**. It's a NoSQL database, meaning it doesn't use the traditional table-based relational database structure. This makes it more flexible and scalable. Data is stored in flexible JSON-like documents.

**Consequences:**

- **Easier**:
  - Dynamic schema accommodating diverse data types.
  - Horizontal scalability by sharding.
- **More Difficult**:
  - Ensuring ACID transactions for critical operations, given MongoDB's eventual consistency model in distributed settings.

