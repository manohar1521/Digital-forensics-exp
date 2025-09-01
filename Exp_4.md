# Experiment 4 : Analyze Email Headers and Detect Email Spoofing using MHA (Mail Header Analyzer) 

## Aim
The aim is to analyze an email header to detect email spoofing using a specialized tool like MHA (Mail Header Analyzer). By examining the header, we'll identify inconsistencies that reveal the email was sent from a source other than the one it claims to be from.

## Description
Email headers contain a wealth of metadata, including the sender's real email address, the servers the message passed through, and authentication results from protocols like SPF, DKIM, and DMARC. Email spoofing exploits the fact that the "From" address shown to the recipient can be easily faked. This experiment uses an online tool to parse and present this complex header data in a human-readable format, allowing for quick analysis and detection of a forged sender.

## Tools & Equipment
A computer or mobile device with an internet connection.

An email client (e.g., Gmail, Outlook, etc.) to access the email you want to analyze.

An MHA (Mail Header Analyzer) online tool, such as the one provided by Microsoft, MxToolbox, or similar services.

## Procedure
Retrieve the Email Header:

Open the suspicious email in your email client.

Locate the option to view the "original" message or "show details" to expose the full email header. The exact steps vary by client (e.g., in Gmail, it's under the three-dot menu; in Outlook, it's often in the message properties).

Copy the entire email header text. It's a block of technical information, often starting with "Received:" lines.

Paste into MHA:

Navigate to your chosen online Mail Header Analyzer tool.

Paste the copied header text into the designated input box.

Analyze the Results:

The analyzer will parse the header and display the results in a clean, easy-to-read format.

Focus on key fields for spoofing detection:

Received: This section shows the email's journey. Read from the bottom up to trace the email's true origin. The first "Received" line at the bottom shows the sending server's IP and domain. If this domain doesn't match the "From" address, it's a major red flag. 🚩

From: This is the visible sender address. Compare this to the Return-Path and Reply-To fields, which are harder to forge. If they don't match, the "From" address is likely spoofed.

Authentication-Results: Look for the results of SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail), and DMARC (Domain-based Message Authentication, Reporting & Conformance).

SPF: A "Fail" result means the sending server's IP address isn't authorized to send mail for the domain in the "From" address.

DKIM: A "Fail" result indicates the digital signature is invalid.

DMARC: This provides a policy on what to do if SPF or DKIM fail. A "Fail" result is a strong indicator of spoofing.

## Result Experiment
The result of this experiment is a clear determination of whether the analyzed email is spoofed. By cross-referencing the parsed header information, you will identify mismatches between the displayed sender (From address) and the email's true origin (as seen in the Received headers and authentication results). A "Fail" on SPF, DKIM, or DMARC, coupled with a mismatched Received or Return-Path domain, provides conclusive evidence of an email spoofing attempt.