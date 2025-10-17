# File-Based Login System with OTP Verification

This Python program implements a **secure file-based user authentication system** that validates passwords, limits login attempts, and supports **password reset using OTP verification via Twilio SMS**.

---

## 🔐 Features

- User credentials (username, password, phone number) are stored in a **text file**.  
- **Login system** with limited password attempts (default 5).  
- **Forgot Password** feature with OTP sent to the user's registered mobile number using Twilio.  
- **Password reset** updates the credentials file automatically.  
- **Logging system** records:
  - Successful logins  
  - Failed attempts  
  - OTP sending status  
  - Password reset activity  

---


---

## ⚙️ How It Works

1. **Credentials File Format (`credentials.txt`):**


2. **Program Flow:**
- Prompts the user for a username.
- If valid, allows up to 5 password attempts.
- If the user forgets their password, they can request an OTP.
- OTP is sent using the Twilio API.
- On successful OTP entry, user can set a new password.

---

## 🧠 Key Functions

| Function | Description |
|-----------|-------------|
| `load_credentials()` | Loads user data from the credentials file. |
| `save_credentials()` | Updates and saves any changes back to the file. |
| `send_otp()` | Generates and sends a 6-digit OTP via Twilio SMS. |
| `reset_password()` | Allows the user to set a new password after OTP verification. |
| `validate()` | Handles login attempts and triggers password reset if needed. |

---



