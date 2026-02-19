---
title: "Batch_Run-Batch_Runs"
source: "Batch_Run-Batch_Runs.docx"
tags: ["batch run", "batch runs", "batch processing", "operations", "scheduling", "monitoring", "procedure", "runbook", "configuration", "documentation"]
version: "1.0"
last_updated: "2025-12-03"
short_description: "This Markdown file is a structured conversion of 'Batch_Run-Batch_Runs.docx', preserving the original hierarchy, lists, tables, and embedded images for vector-store ingestion. It includes 1 section header(s), such as: Batch Run - Batch Runs. 14 embedded image(s) were extracted and referenced inline. Formatting has been normalized, encoding artifacts cleaned, and duplicate lines removed to ensure high-quality text suitable for semantic search and retrieval. All content from the original document is retained and organized with consistent headings and list syntax."
long_description: "This file provides a faithful, structured Markdown rendition of the source document 'Batch_Run-Batch_Runs.docx'. The conversion focuses on accurately preserving the document's information architecture so it can be indexed and retrieved effectively from a vector store. The document includes 1 section header(s). Top-level sections use '##' and sub-sections use '###' so the outline is consistent and easy to navigate. The primary sections include: Batch Run - Batch Runs. Procedural or enumerated content has been preserved as Markdown lists, with 35 list item(s) detected across the document. Nested list levels are represented via indentation that aligns with Markdown conventions. No tables were detected in the source document; the conversion focuses on headers and paragraph text. Embedded images were extracted from the DOCX package (14 image file(s)) and are referenced inline at the point of appearance using Markdown image tags. The binary image files are saved alongside the Markdown for portability. To ensure text quality, common encoding artifacts (for example, mojibake such as 'â€“' in place of an en dash) have been normalized to UTF-8 equivalents. Consecutive duplicate lines were removed to reduce noise without altering meaning. The output uses clean Markdown syntax designed for robust parsing by downstream tooling, including vectorizers and embedding pipelines. The resulting Markdown is suitable for use cases such as semantic search, RAG pipelines, and documentation portals. It offers predictable structure, making it straightforward to split by headings or lists, and the table representations can be parsed into records if needed. Summary of structural elements: headings = 1, paragraphs = 29, lists items = 35, tables = 0, embedded images = 14. During transformation, textual content was left intact and not rewritten; only formatting and structural markers were added to clarify hierarchy. Where the original file used Microsoft Word styles such as 'Heading 1' or 'Heading 2', these were translated directly into Markdown header levels to preserve the author’s intended outline. Numbered or bulleted lists were converted into Markdown list syntax. Tables were converted to GitHub Flavored Markdown using the first row as the header row when present. Blank lines were inserted strategically to separate blocks and improve readability in plain text renderings."
---

## Batch Run - Batch Runs

![image](images_Batch_Run-Batch_Runs/image1.jpeg)![image](images_Batch_Run-Batch_Runs/image1.jpeg)

Batch Runs

This document outlines the configuration, troubleshooting and maintenance of the daily batch run process.

[!!!ATTENTION!!!: This document is intended for internal purpose s only. To make the document more relatable, live customer data is utilized.]

Configuration

Batch runs need to be setup in 3 areas for the process to work correctly. These areas are the: SM3 A pplication, ProIV C ontrol P anel and S erver.

SM3 Application

In SM3, the batch run configuration consists of the param eter setup, adding the DLY or RPT operators in MS32 and ensuring that the groups are adequately configured in developer mode.

Parameter Setup

- In Batch Run Menu > Function Parameter Maintenance you can configure the SM3 functions that would execute during the batch run process. Additionally, you would configure the appropriate options for each function. This is usually completed by the Implementation team or copied over from an existing environment.
![image](images_Batch_Run-Batch_Runs/image2.png)![image](images_Batch_Run-Batch_Runs/image2.png)

- In Batch Run Menu > Batch Run Parameter Maintenance, the functions that were created in the previous se ction would be added together to create a run. This is usually DLY (Daily), RPT (Report) or a specific day in the week such as MON (Monday). Th e s e essentially tell SM3 which functions to automatically run once the batch run process is executed.
![image](images_Batch_Run-Batch_Runs/image3.png) ![image](images_Batch_Run-Batch_Runs/image3.png)

In the above screenshot, the DLY batch run has 10 functions that would automatically run once the execution has been trigged by the time on the server (see the Server configuration for more details). Some functions require the “ Mnt ” and “ Inp ” columns to be setup correctly for the function to execute as intended. The Date column that is highlighted in the screenshot indicates the last execution date of the batch run.

- The Batch Run Submission and Batch Run Log Inquiry are tools used in the troubleshooting process and would be covered in the troubleshooting section.

Operators

- In the Security Menu > Operators, the appropriate user for the batch run must be created. For example, the DLY batch run would require a DLY operator to exist for things to work. These operators are typically created by copying the 4GL user and setting the password to a lowercase version of the operator ID. Hence, DLY’s password would be “ dly ”.
![image](images_Batch_Run-Batch_Runs/image4.png)![image](images_Batch_Run-Batch_Runs/image4.png)

Groups

- Go into Developer mode by entering “#” in the SM3 shortcode field. **Note** this can only be done in DEV environments.
![image](images_Batch_Run-Batch_Runs/image5.png)![image](images_Batch_Run-Batch_Runs/image5.png)

- Once in Developer mode, click the Administration Suite and then click “Groups”
![image](images_Batch_Run-Batch_Runs/image6.png)![image](images_Batch_Run-Batch_Runs/image6.png)

![image](images_Batch_Run-Batch_Runs/image7.png)![image](images_Batch_Run-Batch_Runs/image7.png)

- For each batch run (DLY, RPT and MON for example), ensure that there is a group configured with the company code of the environment you are working on assigned as a valid Co/Div. This is an important part of the process as it grants the batch run permission to log into the environment. Additionally, it dictates which function the batch run lo gs into.
![image](images_Batch_Run-Batch_Runs/image8.png)![image](images_Batch_Run-Batch_Runs/image8.png)

- In the screenshot above, the DLY batch run is assigned to MRU. Hence it can log into the MRU environment successfully. Once the DLY operator logs in, it executes the batch run function “BT921” which in turn, automatically executes all the functions that were setup in the parameters.

ProIV Control Panel

- Navigate to the ProIV Control Panel by entering [ Environment_IP_Address: 9801] in your browser. The credentials are typically the root credentials of that environment.
- Ensure that a “BATCHJOBS” profile exists for the environment.
![image](images_Batch_Run-Batch_Runs/image9.png)![image](images_Batch_Run-Batch_Runs/image9.png)

- In this case, the MRU deployment has a “BATCHJOBS” profile which would be responsible for handling the batch jobs process. This is typically already setup during the initial configuration of the environment. However, in the event that the profile does not already exists, follow the steps in the “ Setting up ProIV Control Panel/ Dashboard” section in this docume ntation:

Server

- On the server side of things, the batch run script must exist in / usr /bin/. Additionally, the crontab must be configured to execute that script at a specified time. The crontab is the trigger for the entire batch run process! Below we would highlight and breakdown each section of the script:
![image](images_Batch_Run-Batch_Runs/image10.png)![image](images_Batch_Run-Batch_Runs/image10.png)

- In the above screenshot we are looking at the mrudlybat scr ipt. This script handles the DLY batch run for MRU. I t is important to have the correct COMPANY_CODE- BATCHJOBS.prope rties as this connects the script to BATCHJOBS profile on the ProIV Control Panel.
- It is also important to have the correct ORACLE_HOME path and ORACLE_ SID
![image](images_Batch_Run-Batch_Runs/image11.png)![image](images_Batch_Run-Batch_Runs/image11.png)

- The “ script_path ” section must be set up with the name of the batch run as well as the company code and the server password.
- Most environments have the “Recreate batchque.pro” section in the script. This recreates batchque.pro every time once the batch run has been completed. This automates one of the troubleshooting steps!
- The last highlighted section in the above screenshot ensures that the DLY user is logging into the MRU environment, and the logs are generated accordingly.

Crontab

- Entering “crontab -e” in the CLI would open the crontab. This is where the scripts are scheduled to execute at a particular time.
![image](images_Batch_Run-Batch_Runs/image12.png)![image](images_Batch_Run-Batch_Runs/image12.png)

- MRUs DLY batch run is scheduled to execute at 3:30 AM on the server time. Below is the crontab syntax for quick reference
![image](images_Batch_Run-Batch_Runs/image13.png)![image](images_Batch_Run-Batch_Runs/image13.png)

- Once all these sections: SM3 Application, ProIV Control Panel and Server have been configured correctly, the batch runs should successfully run!

Troubleshooting

- Check if everything is configured correctly
- Check if the Groups have the company configured as Co/ Divs
- Verify that the BATCHJOBS profile has a license number. If not, then the batch jobs would not be able to get a license to log into SM3 and run the process
- Check to see if the crontab executed at the proper time: vi /var/log/ cron and scroll to the bottom of the page. Look for the time that crontab -e is configured to run and verify if it actually executed
- Manually recreate the batchque.pro file:
  - In / usr /dev 9/ virtual_machine / xxx_run / xxx_data run the commands below (where xxx is company code):
  - For the MRU example this is the path: / usr /dev9/ virtual_machine / ctbrun / mrudata
  - rm -f batchque.pro
  - ../.. / iscr batchque.pro -k59 -r16000
  - chmod 664 batchque.pro
  - chown 4gl batchque.pro
  - chgrp pro4 batchque.pro
- Ensure that the active checkbox is not checked in BT92
![image](images_Batch_Run-Batch_Runs/image14.png)![image](images_Batch_Run-Batch_Runs/image14.png)

- If the batch run hangs for whatever reason, the active checkbox remains checked which prevents any future processes from running
- Reach out to a programmer! Richard is the go to guy!
