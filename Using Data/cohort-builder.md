---
order: 100
---
# Cohort Builder

The Cohort Builder is a tool in the **Reporting Compatibility** module \(included with most OpenMRS installations\) that lets you perform ad-hoc queries for patients with defined characteristics, and combines multiple queries into more complex ones.

A cohort query returns a list of patients matching the specified criteria. Cohort Builder cannot create lists of data elements other than patients. For example, you can use the cohort builder to search for all patients with any weight observation &gt; 70, but it is not possible to create a list of all observations of weight &gt; 70.

To use this tool, click **Cohort Builder** at the top of any page.

## Cohort definitions, cohorts, and search history

Each **Patient Search** is added to your search history. This history is preserved until you choose to clear it or the web application is restarted. You may also save your search history to preserve it for future re-use.

You may save any search \(simple or combined\) as a **Cohort Definition** to make it easier to re-run that same search in the future. When you save a combined search, it includes copies of all its component searches.

You may also save the list of patients resulting from a query as a **Cohort**. The list of members in a saved cohort will never change. On the other hand, running a saved search again may produce new results.

The initial screen of the cohort builder contains several sections:

1. The top tabs allow you to run different kinds of queries.

2. Each query you perform goes into the search history.

3. The **Save**, **Load**, and **Clear** buttons help keep your entire search organized.

4. After running a query, cohort members are displayed here.

5. Click this **Save** button to save this cohort for future re-use.

6. Click these **Save** buttons to save a previous query as a cohort definition for future re-use.

7. Use the link at the top of the cohort builder to load saved cohorts and cohort definitions.

![](/assets/cohort-builder-overview.png)

## Searching by observation

To search for patients who have observations matching certain criteria, choose the **Concept/Observation** tab. Start typing the name of a concept that you want to search for [1], and choose that concept from the search results [2].

If you choose a concept whose datatype is anything other than N/A, you can search for observations whose question is the concept you selected [3]. Depending on the datatype, you can limit this to a numeric or date range, or to specific coded answers. You can also choose which observations you are looking for (first, last, min, max, any, none) or combine (average), and you can specify date ranges.

This example will build a cohort of patients whose last systolic blood pressure measurement was above 130 mmHg:

![](/assets/cohort-builder-obs-question.png)

You can also search for any observations that have your chosen concept as an **answer**. \(You'd typically use this for doing a highly selective search, which you'll later filter down to something more specific.\)

In this example we search for patients who have any observation whose answer is Hypertension, which might include both confirmed diagnoses of hypertension as well as consults to rule out Hypertension:

![](/assets/cohort-builder-obs-answer.png)

## Searching by demographics

Select the **Patient Attributes** tab to search based on simple demographic characteristics: gender, age, birthdate, and vital status.

In this example, we search for living male patients between 45 and 65 years old: 

![](/assets/cohort-builder-demographics.png)

## Searching by encounters

Select the **Encounters** tab to search for patients based on encounters they have had. You can search by encounter type \(control-click to select multiple types\), location, the form with which the encounter was recorded, date ranges, and the number of matching encounters to look for.

In this example we search for patients who have had at least 3 encounters whose types were either ADULTINITIAL or ADULTRETURN:

![](/assets/cohort-builder-encounters.png)

## Searching by program enrollments

Select the **Program Enrollment** tab to search for patients enrolled in a particular program, or patients who have a particular status.

In this example, we search for patients who have ever been in the Hypertension Program:

![](/assets/cohort-builder-program.png)

## Combining searches

After you have done several searches, the **Composition** tab allows you to combine them using Boolean algebra. You can use AND, OR, NOT, or parentheses to build complex combinations of the other searches in your history. Refer to your previous searches using the number next to them in the **Search History** section.

Here, we search for patients who match a combination of the previous example queries:

![](/assets/cohort-builder-composition_1.png)

