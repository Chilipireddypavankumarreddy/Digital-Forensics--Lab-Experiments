# Experiment No. 4: Analyze Email Headers and Detect Email Spoofing Using MHA

## Aim

To analyze an email header using Mail Header Analyzer (MHA) and detect possible email spoofing by examining email routing information and authentication results.

## Requirements

* Gmail / Outlook / Yahoo Mail
* Mail Header Analyzer (MHA)
* Web browser
* WHOIS / IP lookup tool
* Internet connection

## Procedure

### Step 1: Access the Email Header

**Gmail:**

1. Open the email.
2. Click the three-dot menu in the upper-right corner.
3. Select **Show original**.

**Outlook:**

1. Open the email.
2. Click **File**.
3. Select **Properties**.
4. Locate the **Internet headers** section.

**Yahoo:**

1. Open the email.
2. Click the three-dot menu.
3. Select **View raw message**.

<img width="1217" height="513" alt="Screenshot 2026-09-25 202556" src="https://github.com/user-attachments/assets/6298d639-c59e-4d77-99ff-54f6f67dae17" />

### Step 2: Copy the Email Header

Copy the complete email header displayed by the email service.

<img width="1916" height="627" alt="image" src="https://github.com/user-attachments/assets/c0ffb7cd-6d39-474a-9edc-f92a3b403db5" />

### Step 3: Analyze the Header Using MHA

1. Open Mail Header Analyzer.
2. Paste the copied email header into the analyzer.
3. Submit the header for analysis.
4. Examine the parsed header information.
5. Identify the `From`, `To`, `Return-Path`, `Received`, and `Message-ID` fields.
6. Check the SPF, DKIM, and DMARC authentication results.

### Step 4: Analyze the Received Fields

Examine the `Received` fields to determine:

* Sending server hostname
* Sending server IP address
* Receiving server
* Date and time of transmission
* Sequence of mail servers

The `Received` headers should be analyzed from the **bottom upward** to trace the email's path.

<img width="1917" height="505" alt="image" src="https://github.com/user-attachments/assets/a9966ad8-3511-47a9-8e65-0423608f638d" />

### Step 5: Check IP Addresses and Hostnames

Use an IP lookup or WHOIS tool to check the IP addresses found in the `Received` headers.

Verify whether:

* The IP belongs to the expected mail server.
* The hostname matches the IP address.
* The sending server appears legitimate.
* Any unexpected server or IP address is present.

### Step 6: Check SPF, DKIM, and DMARC

Record the authentication results.

| Check | Result    | Observation                                |
| ----- | --------- | ------------------------------------------ |
| SPF   | PASS/FAIL | Check whether the sending IP is authorized |
| DKIM  | PASS/FAIL | Check whether the DKIM signature is valid  |
| DMARC | PASS/FAIL | Check domain authentication and alignment  |

<img width="1915" height="872" alt="image" src="https://github.com/user-attachments/assets/402c5221-09e8-42c3-906b-7ab9890abff5" />
<img width="1917" height="718" alt="image" src="https://github.com/user-attachments/assets/0c6dac7f-d237-41c6-be82-62e08f7d6fbf" />

### Step 7: Analyze Message-ID

Check the domain used in the `Message-ID` and compare it with the sender's domain.

<img width="1917" height="610" alt="image" src="https://github.com/user-attachments/assets/cc789c4c-bb1a-4094-ba32-ba5625430d3e" />


### Step 8: Identify Possible Spoofing Indicators

Check for:

* `From` and `Return-Path` domain mismatch
* Suspicious IP addresses
* Unexpected hostnames
* SPF failure
* DKIM failure
* DMARC failure
* Unusual timestamps
* Inconsistent mail-server routing
* Suspicious Message-ID domain
  
<img width="1917" height="388" alt="image" src="https://github.com/user-attachments/assets/123e5419-fa15-4a96-8fe2-20acbf8e548d" />


## Observation

The email header was successfully parsed using MHA. The sender information, mail-server path, IP address, Message-ID, and email authentication results were examined for inconsistencies.

## Result

The email header was successfully analyzed using Mail Header Analyzer, and possible email spoofing indicators were identified by examining the **Received, Return-Path, Message-ID, SPF, DKIM, and DMARC** fields.

## Conclusion

Email header analysis using MHA can be used to trace the email's delivery path and identify inconsistencies that may indicate email spoofing or phishing.
