# Threat Model

## Assets Protected
- Authentication credentials
- User account
- Administrative dashboard access

## 2. Attacker Goals
- Steal credentials
- Bypass MFA
- Gain unauthorized access

## 3. Attacker Capabilities
- Create phishing websites
- Capture credentials
- Relay authentication requests
- Replay OTP codes

## 4. Assumptions
- Legitimate website is uncompromised
- Users may fall for phishing
- Attackers cannot break modern cryptography

## 5. Attack Scenarios
### SMS-OTP
### HOTP
### WebAuthn

## 6. Out of Scope
- Malware Infections
- Full device compromise
- Insider threats
