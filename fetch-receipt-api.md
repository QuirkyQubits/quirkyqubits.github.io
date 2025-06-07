# 🧾 Fetch Receipt Processor Project

**Author**: Jonathan Huang

**Repository**: [GitHub](https://github.com/QuirkyQubits/fetch-receipt-processor-challenge)

📄 **Note**: The [GitHub README](https://github.com/QuirkyQubits/fetch-receipt-processor-challenge#readme) is written for developers and assumes familiarity with tools like Git and Docker.

---

## 📌 Overview

This project is the backend for a digital points system that awards users for their shopping receipts. By entering details like the store name, total amount, and purchased items, the app calculates how many points each receipt earns.

Built as part of a challenge from Fetch Rewards, a company that rewards users for everyday purchases, the project demonstrates how purchase data can be programmatically processed and scored.

This page aims to provide an accessible summary of the project for a broad audience.

---

## 🔍 Behind the Scenes

Imagine you take a photo of your grocery receipt in a shopping rewards app. While you see reward points appear almost instantly, there's a backend engine processing the data behind the scenes. This project serves as an example implementation for that invisible part of the system, which stores, parses, and scores receipts using rules built into APIs.

---

## 🚀 How It Works

This project exposes two API endpoints that power the receipt processing system:

- `POST /receipts/process`: Submits a digital receipt to the system. It stores the receipt content and returns a unique receipt ID for later use.
- `GET /receipts/{id}/points`: Given a receipt ID, this returns the number of points that receipt earns based on the scoring rules.

Different purchases earn different points – for example, based on the amount spent or the time of day the purchase occurred.

For full technical instructions, check out the GitHub repository:🔗 [GitHub Repo](https://github.com/QuirkyQubits/fetch-receipt-processor-challenge/tree/main)

---

## 📬 Contact

For questions or contributions, contact: [quirkyqubits.dev@gmail.com](mailto\:quirkyqubits.dev@gmail.com)
