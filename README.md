# Retention Improvement Case Study
### Data-Driven Cohort Experiment & Hypothesis Validation
This respository summarizes a case study I conducted as a Data Team intern at **Newruns**, focusing on data-driven experimentation to improve new user retention for **A Perfect Day**, an AI powered dating course recommendation app.

\* Detailed SQL queries, internal metrics, and confidential assets are excluded in accordance with company data policies.

## Goal
As the company prepared for a long term product renewal, we designed and evaluated several data-driven, hypothesis based experiments to understand how different engagement strategies affects early retention and overall app activation.

## My Key Contributions
As part of data team, I contributed to experimental design, data-driven decision making, and impact measurement, ensuring data validation and controlling confounding variables, while collaborating closely with the marketing team who created the content informed by our analysis.

### 1. Content theme/region selection based on user data
We used multiple behavioral datasets to determine which content to update
- last 1,3,6,12 months of search queries
- theme and regional interest trends
- regions not covered within the last 3 months
- app navigation flow insights

All curated courses, banners, and push notification themes/regions were selected based on actual user interest data.

### 2. Optimizing push notification and content update timing through user activity analysis
- Analyzed user activity patterns across days of the week.
- Identified peak usage hours through session data.
- Considered seasonal behavior and weekday/weekend usage patterns.

Use this to determine optimal push delivery and content update timing to maximize revisit probability.

### 3. Exposure based cohort design
Because randomized A/B testing wasn't possible, we constructed nautral eposure cohorts based on when users signed up relative to content updates timing.
- Group A: No exposure
- Group B: Partial exposure
- Group C: Full exposure

\* To ensure Group A was an appropriate baseline, we examined multiple recent weeks and confirmed that their retention patterns were consistent.\
\* Group B served only as a reference and was not included in the final effect estimation.

#### Controlling Key Confounding Variables
- avoided weeks containing holidays
- used consistent analysis periods across groups
- accounted for weekday/weekend engagement variations
- ensured no external paid marketing was running during the experiment

These controls improved our ability to isolate the impact of in-app changes.

### 4. Analyitics Integration
**Google Analytics**
- screenflow and funnel transitions
- user journey paths
- session retention indicators

**App DB (MySQL)**
- content views & bookmarks
- push exposure behavior
- in-app actions related to each update


## Hypothesis Framework
- Interest aligned, freshly updated content will improve D+7 retention.
- New curated courses and banners will increase content engagement.
- Well timed, contextually relevant push notifications will increase revisit behavior.
- Combining multiple engagement strategies will increase Daily Activate Users.

## Key Findings
- **D+7 Retention Improved** \
    Users exposed to upadated content and well timed push notifiacation showed an approximately 20% improvement in D+7 retention compared to the baseline group.
- **Curated Course Updates had the Strongest Impact** \
    Curated courses increased the largest in engagement, with course related pageviews increasing by about 55%.
- **Push Notifications Showed Mixed but Positive Results**
    - Informational notices showed a clear increase in engagement
    - Store related pushes had limited effect
- **Daily Active Users Increased**\
    Daily Active Users increased by about 19.7% during the experiment, indicating overall app activation.

## Insights from the Data
1. Content relevance strongly influences behavior
    Interest aligned, fresh content produced consistent engagement and retention gains.
2. Update and timing combination increases revisits
    Push notifications performed best when aligned with usage peaks.
    (e.g., commute hours abd Thu-Fri pre-weekend behavior in South Korea).
3. Bookmarks & course customization require UX clarity
    High course engagement contrasted with low bookmark usage, indicating that new users did not realize courses could be saved or edited.
4. No external ads improved validity
    With no paid marketing during the experiment, retention and engagement changes could be attributed more directly to in-app updates.

## Limitations
- Retention did not continue to improve after the initial increase.
- Limited impact on deeper participation
    - Features such as course creation, reviews, and community engagement showed minimal growth.
- The lack of a randomized A/B environment limited the ability to fully isolate causal effects.
- Despite efforts to control major confounders, residual weather or behavioral variations may have influenced user activity.

## Future Improvements
- Improve UX clarity and discoverability for key actions such as saving and customizing courses to increase deeper participation.
- Introduce simple, low friction engagement features to encourage interaction.
- Run longer term experiments to measure sustained retention and daily active users and reduce short term fluctuations.
- Collect qualitative feedback through in-app prompts or short surtveys to identify barriers to user participation.