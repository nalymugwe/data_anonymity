# Data_Anonymity
A project to try out the various option to anonymize data.

## **Data Privacy**

Data privacy, also known as information privacy, is concerned with the proper handling of data—specifically, the consent, notice, and regulatory obligations for personal data. Personal data which is commonly abbreviated as PII (Personally Identifiable Information) is information that could potentially identify a specific individual. Examples of PII include, but are not limited to: Full name, ID number, Address,email address, telephone number etc.

Due to various laws, rules, and standards that are in place, the precise definition of data privacy may fluctuate greatly depending on the region and industry. The General Data Protection Regulation (GDPR) of the European Union and Kenya's The Data Protection Act, 2019 are examples of comprehensive data protection regulations. Therefore, it's critical to understand these rules and have a working knowledge of data, especially for those who work in the data industry.

There are programming techniques that can be used to privatize the data at hand in addition to any rules that may have been established by the organization or nation. Below, we'll examine each of these tools separately. 

### Faker Library

The Faker library generates realistic fake data, such as names, addresses, phone numbers, and email addresses. It can be used to replace sensitive information with synthetic data while preserving the structure and format of the original data.

### Data Masking

This technique involves replacing some or all of the data in a particular field with asterisks, X's, or other placeholders.

### Data Shuffling

This method involved randomly rearranging the data in a column so that the original values exist, but their connection to the rest of the data in each row is broken. It's used when the individual values are important, but the association between them is not.

### Data Tokenization

This involves replacing sensitive data with tokens (usually random strings of characters). 

Ihaven't covered all the tools available but some of the common tools used by data profesionals as they analyze the data. As noted, the shape of the dataset remained constant as you wouldn't want to use a tool that would aletr the shape of your data. However, kindly note that there are certain factors to consider as you select a tool for anonymizing your data:

- Data Consistency: When anonymizing data, it's important to maintain the same type and format of data. For example, if a field originally contains a phone number, it should still contain a phone number after being anonymized.
- Relevance: If you are replacing data in fields like 'Location', ensure the generated data is relevant. For instance, it might be misleading to have a country that doesn't match the phone number country code. Additionally, when shuffling data, you disrupt the relationships between different data fields. This can limit the usefulness of the data for many analytical tasks that rely on understanding correlations between different data fields.
- Information Loss: Always consider the nature of your data and the requirements of your use case when choosing an anonymization tool. Be aware that data masking could lead to loss of information. The masked part of the data cannot be used for analysis, so it's important to balance the need for privacy with the need for data utility.
- Risk of Re-identification: Even if some data is masked, individuals may still be re-identifiable if there's enough unmasked data that could be linked back to them. This could be a risk especially with semi-identifiers or quasi-identifiers. Shuffling preserves the overall distribution of data in each column. If your use case depends on maintaining the same overall patterns in the data, shuffling can be a good choice. However, if there's data on the email address that contains the names of the indvidual, then re-identification may be possible.
- Uniqueness: If the same original value gets assigned different tokens in different instances, it might create inconsistencies in data analysis. So, you should consider whether to use consistent tokens (the same original value always gets the same token) or unique tokens (the same original value can get different tokens).
- Legal and Ethical Considerations: Even though data is anonymized, you should still handle it responsibly. Some jurisdictions have specific legal requirements around data anonymization, so ensure that your tool complies with any relevant laws and regulations.
