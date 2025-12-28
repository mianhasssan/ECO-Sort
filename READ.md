# Eco-Sort – Rule-Based Waste Classification System

Eco-Sort is a browser-based Single Page Application (SPA) designed to assist recycling facility workers in accurately classifying waste items under time pressure. The system applies strict, rule-based logic to minimize human error, especially when handling hazardous or contaminated materials.

---

## 🎯 Problem Statement

Manual waste sorting is error-prone and slow, particularly in recycling facilities where workers must make fast decisions on conveyor belts. Misclassification of hazardous or greasy items can lead to safety risks and recycling contamination.

Eco-Sort provides a fast, reliable, and browser-based solution that classifies waste items into **Hazard**, **Compost**, **Recycle**, or **Trash**, using predefined priority rules and clear visual indicators.

---

## 👤 User Persona

**Primary User:**  
Ahmed – a recycling facility worker who sorts waste quickly under pressure.  
He uses Eco-Sort to upload or capture an image of a waste item to instantly determine the correct disposal category.

---

## 🎭 Actors

- **User (Facility Worker):** Uploads or captures waste images
- **Rule-Based Classification Engine:** Applies waste-sorting rules
- **Web Browser:** Runs the SPA and displays results instantly

---

## ⚙️ System Requirements Specification (SRS)

### Functional Requirements

- **FR1:** Upload or capture a single JPG/PNG image (minimum 720p)
- **FR2:** Batteries, electronics, and chemicals are always classified as **RED (Hazard)**
- **FR3:** Greasy or food-stained paper/cardboard → **YELLOW (Compost)**
- **FR4:** Clean plastic, glass, cardboard → **GREEN (Recycle)**
- **FR5:** Soft plastic or unrecognized items → **GREY (Trash)**
- **FR6:** Display disposal color, category, and handling instructions

### Non-Functional Requirements

- **NFR1:** Classification completed within 5 seconds
- **NFR2:** Runs fully in-browser (no backend)
- **NFR3:** Mobile-responsive UI
- **NFR4:** Easy to use under time pressure
- **NFR5:** Stable performance for multiple consecutive uploads
- **NFR6:** Hazardous items must never be misclassified

---

## 🏗 Software Design Document (SDD)

### Architecture

- React + TypeScript SPA
- Tailwind CSS for responsive UI
- Rule-based classification engine
- No backend or server dependency

### Data Flow

1. User uploads or captures an image
2. Image labels are analyzed
3. Rule-based engine applies classification priority:
   **Hazard → Grease → Recycle → Trash**
4. Color-coded result and instructions are displayed

---

## 🧠 System Instructions (ICC Structure)

### Instruction
You are an Eco-Sort Rule-Based Agent responsible for accurate waste classification and responsive UI generation.

### Context
- Browser-based SPA
- Tailwind CSS + React
- Designed for fast decision-making

### Constraints
- Hazard items always take priority
- Greasy paper must never be recycled
- Default unrecognized items to Trash
- High-contrast, accessible UI

---

## 📚 Domain Knowledge

| Category  | Logic |
|----------|-------|
| Hazard   | Batteries, electronics, chemicals |
| Compost  | Greasy or food-stained paper |
| Recycle | Clean plastic, glass, cardboard |
| Trash   | Soft plastic or unknown items |

---

## 🧩 Project Structure

