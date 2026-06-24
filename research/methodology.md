# Methodology

## Overview

This research evaluates the phishing resistance of 3 Multi-Factor Authentication (MFA) Protocols:
- SMS-OTP
- Hmac-OTP (HOTP)
- WebAuthn

A controlled phishing environment was developed using a Django-based ticketing application and a phishing clone version designed to simulate an adversary in the middle (AiTM) attack.

## Research Objective

The objective of this experiment was to compare how different MFA systems perform against phishing and adversary-in-the-middle attacks under controlled testing environments.

The study focused on:
- Phishing Resistance
- Replay Attack Resistance
- Credential Interception
- Origin Binding
- Authentication Architecture

## Authentication Methods Evaluated

### SMS-OTP
Server-generated one time passwords that are delivered via text message after successful username/password authentication

### HOTP
Counter-based HMAC one-time password system using shared secrets between the client and the server (ever request moves the counter, which combines with the shared secret to produce a new code)

### WebAuthn
Public-key authentication system using origin-bound asymmetric cryptography and browse-enforced verification

## Experimental Environment
Testing was performed using:
- Python
- Django
- Localhost web applications
- Simulated phishing domains
- OTP authentication workflows
- WebAuthn credential registration/login flows

The experiment used a custom-built cybersecurity ticketing system with MFA-enabled authentication

## Phishing Design Simulation
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
