# Architecture

This document outlines the architectural improvements made during the redesign of Integrity Geophysical Services Inc, focusing on structure, maintainability, and scalability.

---

## Overview

Prior to the redesign, the project lacked a clear architectural structure. Most components, pages, and utilities were colocated within the `app/` directory, leading to poor separation of concerns.

As the codebase grew, this made it increasingly difficult to maintain, reason about, and extend. Changes in one area often required navigating unrelated parts of the codebase, and there were no clear patterns guiding organization.

The redesign introduced a more deliberate structure, separating concerns and establishing consistent patterns for component organization and reuse.

## High-Level Structure

```
/
├─ app/   
│  ├─ (home)
│  │  ├─ Companies.tsx
│  │  ├─ Fractured.tsx
│  │  ├─ Hero.tsx
|  |  └─ Services.tsx          
│  ├─ (contact)
|  |  └─ Contact.tsx  
│  ├─ samples/
│  │  └─  page.tsx            
│  └─ api/                 # API route for form submission 
│     └─ submit
|      └─ route.ts         
├─ components/               # Reusable UI components
├─ data/                   # Static configuration & JSON data
├─ img/                    # Static images
└─ utils/                  # Utility functions
```

## Routing & Route Groups

Route Groups: Folders wrapped in parentheses, like (home), and (contact), are used purely for organization and do not affect the URL path.

Pages inside groups:

- (home)/Hero.tsx → /

- (home)/Services.tsx → /

- (contact)/Contact.tsx → /

Each section is composed into the root route (`/`), while the route groups exist purely for structural organization and separation of concerns.

### Separation of Concerns

The repository separates functionality into distinct folders based on responsibility:

-  ```components/``` – shared UI components used across the entire site

-  ```data/``` – static configuration objects and structured data

-  ```utils/``` – reusable helper functions and logic

-  ```img/``` – static visual assets

This separation ensures that UI rendering, data configuration, and utility logic remain decoupled, improving maintainability and scalability.

## Design Principles

- Keep routing structure separate from UI composition
- Prefer feature-based grouping over flat organization
- Isolate reusable logic in dedicated utility layers

## Summary

The redesigned architecture introduces clearer boundaries between concerns, improves navigability of the codebase, and establishes consistent organizational patterns to support long-term maintainability and scalability.
