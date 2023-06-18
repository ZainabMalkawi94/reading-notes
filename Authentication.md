## Authentication
### Securing Passwords

- Explain to a non-technical friend how you would safely hash and store a password.

    To safely hash and store a password:

    1. Choose a strong hash function like bcrypt or Argon2.
    2. Hash the password using the chosen function before storing it.
    3. Store only the hashed password; never store the actual password in any form.


- What is Bcrypt?

    Bcrypt is a widely-used password hashing algorithm:

   1.  It incorporates a salt and multiple iterations to enhance security.
   2. It is designed to be slow and computationally expensive, making it resistant to brute-force attacks.
   3. Bcrypt is commonly used in applications to securely store passwords.


- Why might you use something like Bcrypt?

    Bcrypt is used for password hashing due to its key advantages:

    1. It provides a high level of security by incorporating salts and multiple iterations, making it difficult for attackers to reverse-engineer passwords.
    2. Bcrypt is computationally expensive, slowing down brute-force attacks and making them less feasible.
    3. By using bcrypt, organizations can enhance the protection of user passwords and reduce the risk of unauthorized access in case of a data breach.


---


### Basic Auth

- What is Basic Authentication?

    Basic Authentication is a simple authentication scheme:

    1. It involves sending credentials (username and password) in plain text with each request to authenticate users.
    2. However, it is considered less secure as the credentials can be easily intercepted and compromised if transmitted over an insecure network.




- What properties are necessary in the header of a Basic Auth request?

    The header of a Basic Auth request requires specific properties:

    1. The "Authorization" header field, indicating the use of Basic Authentication.
    2. The word "Basic" followed by a space.
    3. Base64 encoding of the username and password in the format "username:password".




- How are username:password in Basic Auth encoded?


    In Basic Authentication, the username:password combination is encoded using Base64 encoding:

    1. The username and password are concatenated with a colon (e.g., "username:password").
    2. The resulting string is encoded using Base64 encoding.
    3. The encoded string is then included in the "Authorization" header as "Basic [encoded_string]".
---
### OWASP auth cheatsheet
- Define the authentication process to a non-technical recruiter.

    The authentication process verifies the identity of users applying for a job:

    1. Users provide their username and password during login.
    2. The system securely stores the password using a hashing algorithm.
    3. When a user attempts to log in, the system hashes the entered password and compares it with the stored hashed password.
    4. If the hashes match, the user is authenticated and granted access to the system.
    5. This process ensures only authorized individuals can access job-related resources and protects against unauthorized access.


- How should your error messaging respond (both HTTP and HTML)? Why?


    In authentication, error messaging should be handled carefully to balance security and user experience:

    1. For HTTP responses, it's important to use generic error messages without revealing specific details about the authentication failure (e.g., "Invalid username or password"). This helps prevent potential attackers from gaining insights into the authentication system.
    2. In HTML, error messages should provide user-friendly feedback, highlighting the specific issue encountered (e.g., "Incorrect username or password"). This helps users understand and troubleshoot their login problems more effectively.

    By following this approach, you maintain security by not exposing sensitive information in HTTP responses while still providing meaningful feedback to users in the HTML interface.


- Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.

        https://www.npmjs.com/package/bcrypt




----------------------
return to [Main Reading File](./README.md)
