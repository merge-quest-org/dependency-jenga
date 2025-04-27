# Welcome to Dependency Jenga 🧩

Your app runs... for now. But it's riddled with security vulnerabilities!

## The Challenge
This puzzle tests your ability to identify and fix security vulnerabilities in a Node.js application. The app uses outdated dependencies and contains several security flaws that need to be addressed.

## Vulnerabilities to Find and Fix

### Dependency Issues
- Express.js 4.10.0 (outdated with known vulnerabilities)
- Lodash 3.10.1 (outdated with known vulnerabilities)

### Security Vulnerabilities
1. **Prototype Pollution** (`/prototype-pollution`)
   - Lodash merge vulnerability
   - Allows modification of object prototypes

2. **Cross-Site Scripting (XSS)** (`/xss`)
   - Unsanitized user input
   - Express 4.10.0 doesn't escape by default

3. **Path Traversal** (`/file`)
   - Unrestricted file access
   - Potential directory traversal attacks

4. **Command Injection** (`/ping`)
   - Unsanitized command execution
   - Allows arbitrary command injection

5. **Authentication Issues** (`/login`)
   - Weak MD5 password hashing
   - SQL Injection vulnerability
   - String concatenation in queries

6. **Broken Access Control** (`/profile`)
   - No authorization checks
   - Horizontal privilege escalation
   - Sensitive data exposure

## How to Play
1. Clone this repository:
   ```bash
   git clone https://github.com/merge-quest-org/dependency-jenga.git
   cd dependency-jenga
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   npm start
   ```

4. Identify and fix all vulnerabilities:
   - Update outdated dependencies
   - Fix security issues in the code
   - Ensure all endpoints are secure

5. Submit your solution as a PR

## Testing Your Fixes
You can test your fixes by:
1. Running the server
2. Testing each endpoint
3. Using tools like `npm audit` to check dependencies
4. Verifying no security vulnerabilities remain

Good luck! May your dependencies be secure and your code be clean! 🚀