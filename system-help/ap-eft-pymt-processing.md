---
title: "Electronic Payments and Verification (EFT)"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Electronic Payments and Verification (EFT)"
long_description: "This topic provides detailed information about Electronic Payments and Verification (EFT) in the 4GL system."
---


Electronic Payments and Verification (EFT)
==========================================

provides connection with third-party vendors that allow transactions for electronic bill payment (Electronic Funds Transfer, or EFT). Instead of printing a check,  creates a file that is uploaded to your bank. Your bank then processes the payment directly into the vendor's bank account, and  emails a statement to the vendor.

The Check Verification process involves loading the details of the check sent to the vendor. When the check is cashed the bank matches the details and provides information regarding the match.

Batch-based processing provided by the vendor allows for cheaper, faster and more secure transactions than processing individual paper checks. The number of individuals who have access to personal or financial information is dramatically reduced. These electronic transactions cannot be lost, misplaced or stolen in the mail.

ACH (American Clearing House) is an EFT format used for cross-border transactions. If you are outside of Canada or US, please  to discuss your options.  
For more information about ACH, see:  
http://banking.about.com/od/businessbanking/fl/What-does-ACH-Stand-For.htm  
or  
https://www.depositaccounts.com/blog/difference-between-wire-transfer-and-ach.html  
  
Using the “RBE” EFT format, a USD bank can make payments to both US and Canadian-based vendors who have USD bank accounts.

Collecting Vendor EFT Information
---------------------------------

1. 4GL will setup your  bank to handle EFT transactions and, if necessary, assist you in creating the file to transmit to your bank.
2. Download the Vendor EFT Authorization document, which contains a cover letter, privacy statement, and form to collect the vendor's banking information and authorization. Customize these with your logo, company name, contact info, etc.
3. Send the customized Vendor Authorization documents to your vendors.
4. Your vendors must supply you with their banking information and an email address for  to deliver the Payment Advice. As this information is returned, your staff must update the Vendor Maintenance file [PO11] as follows:
   * Contacts - enter the email address to receive the Payment Advice
   * Payment Code - enter “E” (leave “C” for vendors who will not be receiving electronic payments)
   * Bank Format - enter the format code as defined on the Bank Format Entry/Maintenance [CB14]
   * Bank Info - press F4 to enter the banking information provided by the vendor:
     + ABA Number - enter the 9-digit Routing Transfer/ABA #
     + Bank Account Number - enter the bank account number

Setting Up EFT in
-----------------

1. > Integrate EFT Payments = Y.

   If you make both wire and EFT payments, the pseudo check numbers will be prefixed with “E”. If you want to distinguish them, enable  > Separate Prefix for EFT Payments. This will set the wire payments prefix to “W” (EFT payments will remain prefixed with “E”).
2. System Controls [MS33] > Odometers > ensure the two EFT odometers are set up.
3. Vendor Payment Methods [AP16] - ensure that there is an E - EFT entry and that the Bypass flag is not selected.
4. Bank Format Entry/Maintenance [CB14] - Check to see if there is an existing format to satisfy the bank's requirement. If not, a new format must be added to this screen. This will normally be done by a technical person. There will also be programming involved to satisfy this new format.
5. Banks File Maintenance [AR11]:
   1. Select the bank through which you will be processing EFT transactions.
   2. Press F9 to expand the entry, then press F4 on EFT Support.
   3. Select the designated EFT File Format. Make sure that the format supports a Company Odometer to avoid duplication in the event of more than one EFT bank.
   4. Complete the fields with information provided by the bank. Fields not required by the selected EFT File Format will be “greyed out”.
   5. The EFT Directory is where the formatted file will be written in preparation for uploading to the bank. This can be a local drive or network drive.
6. In a test account, set up a couple EFT vouchers to pay through the normal disbursement process.
7. EFT Extract Current Payments [AP3L] – complete the fields and process.
8. The EFT file should be created in the assigned directory, and sent to the bank for verification. If the bank is satisfied, then the test is complete. If not, and this is a new format, modifications might need to be made to either the Bank Format parameters or to the newly created program amendments.

   To view the raw data, open the EFT file in a data editor. This will normally be done by a technical person.  
   The payment transaction can also be confirmed in the EFT Payment Transaction Inquiry [AP3L2].

EFT Formats


Click the Format code link to open or download the file format specifications. These specifications define the bank requirements for assembling data when transmitting information.

| Format | Description | Bank | Country | Odometer | Check | Bank Transit | Bank Account | Balance ACH | Description | Dr Tran Code | ACH Trace | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ACH | ACH - NACHA \* | RBC | US | C | O | Yes | Yes | Yes | Balancing Offset | 27 | Yes |  |
| CPA (HSBC) | CPA STD 1464 | HSBC | CA |  | F | Yes | Yes |  |  |  |  |  |
| CPA (CIBC) | CPA STD 1464 | CIBC | CA |  | F | Yes | Yes |  |  |  |  |  |
| CSV | COMMA SEPARATED | HSBC | CA |  | F | Yes | Yes |  |  |  |  |  |
| RBE | RBC STANDARD 152 | RBC | CA | C |  | Yes | Yes | Yes | Balancing Offset | 27 | Yes |  |
| RBU | RBC A/P LINK V8.891 | RBC | US | C | O | Yes | Yes |  |  |  |  | Payee Match as well |
| RBX | RBC A/P LINK V8.891 | RBC | CA | C | O | Yes | Yes |  |  |  |  | Payee Match as well |
| SSG | SSG TEST BANK | SSG | AU | C | O | Yes | Yes |  |  |  |  |  |
| TDC | TD BANK 80 BYTE | TD | CA | C | O | Yes | Yes |  |  |  |  |  |
| UOB | UOB FAST & GIRO | UOB | SG | C | O | No | Yes |  |  |  |  | Singapore Dollars |

\* See also ACH Direct Payments; and download and complete the ACH Authorization form and return it to 4GL.



Check Verification Formats


Click the Format code link to open or download the file format specifications. These specifications define the bank requirements for assembling data when transmitting information.

| Format | Description | Bank | Country | Odometer | Check | Bank Transit | Bank Account | CFP Account No | CFP Account Name |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ARP | ARP | RBC | US |  |  | Yes | Yes |  |  |
| BMO | BMO Positive Pay | BMO | US |  |  | Yes | Yes | Yes | Yes |
| CFP | CFP 80 Byte | TD | CA |  |  | Yes | Yes | Yes | Yes |
| DSJ | Desjardine 96 Bytes | DSJ | CA |  |  | Yes | Yes | Yes | Yes |
| FNB | First National Bank | FNB | US |  |  | Yes | Yes |  |  |
| HUN | Huntington | HUN | US |  |  | Yes | Yes |  |  |
| KEY | Key Bank 136 Bytes | KEY | US |  |  | Yes | Yes | Yes | Yes |
| RBC | Royal Bank | RBC | CA |  |  | Yes | Yes | Yes | Yes |
| RBP | RBC Payee Match | RBC | CA |  |  | Yes | Yes | Yes | Yes |
| SCC | Scotia Positive Pay | SCO | CA |  |  | Yes | Yes | Yes | Yes |
| WFG | Wells Fargo | WFG | US |  |  |  |  | Yes | Yes |

---
