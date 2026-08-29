# LAB 2: FILE UPLOAD AND COMMAND EXECUTION
# ANALYSIS QUESTIONS ANSWERS

Question 1: Why is browser-only upload validation insufficient?
Browser-only validation is insufficient because it can be bypassed using proxy tools (Burp Suite, OWASP ZAP) to modify or remove client-side checks. Since the browser is controlled by the client, it cannot be trusted. Server-side validation is the only reliable defense.

Evidence: E-12 - Mutillidae accepted a .php file with no server-side validation.

Question 2: What proves that command input was treated as executable structure rather than data?
The whoami command executed and returned www-data when input was 127.0.0.1; whoami. The semicolon (;) acts as a command separator, proving the input was passed to a shell interpreter for execution.

Evidence: E-14 - Mutillidae command injection showing www-data output.

Question 3: Why is minimal proof sufficient for both weaknesses?
Minimal proof is sufficient because it demonstrates the vulnerability exists without causing damage. Executing whoami proves command injection is possible without destructive commands. Uploading a harmless .php file proves validation is missing without deploying malware.

Evidence: E-12 (PHP upload) and E-14 (whoami output).

Question 4: Which control produced the greatest improvement in stronger mode?
Input sanitization in Mutillidae Secure Mode (Level 5) produced the greatest improvement. It blocked special characters (;, |, &, `) and prevented command injection entirely.

Evidence: E-15 - "Malicious characters are not allowed" message blocking the injection.
