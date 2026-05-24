# MFA Phishing Resistance Lab

## About

This project analyzes the phishing resistance of common multi-factor authentication (MFA) methods under adversarial-in-the-middle (AiTM) attack scenarios.
This lab compares:
  - SMS- One-Time passwords (OTP)
  - HMAC-Based One-Time Passwords (HOTP)
  - WebAuthn

This project includes:
  - A django-based authentication system
  - Simulated phishing infrastructure
  - Controlled phishing attack testing
  - Comparative security analysis

# 3. Research Question

How do SMS-based OTP, HOTP and WebAuthn differ in resistance to phishing and adversary-in-the-middle attacks under modern web threat models?

# 4. Technologies Used
- Python
- Django
- HTML/CSS
- pyotp
- Python cryptography library
- WebAuthn concepts
- Session management
- Authentication systems
- Security testing

# 5. Project Architecture


# 6. Attack Simulation Section

## Simulated Phishing Environment

A phishing site was developed to impersonate the legitimate authentication system.

Attack scenarios included:
- Immediate credential relay
- delayed OTP relay
- Credential interception
- WebAuthn phishing attempts

The phishing site captured:
- Username and password pairs
- OTP submissions
- Authentication timing behavior


Full results in attacks-simulation.md and methodology.md

# 7. Results Table
After 30 attempts with each method:

   | Method | 0s Delay | 30s Delay | 60s Delay |
   |---|---|---|---|
   | SMS OTP | ~97% | ~73% | 0% |
   | HOTP | 97% | 77% | 53% |
   | WebAuthn | 0% | 0% | 0% |

# 8. Key Findings
- SMS OTP was highly vulnerable to real-time phishing attacks but was secure past a certain time period (60s) due to expiration
- HOTP remained vulnerable due to reuseable counter-based authentication (No expiration time)
- WebAuthn resisted all phishing attempts
- Origin binding prevented authentication on fake domains
- Asymmetric cryptography eliminateed credential replay

# 9. Why WebAuthn Won
## Why WebAuthn Was Resistant

WebAuthn uses:
- assymetric cryptographic
- origin binding
- browser-enforce authentication
- non-exportable private keys

Unlike OTP systems, no reusable credentials are transmitted or manually entered by the user.

# 11. Setup Instructions
Screenshot of setup

