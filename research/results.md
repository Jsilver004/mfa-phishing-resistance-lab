# Results

## Overview
The objective of this experiment was to compare the phishing resistance of SMS-OTP, HOTP, and WebAuthn under simulated adversary-in-the-middle (AITM) attack conditions.

Testing was conducted using 0 second(immediate/0, 30 second and 60 second attack delays to evaluate if/how timing affected attack success rates.

---

## SMS-OTP 
SMS-OTP demonstrated high vulnerability to phishing attacks when the attackers acted quickly after credential capture.

   | Delay Before Attack | Success Rate |
   |---|---|
   | 0 Seconds | ~97% |
   | 30 Seconds | ~73% |
   | 60 Seconds | 0% |
