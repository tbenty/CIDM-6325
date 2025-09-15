Project Pitch – SubSplit Web App

Section A
Submitted by: Troy Bent
CIDM 6325 – Fall 2025


**My Initial Design Thoughts for Exploration**
- I want a web application that helps small groups, like households or friends, manage and fairly share the costs of their communal subscriptions. The application's main purpose is to serve as a central hub for all shared services, tracking usage and proposing equitable cost splits. This approach directly addresses the financial ambiguity and friction that often arises when sharing accounts. I want to explore this concept iteratively, in a way that allows for continuous learning and adaptation based on user feedback.( Iterative Design In Action, Tips for designing successful web applications) 

**A. Project Pitch: SplitSub (Subscription Sharing App)**

**Problem**
- A significant number of consumers share subscriptions (e.g., streaming services, family mobile plans, online productivity tools) without a simple, clear way to track usage and split the costs fairly. This can lead to frustration and even financial confusion. Traditional solutions to this problem are often manual, ranging from shared spreadsheets and group chat messages to a simple mental tally. These methods are prone to human error, lack accountability, and can lead to awkward conversations about who owes what.  
SplitSub will add value by creating a dedicated, automated, and secure system that centralizes all shared expenses, making the process of tracking usage and calculating fair payments simple and transparent for everyone involved. By providing a clear and trusted source of truth, the app helps to reduce financial friction and maintain harmony within the group.

**Stakeholders**
    • Primary Users: Individuals and groups (households, families, or friends) who are actively sharing subscriptions and need a fair way to split costs.
    • Cost-Conscious Users: Those who require a transparent, detailed breakdown of their shared expenses to ensure they are paying an equitable share.
    • Group Creators: Users who initiate a shared subscription group, inviting members and managing the services within the app.
    • Subscription Service Providers: The companies (e.g., Netflix, Spotify) that offer the subscriptions being managed by SplitSub.


**Scope**
In-scope
    • Core functionality: The application will focus on a web-based "splitter" that calculates and displays a transparent cost breakdown based on user-entered usage data for shared subscriptions.
    • User and group management: Users can manually create a group, add members, and enter shared subscription details with its total cost.
    • Data tracking: The app will allow each member to manually log their usage for the billing period.
    • System components: The system will include a responsive front-end, a back-end to handle user management and calculations, and a secure database for storing all relevant data.
Out-of-scope
    • Automated data scraping: The application will not automatically scrape or predict subscription costs.
    • Advanced features: While future plans include AI touchpoints for suggesting efficient subscription tiers or recommending cancellations, these are beyond the scope of the initial version
    • Automated payments: The application will not handle the transfer of funds or payments between users. Its purpose is to show who owes what, not to facilitate the transaction itself.

**Success Metrics**
    • User Engagement: A measure of how often users interact with the application, such as the frequency of users logging in and updating their usage data.
    • Cost Clarity: The app's ability to clearly and accurately display cost breakdowns. This could be measured by a high rate of completed cost splits and a low number of user-reported disputes about the calculations.
    • Adoption Rate: The number of new groups and shared subscriptions created within the 	application over a specific time period.
    • User Satisfaction: Feedback from users indicating that the app effectively reduces friction and confusion related to shared       expenses. This could be measured through surveys or in-app ratings.

**The Minimal Viable Artifact (MVA)**
 - The Minimal Viable Artifact (MVA) for the SubSplit app will comprise three key deliverables: (1) a Subscription Management Module to track shared subscription costs, (2) a Group & Member Management Module for creating groups and inviting members, and (3) a Core Calculation Engine to generate an equitable cost split. This initial configuration is designed to be focused and extensible, providing a solid foundation for future development.


**Iterative Design Approach**
- An iterative design approach for SplitSub involves breaking down development into a series of short, repeatable cycles. Each cycle follows a loop: Planning and Requirements → Analysis and Design → Implementation → Testing, Evaluation, and Review. This method ensures the project remains focused, transparent, and adaptable.

- The initial cycles will focus on establishing a usable baseline by prioritizing core features like the cost "splitter". Subsequent cycles will introduce more features, such as adding different types of shared subscriptions or enhanced reporting. Each cycle concludes with an explicit review against the predefined success metrics, which helps govern the scope of the next pass and prevents "scope creep". This approach keeps the project manageable and allows for continuous learning and adaptation based on real-world usage and feedback.

**System Sketch**
- https://github.com/tbenty/CIDM-6325/blob/main/Docs/System%20Sketch.png

**Evidence Base**

- **C+R Research (2022) -** Subscription Service Statistics and Costs - <https://www.crresearch.com/blog/subscription-service-statistics-and-costs/>

- **Global Banking and Finance (2025)** - The Subscription Economy Surge

  <https://www.globalbankingandfinance.com/the-subscription-economy-surge-how-recurring-revenue-models-are-reshaping-global-commerce>

- **Synthesis (2025) -** AI and Personalization in Subscription Services 

  <https://synthesis-systems.com/subscription-monetization/ai/how-ai-transforms-subscription-businesses/>


**Risk Register**
https://github.com/tbenty/CIDM-6325/blob/main/Docs/Risk%20Register.png

|**Risk**|**Impact**|**Likelihood**|**Mitigation**|
| :- | :- | :- | :- |
|**Data Privacy & Security Breach**|High|Medium|Utilize secure authentication protocols. Conduct regular security audits.|
|**Calculation Errors**|High|Low|Implement a test suite for all calculation logic. Allow users to review and manually adjust split amounts before finalizing. |
|**Inaccurate User Input**|Medium|Medium|Provide clear, in-app guidance and examples for adding new subscriptions and usage data. Allow for correction of past entries.|
|**Scope creep relative to MVA**|Medium|Medium|Use review gates to confirm or defer features. Track enhancements in a public roadmap. Keep core flows stable.|