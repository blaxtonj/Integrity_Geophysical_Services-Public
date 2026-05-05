# Key Engineering Decisions

This section highlights the key engineering decisions made during the redesign, with a focus on how trade-offs were evaluated in the context of a relatively small, content-driven application.

Rather than optimizing for scale or complex functionality, decisions were guided by the need for clarity, maintainability, and alignment with business goals. This required balancing structure and consistency with the risk of overengineering.

Each decision reflects a deliberate choice between competing approaches, emphasizing pragmatic solutions that supported long-term maintainability without introducing unnecessary complexity.

---

### 1. Lightweight Design System vs Full Design System

#### Context
The original implementation lacked consistency in spacing, typography, and component usage, leading to visual fragmentation and slower development.

#### Options Considered
- Implement a full-scale design system with strict tokens and extensive abstraction  
- Introduce a lightweight, pragmatic system focused on consistency without overengineering  

#### Decision
A lightweight design system was implemented, focusing on typography scale, spacing consistency, and a small set of reusable components.

#### Trade-offs
This approach improved consistency and development speed, but did not provide the level of rigor or extensibility of a fully formalized design system.

#### Impact
The UI became more cohesive and easier to maintain, while avoiding unnecessary complexity for a relatively small project.
