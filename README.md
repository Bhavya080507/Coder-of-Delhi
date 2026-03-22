# Social Network Recommendation System

## Overview
This project builds a simple recommendation system using a social network dataset.  
The goal is to suggest:
- People you may know (friend recommendations)  
- Pages you may like (interest-based recommendations)

It simulates how platforms like Instagram or Facebook suggest connections and content.

---

## Dataset
The dataset is in JSON format and contains:

### Users
- `id`: Unique user ID  
- `name`: User name  
- `friends`: List of friend IDs  
- `liked_pages`: List of page IDs  

### Pages
- `id`: Unique page ID  
- `name`: Page name  

---

## Data Cleaning
Steps performed:
- Checked for missing or inconsistent values  
- Ensured all friend IDs and page IDs exist  
- Removed duplicates (if any)  
- Standardized structure for processing  

---

## Features Implemented

### 1. Friend Recommendation
Logic:
- Find mutual friends
- Suggest users who:
  - Are not already friends  
  - Share common connections  

Example:  
If A and B both know C, A and B may be recommended to each other.

---

### 2. Page Recommendation
Logic:
- Suggest pages liked by:
  - Your friends  
  - Users with similar interests  

Example:  
If your friend likes "AI & ML Community", you may also get that suggestion.

---

## Tech Stack
- Python  
- JSON handling  
- Basic data structures (lists, dictionaries)  

---

## How It Works

### Step 1: Load Data
```python
import json

with open("data.json") as f:
    data = json.load(f)
