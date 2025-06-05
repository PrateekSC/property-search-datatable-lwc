# property-search-datatable-lwc

# 🏠 BatchData Property Search LWC

This project demonstrates a Lightning Web Component (LWC) that integrates with the [BatchData Property Search API](https://developer.batchdata.com/docs/batchdata/batchdata-v1/operations/create-a-property-search). It enables users to:

- Enter a search query (e.g., address, ZIP code)
- Fetch property and mortgage data in real time
- Display results in a responsive Lightning Datatable
- Save selected property records into Salesforce

---

## 🔧 Features

- 🔍 **Property Lookup** using external API  
- 📊 **Dynamic Datatable** rendering of property & mortgage info  
- 🔄 **Real-time API Integration** using Apex callouts  
- 💾 **Salesforce Data Model Integration** for persistent storage  

---

## 🚀 How It Works

1. **User Input**  
   User enters a search parameter (address, ZIP, etc.) via the input field.

2. **API Call**  
   The LWC sends a request to the BatchData API via an Apex controller.

3. **Display Results**  
   Property and mortgage details are parsed and shown in a datatable.

4. **Save to Salesforce**  
   User selects a record and clicks “Save” to store it in custom Salesforce objects.

---

## 🗂️ Salesforce Data Model

The following custom objects/fields are created to store API results:

### 🔹 `Property__c`
- `Address__c`
- `City__c`
- `State__c`
- `Zip__c`
- `YearBuilt__c`
- `LotSize__c`
- `SquareFootage__c`
- `Bedrooms__c`
- `Bathrooms__c`

### 🔹 `Mortgage__c`
- `LoanAmount__c`
- `LoanType__c`
- `InterestRate__c`
- `LenderName__c`
- `OriginationDate__c`
- Lookup to `Property__c`

> The data model is designed based on typical fields from the API response. It can be extended as needed.

---

## 🧪 Prerequisites

- Salesforce DX setup  
- API key from [BatchData](https://developer.batchdata.com/)  
- Named Credential or Remote Site Setting for API callouts
