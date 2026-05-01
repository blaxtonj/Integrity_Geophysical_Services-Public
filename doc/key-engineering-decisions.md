# Key Engineering Decisions

This document outlines the most impactful improvements made during the redesign, focusing on the reasoning behind each change and the trade-offs considered.

## 1. Establishing a Design System

### Before
The original implementation lacked a consistent system for spacing, typography, and component usage. Styles were applied ad hoc, which led to visual inconsistencies and made the UI harder to maintain.

### After
Introduced a lightweight design system built around:

- A consistent typography scale for headings and body text  
- Standardized spacing tokens  
- Reusable UI components (buttons, sections, cards)  
- Defined color usage  

### Why it mattered
This reduced inconsistency across the interface and created a foundation for scalable development. It also improved development speed by minimizing one-off styling decisions.

### Trade-offs
A full design system would have added unnecessary complexity for a relatively small project. A lightweight, pragmatic system was chosen instead to balance consistency with simplicity.

---

## 2. Restructuring Content for Readability

### Before
Content was presented in dense sections with limited hierarchy, making it difficult to quickly scan or identify key information.

### After
- Broke content into clearly defined sections  
- Converted dense text into more scannable layouts  
- Improved heading structure and spacing  
- Introduced visual grouping to guide user flow  

### Why it mattered
Users can now quickly identify relevant information without needing to read through large blocks of text. This is especially important for service-based websites where clarity directly impacts engagement.

### Trade-offs
Some technical detail was condensed to improve readability. The focus shifted from exhaustive explanation to clear communication.

---

## 3. Simplifying Navigation

### Before
Navigation lacked clear prioritization, making it harder for users to understand where to go next.

### After
- Simplified navigation structure  
- Reduced unnecessary options  
- Improved labeling for clarity  
- Ensured consistent navigation behavior across screen sizes  

### Why it mattered
Reducing cognitive load helps users move through the site more efficiently and improves overall usability.

### Trade-offs
Fewer navigation options meant some content needed to be reorganized or consolidated, requiring more intentional content structuring.

---

## 4. Improving Responsiveness

### Before
Responsive behavior was inconsistent, with layouts that did not adapt cleanly across different screen sizes.

### After
- Rebuilt layouts with a mobile-first approach  
- Standardized breakpoints  
- Ensured consistent spacing and alignment across devices  

### Why it mattered
A consistent experience across devices is critical, especially for business websites where users may access content from various contexts.

### Trade-offs
Designing mobile-first required rethinking some desktop layouts rather than simply adapting them, which increased initial development time.

---

## 5. Introducing Purposeful Motion

### Before
The original site had little to no interactive feedback or motion, resulting in a static user experience.

### After
- Added subtle animations using Framer Motion  
- Introduced hover and transition states  
- Used motion to guide attention rather than decorate  

### Why it mattered
Motion improves perceived responsiveness and helps guide user focus when used intentionally.

### Trade-offs
Overuse of animation can negatively impact performance and usability. Animations were kept minimal and optimized to avoid unnecessary overhead.

---

## Summary

The redesign focused on improving structure, consistency, and usability rather than introducing unnecessary complexity. Each decision was made to support clearer communication, better user flow, and a more maintainable codebase.
