# Communication Analysis Tool

A lightweight, zero-dependency, client-side web application designed to analyze and visualize email communication logs. 

By simply uploading a CSV of email metadata, you can generate detailed reports on a specific individual's sent and received communications over time, grouped by individual contacts or overall domains.

## ✨ Features

* **100% Private & Secure:** All data processing, filtering, and chart generation happens entirely within your browser. No data is ever sent to a server, and nothing is saved to cookies or local storage.
* **Dynamic Visualizations:** View communication trends over time using built-in, lightweight HTML5 Canvas Bar and Line charts.
* **Domain & Email Grouping:** Easily toggle between viewing individual email addresses or aggregating data by organizational domains (e.g., `@example.com`).
* **Two-Way Analysis:** See a consolidated view of incoming and outgoing message volume to identify the target's most frequent contacts.
* **Excel Export:** Instantly download a multi-sheet, Excel-compatible `.xls` report of your analysis.
* **Zero Setup:** No Node.js, npm, or build steps required. It runs completely out of a single HTML file using React via CDN.

## 🔒 Privacy & Data Handling

This tool is designed with strict data privacy in mind:
* Data is read directly into your browser's local RAM.
* Refreshing or closing the tab immediately and permanently wipes the data.
* Network connections are only used to fetch the open-source React and Babel libraries on initial load.

## 🚀 Getting Started

Because this is a standalone HTML file, installation is incredibly simple:

1. Clone or download this repository.
2. Double-click the `index.html` file to open it in any modern web browser (Chrome, Edge, Firefox, Safari).
3. Enter the target person's name and email addresses (comma-separated) to establish an identity profile.
4. Drag and drop your communication CSV file into the drop zone.

## 📊 Expected CSV Format

To parse correctly, the tool expects a standard CSV file with headers. The parser is somewhat flexible but specifically looks for columns containing the following keywords (case-insensitive):

* `From` (e.g., "Communication From")
* `To` (e.g., "Communication To")
* `Cc` (e.g., "Communication Cc")
* `Bcc` (e.g., "Communication Bcc")
* `Sent Date` or `Date` (e.g., "Sent Date Time")

**Example CSV Structure:**
```csv
"Communication From","Communication To","Communication Cc","Communication Bcc","Sent Date Time"
"jane.doe@example.com","john.smith@test.com","","", "10/24/2023 14:30:00"
"john.smith@test.com","jane.doe@example.com","","", "10/25/2023 09:15:00"
