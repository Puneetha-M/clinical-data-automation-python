**Clinical Data Automation - Medidata Rave to CDISC SDTM**
**Objective**: To bridge the gap between Clinical Study Build and Regulatory Submission by automating the transformation of raw EDC exports into SDTM-compliant datasets.

**Key Features**

**DM Domain**: Automated USUBJID concatenation and ISO 8601 date normalization.

**AE Domain**: Logic for ongoing event flagging (AEENRF) and sequence numbering (AESEQ).

**VS Domain**: Programmatic "Wide-to-Long" transformation using Pandas/Melt for normalized parameter tracking.

**Tech Stack**: Python, Pandas, NumPy.
