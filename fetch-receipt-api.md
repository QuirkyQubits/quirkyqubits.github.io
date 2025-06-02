# 🧾 Fetch Receipt Processor API Documentation

**Author**: Jonathan Huang  
**Repository**: [GitHub](https://github.com/QuirkyQubits/fetch-receipt-processor-challenge)  
**Challenge**: [Fetch Rewards Receipt API](https://github.com/fetch-rewards/receipt-processor-challenge)  
**Tech Stack**: Django, Docker

---

## 📌 Overview

This project implements a Django-based REST API that calculates reward points from submitted retail receipt data. It was developed as part of the Fetch Rewards receipt processor coding challenge.

Users submit a JSON receipt to the Process API and receive a unique ID. This ID can then be used to query the Points API to determine how many points the receipt earned based on specific business rules.

---

## 🚀 How to Use

The project is fully Dockerized for easy setup and execution. You can also run it locally using Python and Django.

For complete setup instructions, API usage, and example payloads, please refer to the GitHub repository:  
🔗 [Project README](https://github.com/QuirkyQubits/fetch-receipt-processor-challenge/blob/main/README.md)

---

## 📫 API Summary

- **POST `/receipts/process`** — Accepts receipt data and returns a UUID.
- **GET `/receipts/{id}/points`** — Returns the number of points earned by the receipt associated with the given ID.

For full API specification, see the original challenge:  
📄 [API Spec](https://github.com/fetch-rewards/receipt-processor-challenge/blob/main/api.yml)

---

## 📬 Contact

For questions or contributions, contact: [quirkyqubits.dev@gmail.com](mailto:quirkyqubits.dev@gmail.com)
