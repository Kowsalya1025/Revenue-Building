# RevIntel — Revenue Intelligence Inbox

## 1. Project Overview

RevIntel is a Revenue Intelligence Inbox designed to help sales managers review sales calls and meetings, analyze customer conversations, identify follow-up priorities, and route conversations to the appropriate teams.

The application provides a centralized dashboard for monitoring sales activities, reviewing conversation insights, managing records, and generating structured data exports.

## 2. Objectives

- Monitor calls, meetings, and sales activities through a dashboard.
- Analyze conversations to identify customer needs, risks, and follow-up actions.
- Route conversations to Sales, Support, or Management.
- Import CSV and JSON files to manage conversation records.
- Detect duplicate records and update existing conversations.
- Allow manual corrections to priorities, assignments, and statuses.
- Generate downloadable reports and a JSON/CSV export manifest.

## 3. Key Features

### Dashboard
- Total conversations, calls, and meetings.
- Pending follow-ups and high-priority records.
- Conversation outcomes and routing distribution.
- Sales activity summaries and trends.

### Conversation Inbox
- Search and filter conversations.
- View customer details and conversation summaries.
- Review priorities, outcomes, assigned teams, and next actions.
- Identify conversations requiring immediate attention.

### Conversation Routing
- Rule-based routing to Sales, Support, and Management.
- Routing recommendations with explanations.
- Manual assignment and priority corrections.
- Tracking of routing decisions and overrides.

### Data Import and Management
- CSV and JSON import support.
- Input validation and import summaries.
- Duplicate detection using stable conversation identifiers.
- Updates to existing records instead of creating duplicates.
- Manual corrections and conflict handling.

### Exports
- Conversations CSV.
- Routing decisions CSV.
- Findings JSON.
- Import history export.
- Export manifest in JSON or CSV format.

## 4. Technology Stack

- **Frontend:** React, Vite, TypeScript
- **Styling:** Tailwind CSS
- **Charts:** Recharts
- **Data Storage:** Browser storage or the configured database
- **Data Formats:** CSV and JSON
- **Deployment:** Vercel or another compatible hosting platform

*Update this section to match the technologies actually implemented in the final application.*

## 5. Project Structure

```text
Revenue-Intelligence-Inbox/
├── client/
│   ├── src/
│   ├── public/
│   └── package.json
├── exports/
│   ├── conversations.csv
│   ├── routing_decisions.csv
│   ├── findings.json
│   └── manifest.json
├── slides/
│   └── findings-and-decisions.pptx
├── recording/
│   └── product-demo.mp4
├── tests/
└── README.md
```

*The structure above is a suggested layout. Adjust it to match the actual project files.*

## 6. Installation and Setup

### Prerequisites

- Node.js and npm installed.
- A code editor such as Visual Studio Code.
- The project source files.

### Steps

1. Download or clone the project repository.
2. Open the project folder in Visual Studio Code.
3. Open a terminal.
4. Navigate to the frontend directory.

```bash
cd client
npm install
```

5. Start the development server.

```bash
npm run dev
```

6. Open the local URL displayed in the terminal, usually `http://localhost:5173`.

### Running Tests

If the project includes an automated test script, run:

```bash
npm test
```

Use the test commands defined in the project's `package.json`.

## 7. Import and Duplicate Handling

The application accepts supported CSV or JSON conversation files.

During import, records are validated and compared using their stable conversation identifiers.

- **New record:** Inserted into the application.
- **Existing unchanged record:** Recognized without creating a duplicate.
- **Updated record:** Existing record updated using the defined update rules.
- **Invalid record:** Rejected with an explanatory message.
- **Conflicting record:** Flagged for review when incoming data conflicts with a manual correction.

The import summary displays the number of records inserted, updated, skipped, rejected, or flagged for conflicts, as supported by the implementation.

## 8. Testing Strategy

The following scenarios should be tested before submission:

1. Import 10 unique conversation records.
2. Import the same file again and verify that no duplicates are created.
3. Import a modified record and verify that the existing record is updated.
4. Test duplicate identifiers within the same file.
5. Test invalid and incomplete records.
6. Modify a conversation manually and verify that the correction persists after refresh.
7. Test conflicts between manual corrections and incoming source data.
8. Download CSV and JSON exports and verify their contents.
9. Check that the manifest matches the generated exports.
10. Verify that dashboard metrics update after data changes.

## 9. Findings and Decision Log

The application should document three important findings based on the available source conversations.

Each finding should include:

- Finding summary.
- Supporting conversation IDs and dates.
- Relevant source evidence.
- Business impact.
- Recommended action.

The decision log should also document one considered but rejected approach, explaining the reasoning and trade-offs.

Findings must be based on actual source data. Any demonstration data should be clearly labelled.

## 10. Deployment

Deploy the application using a compatible hosting platform such as Vercel.

Before sharing the deployment link:

1. Build the application successfully.
2. Configure the required environment variables, if any.
3. Deploy the latest tested version.
4. Open the public URL in an incognito browser window.
5. Verify that the application loads without requiring access approval.
6. Test the key workflows and confirm that downloads work.

**Deployed application:** Add the verified public URL here.

**Source code:** Add the repository URL or submission location here.

## 11. Deliverables

- Working Revenue Intelligence Inbox application.
- Publicly accessible deployment link.
- Editable source files.
- Generated CSV/JSON exports.
- Export manifest.
- README documentation.
- Five-slide presentation explaining findings and decisions.
- Three-minute narrated screen recording demonstrating the workflow, a difficult routing decision, and the duplicate/update test.

## 12. Limitations

Document any known limitations of the implemented version, such as browser-local data storage, supported input formats, rule-based analysis, or the absence of external CRM integrations.

Do not describe a feature as completed unless it has been implemented and tested.

## 13. Conclusion

RevIntel provides a centralized approach to reviewing sales conversations, prioritizing follow-ups, routing customer issues, and maintaining reliable conversation records. Its import validation, duplicate handling, manual correction workflow, and structured exports help sales managers make informed decisions using traceable conversation evidence.
