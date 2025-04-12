# Peer Test 05/11/2025
## Kate Hill and Dylan Shuldberg

## Self Attack
### Kate:
| Item | Result|
| --- | --- |
| Date | April 10, 2025 |
| Target | pizza.rundiary.click |
| Classification | Security Misconfiguartion |
| Severity | 2 |
| Description | Default admin login still in use. Gained admin access. |
| Image | ![attack 1](attack1.png) |
| Corrections | Remove default users, add new admin with secure login. |

| Item | Result|
| --- | --- |
| Date | April 10, 2025 |
| Target | pizza.rundiary.click |
| Classification | Injection |
| Severity | 1 |
| Description | SQL injection changed all users to have new username and password. Gained admin access and all accounts are unusable. |
| Image | ![attack 2](attack2.png) |
| Corrections | Parameterize SQL statement to update user. |

### Dylan:

## Peer Attack
### Kate attack on Dylan:
| Item | Result|
| --- | --- |
| Date | April 11, 2025 |
| Target | pizza.shuldberg.click |
| Classification | Security Misconfiguartion |
| Severity | None |
| Description | Attempted default admin login, not recognized. |
| Image | ![attack 3](attack3.png) |
| Corrections | None |

| Item | Result|
| --- | --- |
| Date | April 11, 2025 |
| Target | pizza.shuldberg.click |
| Classification | Injection |
| Severity | None |
| Description | SQL injection attempted but safeguarded against. |
| Image | ![attack 4](attack4.png) |
| Corrections | None |

### Dylan attack on Kate:

## Summary
We both found and protected against the vulnerabilites of the default admin login and SQL exploit in the updateUser endpoint. Through self-testing and fixing these vulnerabilities on our own applications, we learned to protect admin login credentials and the power of parameterized inputs for SQL statements.  
As we tested each other's applications, we were not able to penetrate either application in a significant way because we had both found and fixed the same vulnerabilites.