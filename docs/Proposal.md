# PhishGuard: Phishing Website Detection and Classification Using URL & DNS Features

- **Author**: Alisha Minj  
- **Prepared for**: UMBC Data Science Master’s Degree Capstone  
- **GitHub Profile**: [Alisha Minj's GitHub](https://github.com/DATA-606-2023-FALL-THURSDAY/Minj_Alisha)  
- **LinkedIn**: [Alisha Minj's LinkedIn](https://www.linkedin.com/in/alisha-minj)  
- **PowerPoint Presentation**: [To be updated]  
- **YouTube Video**: [To be updated]  


## Background

The digital landscape, though filled with opportunities, is riddled with threats that pose significant challenges to individual and institutional security. One such prevalent threat is phishing. Phishing websites, designed to deceive and extract confidential information from unsuspecting users, leverage the trust that is typically associated with legitimate domains. As the vastness and complexity of the internet grow, manual detection and mitigation of such threats become increasingly untenable. This project, "PhishGuard", endeavors to bridge this gap by employing URL and DNS features to robustly detect and classify domains based on their potential malicious intent.

The creation and deployment of an effective detection model holds paramount importance in today's digital age. It extends benefits not only to individual users but also to businesses, organizations, and governments. By proactively identifying and classifying potential threats, we can significantly reduce the risk of data breaches and other security compromises, fostering a safer digital environment for all.


## Data

### **Sources**:
- **Phishing URLs from PhishTank**:
    - **Description**: Phishing URLs collected from the open-source service, PhishTank. The service provides phishing URLs in various formats like CSV, JSON, etc., updated hourly.
    - **Source Link**: [PhishTank Developer Info](https://www.phishtank.com/developer_info.php)

- **Legitimate URLs from the University of New Brunswick**:
    - **Description**: This dataset consists of a collection of benign, spam, phishing, malware, and defacement URLs. The specific file of interest from this collection is 'Benign_list_big_final.csv', which contains 35,300 legitimate URLs.
    - **Source Link**: [University of New Brunswick Dataset](https://www.unb.ca/cic/datasets/url-2016.html)
    
### **Data Size**:
- Phishing URL: 3,157 KB
- Legitimate URL: 4,043 KB
  
### **Data Shape**:
- Columns: 8
- Rows: 14858
  
### **Each Row Represents**: A unique domain or URL with its associated features.


## Data Dictionary

| Column Name           | Data Type   | Definition                                               |
|-----------------------|-------------|----------------------------------------------------------|
| `phish_id`            | Numeric     | Unique identifier for each phishing instance.            |
| `url`                 | String      | The actual URL that is identified as phishing.           |
| `phish_detail_url`    | String      | URL providing more details about the phishing attempt.   |
| `submission_time`     | DateTime    | Timestamp when the URL was submitted for verification.   |
| `verified`            | Categorical | Indicates if the URL was verified as phishing.           |
| `verification_time`   | DateTime    | Timestamp when the URL was verified.                     |
| `online`              | Categorical | Status of the phishing URL (online/offline).             |
| `target`              | String      | Target or subject of the phishing attempt.               |



**Target Variable/Label**:  
The primary classification label indicating the domain's category, i.e., benign, phishing, malware, or spam.

**Potential Features/Predictors**:  
Features extracted from URLs, such as their length, TLD, SLD, combined with DNS dataset information.
