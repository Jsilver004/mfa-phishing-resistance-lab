# Methodology

## 1. Overview

This research evaluates the phishing resistance of 3 Multi-Factor Authentication (MFA) Protocols:
- SMS-OTP
- HMAC-OTP (HOTP)
- WebAuthn

A controlled phishing environment was developed using a Django-based ticketing application and a phishing clone version designed to simulate an adversary in the middle (AiTM) attack.

## 2. Research Objective

The objective of this experiment was to compare how different MFA systems perform against phishing and adversary-in-the-middle attacks under controlled testing environments.

The study focused on:
- Phishing Resistance
- Replay Attack Resistance
- Credential Interception
- Origin Binding
- Authentication Architecture

## 3. Authentication Methods Evaluated

### SMS-OTP
Server-generated one time passwords that are delivered via text message after successful username/password authentication

### HOTP
Counter-based HMAC one-time password system using shared secrets between the client and the server (ever request moves the counter, which combines with the shared secret to produce a new code)

### WebAuthn
Public-key authentication system using origin-bound asymmetric cryptography and browse-enforced verification

## 4. Experimental Environment
Testing was performed using:
- Python
- Django
- Localhost web applications
- Simulated phishing domains
- OTP authentication workflows
- WebAuthn credential registration/login flows

The experiment used a custom-built cybersecurity ticketing system with MFA-enabled authentication

## 5. Phishing Design Simulation
A phishing site was created to imitate the legitimate authentication portal.

The phishing workflow simulated:
1. Credential harvesting
2. OTP interception
3. Authentication replay
4. Delayed replay attacks

The phishing site collected:
- usernames
- passwords
- OTP submissions

## 6. Attack Workflow
### Step 0: The Real Site

![VLAN Creation](../screenshots/Images/Ip-Routing.png)

### Step 1: Victim Accesses Phishing Site

### Step 2: Credentials Captured

### Step 3: OTP Requested From Legitimate Site

### Step 4: OTP Relay Attack

### Step 5: Authentication Outcome

## 7. Testing Procedure

Each authentication protocol was tested under multiple delay conditions:
- Immediate Attack (0 seconds)
- Small Delayed Attack (30 seconds)
- Large Delayed Attack (60 seconds)

Each scenario was tested repeatedly to measure:
- Successful phishing attempts
- replay feasibility
- authentication failure conditions

## 8. Evaluation Criteria
Authentication methods were evaluated using the following criteria:
- Phishing/AITM resistance
- Credential Capture Replay resistance
- Successful/Failure rate of an attack

## 9. Data Collection
Attack success rates were recorded for each authentication method under each delay condition.

Results were measured by:
- Success/Failure rate of phishing attempts
- Success/Failure authentication attempts
- Replay Attack rate

## 10. Limitations
This experiment was conducted in a controlled lab environment using a limited number of authentication trials (30 each).

This research did NOT account for:
- Large scale user behavior
- demographic factors
- advanced phishing frameworks
- endpoint compromise scenarios

## 11. Ethical Considerations
This project was conducted strictly for educational and defensive cybersecurity research purposes.

All phishing simulations were performed in a controlled local environment with no real users or external systems involved.

# FURTHER ANALYSIS WILL BE IN results.md

