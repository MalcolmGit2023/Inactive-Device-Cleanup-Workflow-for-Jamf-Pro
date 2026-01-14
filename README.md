***

# **Inactive Device Cleanup Workflow for Jamf Pro**

*Automated Detection + Manual Validation*

This document outlines the workflow for identifying, reviewing, and safely removing inactive or stale macOS devices from Jamf Pro.  
The process uses Jamf’s **Advanced Search** for automation and a **manual verification** step before permanent deletion.

***

## **Checklist**

### **1. Configure / Verify Advanced Search**

*   [ ] Create or verify a saved Advanced Search with the following criteria:
    *   [ ] Last Check-in > 90 days
    *   [ ] Last Inventory Update > 90 days
    *   [ ] Exclude ADE-enrolled devices
    *   [ ] Exclude loaners, labs, or long-term offline assets

***

### **2. Generate the Inactive Device List**

*   [ ] Run the saved Advanced Search
*   [ ] Confirm results populate dynamically

***

### **3. Export List for Manual Validation**

*   [ ] Export results to CSV
*   [ ] Validate each device:
    *   [ ] Check asset database
    *   [ ] Confirm no active user assignment
    *   [ ] Confirm not in repair/RMA workflow
    *   [ ] Confirm not expected to check in (travel, leave, etc.)

***

### **4. Perform Mass Deletion in Jamf Pro**

*(Only after confirmed validation)*

*   [ ] Return to Advanced Search results
*   [ ] Select all confirmed inactive devices
*   [ ] Click **Actions → Delete**
*   [ ] Acknowledge deletion is permanent

***

### **5. Remove from Apple Business Manager (If Applicable)**

*   [ ] Remove device from ABM if:
    *   [ ] Recycled
    *   [ ] E-wasted
    *   [ ] Permanently decommissioned

***

### **6. Monthly Maintenance**

*   [ ] Run this workflow once per month
*   [ ] Review Advanced Search
*   [ ] Export, validate, and delete stale devices
*   [ ] Update ABM as needed

***

## **Reference**

Jamf’s guidance on removing inactive devices:  
🔗 <https://youtu.be/H_jvFtQF6WU?si=wUsK0xnRodGAhjoz>

***
