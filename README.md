# Retention Improvement Case Study
### Data-Driven Cohort Experiment & Hypothesis Validation
This repository summarizes a case study I conducted as a Data Team intern at **Newruns**, focusing on data-driven experimentation to improve new-user retention for **A Perfect Day**, an AI-powered dating course recommendation app.

\* Detailed SQL queries, internal metrics, and confidential assets are excluded to comply with company data policies.

## Goal
As the company prepared for a long-term product renewal, we designed and evaluated several data-driven, hypothesis-driven experiments to understand how different engagement strategies affect early retention and overall app activation.

## My Key Contributions
As part of the data team, I contributed to experiment design, behavioral data analysis, and impact measurement, while helping validate data quality, control for confounding variables, and collaborate with the marketing team on content decisions informed by the analysis.

### 1. Data-Driven Content Selection
We used multiple behavioral datasets to determine which content themes and regions to update:
- Search queries from the last 1, 3, 6, and 12 months
- Theme and regional interest trends
- Regions not covered within the last 3 months
- App navigation flow insights

Based on these findings, curated courses, banners, and push notification themes and regions were selected using observed user-interest patterns rather than intuition alone.

### 2. Engagement Timing Analysis
- Analyzed user activity patterns across days of the week
- Identified peak usage hours through session data
- Considered seasonal behavior and weekday/weekend usage patterns

These insights were used to determine optimal push delivery windows and content update timing to maximize revisit probability.

### 3. Exposure-Based Cohort Design
Because randomized A/B testing wasn't possible, we constructed natural exposure cohorts based on when users signed up relative to the timing of content updates.
- Group A: No exposure
- Group B: Partial exposure
- Group C: Full exposure

\* To ensure Group A was an appropriate baseline, we examined multiple recent weeks and confirmed that their retention patterns were consistent.\
\* Group B served only as a reference and was not included in the final effect estimation.

#### Controlling Key Confounding Variables
- Avoided weeks containing holidays
- Used consistent analysis periods across groups
- Accounted for weekday/weekend engagement variation
- Ensured no external paid marketing was running during the experiment

These controls improved our ability to estimate the impact of in-app changes in a non-randomized setting.

### 4. Analytics Integration
**Google Analytics**
- Screen flow and funnel transitions
- User journey paths
- Session retention indicators

**App Database (MySQL)**
- Content views and bookmarks
- Push exposure behavior
- In-app actions related to each update


## Hypothesis Framework
- Updating content based on user interest will improve D+7 retention
- Curated course updates will increase content engagement
- Push notifications delivered during peak usage periods will increase revisit behavior
- Combining content updates with push notifications will increase daily active users

## Key Findings
- **D+7 Retention Improved** \
    Users exposed to updated content and well-timed push notifications showed an approximately 20% improvement in D+7 retention compared with the baseline group.
- **Curated Course Updates Had the Strongest Impact** \
    Curated course updates showed the largest increase in engagement, with course-related pageviews increasing by about 55%.
- **Push Notifications Showed Mixed but Positive Results**
    - Informational notices showed a clear increase in engagement
    - Store-related pushes had limited effect
- **Daily Active Users Increased**\
    Daily active users increased by about 19.7% during the experiment, indicating stronger overall app activation.

## Insights from the Data
- **Content Relevance Strongly Influenced Behavior**\
    Content updates based on user interest were associated with improved D+7 retention, while curated course updates drove the strongest gains in content engagement.
- **Timing Amplified the Impact of Updates**\
    Push notifications performed best when aligned with usage peaks, such as commute hours and Thu-Fri pre-weekend behavior in South Korea.
- **Bookmarks and Course Customization Needed Clearer UX Guidance**\
    High course engagement contrasted with low bookmark usage and edit features, suggesting that new users did not clearly realize that courses could be saved or edited.
- **No External Ads Strengthened Internal Validity**\
    With no paid marketing during the experiment, changes in retention and engagement could be attributed more directly to in-app updates.

## Limitations
- Retention did not continue beyond the initial improvement period
- The experiment had limited impact on deeper participation
    - Features such as course creation, reviews, and community engagement showed minimal growth
- The lack of randomized A/B testing limited the ability to fully isolate causal effects
- Despite efforts to control major confounders, residual temporal or behavioral variation may still have influenced user activity

## Future Improvements
- Improve UX clarity and discoverability for key actions such as saving and customizing courses to increase deeper participation
- Introduce simple, low-friction engagement features to encourage interaction
- Run longer-term experiments to measure sustained retention and daily active users while reducing short-term fluctuations
- Collect qualitative feedback through in-app prompts or short surveys to identify barriers to user participation
