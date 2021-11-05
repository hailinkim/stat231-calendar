# Calendar Assignment: How do I spend my time?

# Introduction

In the beginning of this semester, I have been wondering how I could maximize my productivity (not just for studying, but more broadly, the activities I find meaningful) and what particular conditions enable me to spend more time on doing those meaningful activities. For the project, I intended to answer how the time I go to bed affects my studying time and how the time I wake up affect how I spend my time engaging in spiritual activities as well as studying. I also noticed the difference in my eating patterns from the previous semesters. As the College provided fridge and microwave per room due to the pandemic, I would end up cooking or more precisely, reheating the refrigerated foods and eating them in my room, instead of going to Val(the one-and-only dining hall of Amherst College) for meals. Thus, I planned to explore whether I spend more time when eating at Val or eating in my room.

---

# Motivating Questions

- How does sleep affect my productivity?
- How do I spend time eating?
- Is the type of course related to the time I spend studying for it?

---

# Data Collection

I collected data by tracking my daily schedule in Google Calendar for 26 days. To answer my questions above, I tracked my sleep, work time, spiritual activities (attending online service, listening to sermons and praying) and eating schedule. When I found out during the first phase of my data wrangling that the description feature of Google calendar could be used for my data analysis, I tried to make my entries(i.e. summary or title of an activity) general and simple for the sake of consistency and convenience of analysis and recorded different attributes in the description so I could conduct more meaningful analysis. For example, when describing what work I did, I wrote the class name in the description slot. For meals, I recorded the place I ate (Val or room) and whom I ate with (alone or friends), separated by semicolons.

# Results

## Question 1 How does sleep affect my productivity?

First, I looked at the relationship between the time I wake up and the average amount of time I spend everyday studying and doing spiritual activities. I created a contingency table where each row corresponds to whether I wake up early (before 8:30 a.m.) or late (after 8:30 a.m.) and each column represents the type of activities. The table shows that there seems to be a clear association. On a day I wake up early, I spend on average 305.91 minutes studying, which is approximately 42 minutes more than when I wake up late. For spiritual activities, I spend around 26 minutes when I wake up early, which is more than twice as much compared to when I get up late. However, I cannot conclude from this visualization that I spend more time on those activities because rising early actually boosts my productivity, or simply because I have more time during the day to get work done.

![Image](https://github.com/hailinkim/stat231-calendar/blob/main/calendar_project/images/table.png)

Looking at this table, I became interested if my bedtime would also be associated with my work time. I created a boxplot to show how the amount of time I spend studying varies with my bedtime. I considered going to bed before 1 a.m. early and after 1 a.m. late. The boxplot shows that variability of the amount of time is similar in terms of distribution, but the median time spent on studying is higher when I go to bed early than when I sleep late. While I would have more time to work when I sleep late, the actual (median) time I spent studying is less than when I wake up early. This suggests that bed time might be associated with my productivity.

![Image](https://github.com/hailinkim/stat231-calendar/blob/main/calendar_project/images/boxplot.png)
---

## Question 2 How do I spend time eating?

I created a stacked barplot that depicts whether eating alone or with others affects the amount of time I eat, and facetted it by the place I eat, to see if it has any effect on my eating time. It seems I spend so much more time–more than 200 minutes–eating with friends in my room, but, in fact, that is an outlier. I have only eaten twice with friends in my room when we cooked and watched movies together, both of which took us more than 2 hours. I also see that when I eat alone, I spend similar amount of time eating regardless of the dining area. However, more time is spent when I eat with friends both in Val and my room. This means that it is whom I eat with, not where I eat, that works as a factor that affects my eating time.

![Image](https://github.com/hailinkim/stat231-calendar/blob/main/calendar_project/images/barplot.png)

I also wanted to explore the relationship between eating regular meals and my productivity, though not addressed in the initial questions of interest. Often when I skipped meals to get work done, I rather found myself snacking and binging in my room, only to feel bad and lose productivity. That being said, I expected that there would be a negative association between time gap between meals and productivity. However, the scatterplot shows that it is exactly the opposite. With the correlation coefficient of 0.34, they have a positive, albeit weak, relationship. Does this really mean I become more productive if I skip meals? While I tracked the duration of studying to measure productivity, it might not accurately represent that information because the time I was distracted was not excluded accurately. When I skipped meals (and fell into the vicious cycle of binge-eating), I might have had more time to study and actually ended up spending more time studying (possibly by reducing sleep) to compensate for the wasted time, but that would not necessarily mean I was feeling more productive.

![Image](https://github.com/hailinkim/stat231-calendar/blob/main/calendar_project/images/scatterplot.png)
---

## Question 3 Is the type of course related to the time I spend studying for it?

This question is not included in my initial research questions, but as the semester progressed, I found myself spending disproportionately more time studying for my POSC course than the other two STEM courses(CS and Data Science). This led me to wonder if the the course type is actually associated with how I spend time studying. In order to investigate that relationship, I first created a line graph showing the amount of time I study each day for each course I am taking this semester. It shows that except for Thursday, I constantly invest my time in studying for POSC class throughout the week. That would be because being a slow reader, I split up the workload to finish 100-page readings assigned for every class. Thursdays are an exception because once I am done with the class on Wednesday, I choose to allocate my Thursdays to study for other courses. Though the graph shows that I also work on Data Science quite constantly throughout the week, I tend to spend more time working on the POSC each day. And for Data Science, I work the most on Fridays presumably because we have problem sets due every Friday. I seem to do the most work on Thursdays for CS because we have homeworks due Friday mornings. However, I see that I do not devote as much time to CS for the rest of the week.

![Image](https://github.com/hailinkim/stat231-calendar/blob/main/calendar_project/images/timeseries.png)

As mentioned above, I divide up the workload for my POSC class because I often find non-STEM courses more challenging than STEM courses. And I wanted to confirm if my data captures my anxiety about non-STEM courses. I looked at the distribution of the time I spent studying in one sitting by course types– STEM and non-STEM. Although there is more variation in study time for STEM courses, the median time is higher. On the contrary, the entire distribution of time spent studying for non-STEM courses lies at and even below the bottom end of the distribution for STEM classes. This validates that I tend to have poor concentration when I work on my POSC course.

![Image](https://github.com/hailinkim/stat231-calendar/blob/main/calendar_project/images/boxplot2.png)

In general, sleep does affect my productivity in that waking up early and going to bed early seems to enables me to dedicate more time to the activities I find meaningful, in addition to my academics. While I expected that I would spend more time eating when I eat in my room than in Val because I need to cook and wash dishes, dining area does not seem to really matter according to the stacked barplot; instead, the average duration of having meals is much higher when I eat with others. Additionally, visualizations convey that my study time varies with which course I am working on. The line graph validates my feelings that the amount of time I spend on POSC course is disproportionate(because I split up the workload for the course throughout the week), and the boxplot confirms I tend to show poor concentration when I study for POSC, unable to work longer than 100 minutes in one sitting.

---

# Reflection

Collecting my daily schedule data was insightful but definitely challenging at times. I had planned to track time spent eating and talking with friends separately when I eat with friends, but the distinction was not clear and I ended up recording the total amount of time I spent eating each meal. I also had tried to keep track of dish-washing time for each meal when I eat in my room, but I was not always able to do the dishes immediately after eating each meal if I had meetings or classes afterwards and did them all at once a few times a week. To address this issue, I calculated the overall average time spent washing dishes and added it manually to the data set.

Another challenge when analyzing my study time was taking into account the consistency. When I tried to calculate the average time I worked on each course for each day of week, I observed that the mean time spent studying for CS was much higher than for the POSC course, even though I was certainly dedicating more time to the POSC course. This was because the mean was not weighted–for CS, the sum and mean time on a particular day was equal because I have studied for CS on that day only once throughout the entire data collection period, while I worked on POSC on that day every week. To solve this issue, I had to manually add the rows with duration of 0 for the days I did not work on a particular course and weight the average based on those rows.

The scatterplot depicting the relationship between time gaps between meals and productivity failed to prove my hypothesis that eating regular meals would positively affect my productivity. This may be due to the fact that I lacked data to control for a potential confounding variable: the actual level of productivity. I tracked the time I actually concentrated as best as I can as a measure of productivity, it might not be accurate because I was not able to measure every single time I got distracted in between. For future data collection, I would consider the quality of work being produced or the proportion of time wasted out of the total intended work time as my productivity variable. Yet, it would be quite challenging to collect the quality of work being done because it is such subjective, not to mention qualitative, data. Additionally, if I could redo this project, I would collect data over a longer period of time and run significance tests so that I can make conclusions about statistically significant results.

## Ethical Consideration

As someone who provides data, I expect that my data is treated with ethical considerations. I expect that my data is kept confidential and anonymous so that it cannot be traced to its provider. In order to ensure privacy of my data, I hope that data usage and any information gathered in the data analysis procedure are clearly communicated to me.

As a data analyst, I think it is imperative to be aware of ethical implications of my analysis, given the privacy and sensitivity of the data. It is important to communicate the use of data and obtain informed consent from the data provider. I would also have to be very cautious about my personal opinions or bias that might get in the way of accurate data analysis procedure.