# User Story 004: Search Products

**ID:** US-004
**Role:** Customer

---

## Description

A brief summary of the user story:

> As a customer I want to search for products by name or keywords So that I can quickly find what I'm looking for.

---

## Acceptance Criteria

Specific conditions that must be met for this user story to be considered complete:

- Search bar is prominent on all pages
- Search accepts minimum 2 characters
- Results are displayed within 2 seconds
- Results show product name, image, price
- Search matches product name and description
- "No results found" message shown when appropriate
- Search suggestions appear as user types (autocomplete)
- Search is case-insensitive

---

## Flowchart

### High-level visual representation of the process:

<div align=center>

![Flowchart](./flowchart.png)

 </div>

## Sequence Diagram

### Illustrates the step-by-step interaction between actors and the system:

<div align=center>

![Sequence Diagram](./sequence-diagram.png)

 </div>

## Pseudocode

```text
function searchProducts(keywords){
    if(keywords.length()<2)
        return;

    list<Products> products=findRelevantProducts(keywords) // DB call

    if(products==null)
        return "No results found";

    return products;

}
```
