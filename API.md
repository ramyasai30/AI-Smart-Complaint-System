# AI Smart Complaint System - API Contract

## Base URL

/api

---

# 1. Submit Complaint

## Endpoint

POST /api/complaints

### Request Body

```json
{
  "citizenName": "Ramya Sai",
  "phoneNumber": "9876543210",
  "location": "Benz Circle, Vijayawada",
  "complaintText": "There is a water leakage near the main road."
}
```

### Success Response

```json
{
  "success": true,
  "message": "Complaint submitted successfully.",
  "complaintId": "CMP1001",
  "category": "Water Supply",
  "department": "Water Department",
  "status": "Pending"
}
```

---

# 2. Get All Complaints

## Endpoint

GET /api/complaints

### Success Response

```json
[
  {
    "complaintId": "CMP1001",
    "citizenName": "Ramya Sai",
    "category": "Water Supply",
    "department": "Water Department",
    "status": "Pending",
    "createdAt": "2026-07-17"
  }
]
```

---

# 3. Update Complaint Status

## Endpoint

PATCH /api/complaints/:id

### Request Body

```json
{
  "status": "Resolved"
}
```

### Success Response

```json
{
  "success": true,
  "message": "Status updated successfully."
}
```

---

# Complaint Categories

- Roads
- Water Supply
- Electricity
- Sanitation
- Drainage
- Street Lights
- Garbage Collection
- Public Property Damage
- Others

---

# Complaint Status

- Pending
- In Progress
- Resolved