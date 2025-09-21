# Product Requirements Document (PRD)
>
## 1. Document Information

- Product/Feature Name: SplitSub Web App
- Author : Troy Bent
- Date Created: 2025-09-19
- Last Updated: 2025-09-21
- Version: 0.1 (Draft)
- Course: CIDM 6325
---

## 2. Overview

- Summary: SplitSub is a web application designed to help small groups, such as households or friends,
easily manage and fairly share the costs of their communal subscriptions. The initial version will 
focus on core functionality for group management and equitable cost calculation based on manual user input.

- Problem Statement: A significant number of consumers share subscriptions without a simple, clear way
 to track usage and split costs fairly, leading to friction and frustration. Manual methods 
 are prone to error, lack accountability, and can create awkward social situations.

- Goals & Objectives: 
    - Provide a central, transparent hub for tracking shared subscription costs.
    - Simplify the process of calculating fair and equitable cost splits.
    - Reduce financial friction and misunderstandings within user groups.
    - Establish a foundational, scalable platform for future feature development.

- Non-Goals: 
    - Automated data scraping or cost prediction from subscription providers.
    - Handling of financial transactions or payments between users.
    - Advanced features like AI-powered optimization or recommendation engines.

---

## 3. Context & Background

- Business Context: This project is focused on iterative design and product development. This project
 is a core deliverable for CIDM 6325, Fall 2025, and is a component of the MSCISBA program. 

- Market/Customer Insights: Consumers are increasingly participating in the "subscription economy",
with shared accounts being a common practice among friends and families. Existing solutions for 
splitting these costs are often manual and inefficient.

- Competitive/Benchmark References: Traditional methods include shared spreadsheets and manual group
 chat tallies. Indirect competitors could be payment apps like Venmo or PayPal, which facilitate 
 payments but do not provide the cost calculation or tracking functionality.


---

## 4. Scope

- In Scope: Bullet list of included features/capabilities.
    - A responsive web-based user interface.
    - Group management (creating and naming a group, inviting members).
    - Subscription management (adding a subscription with its total cost).
    - Usage tracking (manual input of usage per group member per billing cycle).
    - Core calculation engine to generate a cost breakdown based on usage.

- Out of Scope: Bullet list of excluded items to prevent ambiguity.
    - Mobile-native applications.
    - Direct integration with subscription service APIs.
    - Automated payment processing or wallet features.
    - Public facing dashboards or analytics.
    - Advanced reporting beyond the core cost breakdown.
---

## 5. User Stories & Use Cases

- Primary User Persona(s): 
    - Group Creator: The user who initiates a group and adds the shared subscriptions.
    - Group Member: A member of a group who logs their usage and needs to see their share of the costs.
    - Cost-Conscious User: A user who wants a detailed breakdown of costs to ensure fairness.

- User Stories:
    - As a group creator, I want to create a group and invite my friends so we can start tracking
     our shared costs.
    - As a group member, I want to easily log my usage for a shared subscription so the cost is 
    split fairly.
    - As a group member, I want to view a transparent breakdown of who owes what so there are no 
    awkward conversations.

- Use Case Scenarios: Happy path and 1–2 edge cases.
    - Happy Path: A group creator adds a Netflix subscription to their "Roommates" group. Each 
    roommate logs their viewing time for the month. At the end of the billing cycle, the app 
    calculates each person's share of the cost, and everyone views the result.

    - Edge Case 1 (Incorrect Input): A user accidentally enters an incorrect cost for a subscription.
    The app allows the group creator to edit the subscription details and recalculate the split for 
    the current period.

    - Edge Case 2 (Uneven Usage): A member of the group does not log any usage for a specific 
    subscription. The calculation engine would assign them a cost of $0 for that billing cycle.
  
---

## 6. Functional Requirements

- FR-001: The system will allow a user to create a new group.
- FR-002: The system will allow a user to invite other users to their group.
- FR-003: The system will allow a user to add a new shared subscription with a name, total cost, 
and billing period.
- FR-004: The system will allow a user to manually log their usage for each shared subscription 
within a billing period.
- FR-005: The system will calculate and display an equitable cost split for all members of a group
 based on their logged usage.


---

## 7. Non-Functional Requirements

- Performance: All core calculations and data retrieval should be responsive, with a page load time
 of under 3 seconds on a standard broadband connection.
- Scalability: The system should be able to support up to 1,000 active groups and 5,000 individual
 users without significant performance degradation.
- Accessibility: The application should comply with WCAG standards. This includes ensuring 
proper color contrast, keyboard navigation, and screen reader compatibility.
- Security/Compliance: The application should use secure authentication protocols. User data, 
including subscription information and usage logs, will be stored in a secure, encrypted database.
- Reliability/Availability: The application should have an uptime of 99.9% during peak usage hours.

---

## 8. Dependencies

- Internal system dependencies
- External APIs/third-party services
- Cross-team deliverables
- Internal system dependencies: The front-end is dependent on the back-end API for all user management,
 data storage, and calculation logic.
- External APIs/third-party services:
    - Authentication for user sign-in, management and database storage.
- Cross-team deliverables: None for the MVA.

---

## 9. Risks & Assumptions

- Risks:
    - Inaccurate User Input: Users may enter incorrect data, leading to flawed calculations. 
    Mitigation: Provide clear in-app guidance and an option for users to edit past entries.
    - Scope Creep: The project may expand beyond the MVA before core features are stable. 
    Mitigation: Use review gates and a public roadmap to manage feature requests and prioritize
    based on the iterative design approach.
- Assumptions:
    - Users will be willing and able to manually log their usage data.
    - Users will be able to access the application via a modern web browser.
    - The calculation logic for equitable splitting will be agreed upon by all group members.

---

## 10. Acceptance Criteria

- FR-001: The "create new group" function is complete when a user successfully enters a group name
    and adds at least one other member.
    - FR-002: The "invite member" function is complete when the system successfully sends an invitation
    to a specified user.
    - FR-003: The "add subscription" function is complete when a user successfully enters a subscription
    name, total cost, and billing period, and the subscription is displayed in the group.
    - FR-004: The "log usage" functionality is accepted when a user can successfully enter a usage 
    value for a subscription and that value is stored and reflected in the system.
    - FR-005: The "cost split" calculation is accepted when the system correctly divides the subscription
    cost based on the members' logged usage data and displays the result.

---

## 11. Success Metrics

- KPIs or OKRs that indicate success (adoption %, NPS, revenue impact, error reduction, task completion rate).

- User Engagement: Measured by the percentage of groups with at least one updated usage log per 
billing cycle.
- Cost Clarity: Measured by a low number of user-reported calculation disputes.
- Adoption Rate: Measured by the number of new groups created per month.
- User Satisfaction: Measured via an in-app survey asking users to rate how well the app reduces 
  financial friction.

---

## 12. Rollout & Release Plan

- Phasing: The MVA will be a single release. Future iterations will add features such as
 enhanced reporting and AI-driven insights.
- Release Channels: The MVA will be released as a beta to a small group of users for feedback before
 a general release.
- Training/Documentation Needs: A simple in-app tutorial or a short "How It Works" page to guide new
 users through the core functionality.

---

## 13. Open Questions

- What is the best method for users to log their "usage"? (time, percentage, number of uses)
- How will the system handle a group with a member who refuses to log their usage? 
- What are the most common shared subscription types that users will want to track?

---

## 14. References

- GitHub Repo: <https://github.com/tbenty/CIDM-6325/tree/main/Docs>
- Project Pitch: <https://github.com/tbenty/CIDM-6325/blob/main/Docs/Project%20Pitch.md>
- System Sketch: <https://github.com/tbenty/CIDM-6325/blob/main/Docs/System%20Sketch.png>
- Risk Register: <https://github.com/tbenty/CIDM-6325/blob/main/Docs/Risk%20Register.png>