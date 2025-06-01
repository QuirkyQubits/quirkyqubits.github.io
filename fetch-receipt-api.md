---
layout: default
title: Fetch Receipt Processor API
---

# 🧾 Fetch Receipt Processor API Documentation
  <div class="meta">
    <strong>Author:</strong> Jonathan Huang<br/>
    <strong>Date:</strong> February 2025<br/>
    <strong>Audience:</strong> New developers and contributors<br/>
    <strong>Tools:</strong> Python, Django, Git, Markdown
  </div>

  <hr />

  <h2>📌 Overview</h2>
  <p>
    This project implements a RESTful API that processes retail receipts and calculates reward points based on store, purchase date, and item information.
  </p>
  <p>
    It was created as part of a coding challenge, but documented as if for production handoff — demonstrating ability to write setup guides, explain scoring logic, and support new developers onboarding to the codebase.
  </p>

  <h2>🚀 Getting Started</h2>
  <h3>Requirements</h3>
  <ul>
    <li>Python 3.10+</li>
    <li>pip (Python package installer)</li>
    <li><code>virtualenv</code> (optional but recommended)</li>
  </ul>

  <h3>Setup Instructions</h3>
  <pre><code># Clone the repo
git clone https://github.com/QuirkyQubits/fetch-receipt-processor-challenge.git
cd fetch-receipt-processor-challenge

# Set up and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Start the server
python app.py</code></pre>

  <p>The API will be accessible at <code>http://localhost:5000</code>.</p>

  <h2>📫 API Endpoints</h2>

  <h3>POST /receipts/process</h3>
  <p>Processes a receipt and returns a UUID representing the receipt.</p>

  <strong>Request Body:</strong>
  <pre><code>{
  "retailer": "Target",
  "purchaseDate": "2022-01-01",
  "purchaseTime": "13:01",
  "total": "35.35",
  "items": [
    {
      "shortDescription": "Mountain Dew 12PK",
      "price": "6.49"
    },
    {
      "shortDescription": "Emils Cheese Pizza",
      "price": "12.25"
    }
  ]
}</code></pre>

  <strong>Response:</strong>
  <pre><code>{
  "id": "8f765f3a-bb34-45cb-9e4d-d7c9bbfd6d57"
}</code></pre>

  <h3>GET /receipts/{id}/points</h3>
  <p>Returns the number of reward points for the given receipt ID.</p>

  <strong>Response:</strong>
  <pre><code>{
  "points": 28
}</code></pre>

<h2>🎯 Scoring Rules</h2>
<table>
  <thead>
    <tr>
      <th>Rule</th>
      <th>Points</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Alphanumeric characters in retailer name</td><td>+1 per character</td></tr>
    <tr><td>Total is a round dollar amount</td><td>+50</td></tr>
    <tr><td>Total is a multiple of 0.25</td><td>+25</td></tr>
    <tr><td>Each item description is a multiple of 3 chars</td><td>+20</td></tr>
    <tr><td>Items with trimmed description > 25 chars</td><td>+10</td></tr>
    <tr><td>Purchase date is odd-numbered</td><td>+6</td></tr>
    <tr><td>Purchase time is between 2pm and 4pm</td><td>+10</td></tr>
  </tbody>
</table>

<h2>🧪 Testing</h2>
<p>Run the test suite using:</p>
<pre><code>python -m unittest test_app.py</code></pre>
<p>The tests cover input validation, scoring logic, and endpoint correctness.</p>

<h2>📝 Notes for Contributors</h2>
<ul>
  <li>The app uses an in-memory dictionary to store receipts by UUID.</li>
  <li>Scoring logic is centralized for clarity and testability.</li>
  <li>Suggestions for improvement:
    <ul>
      <li>Add persistent storage (SQLite, PostgreSQL)</li>
      <li>Add schema validation with <code>pydantic</code></li>
      <li>Add Swagger/OpenAPI spec for self-documented endpoints</li>
    </ul>
  </li>
</ul>

<h2>🔗 Links</h2>
<p>
  <a href="https://github.com/QuirkyQubits/fetch-receipt-processor-challenge" target="_blank">
    GitHub Repo
  </a>
</p>

<p style="margin-top: 2em;">
  For questions, reach out at <a href="mailto:quirkyqubits.dev@gmail.com">quirkyqubits.dev@gmail.com</a>.
</p>

