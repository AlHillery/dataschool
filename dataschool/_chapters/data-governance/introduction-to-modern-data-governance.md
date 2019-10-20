---
section: book
title: Introduction to Modern Data Governance and the 4 Stages of Sophistication
meta_title: Stages of Data Sophistication and Modern Data Governance
description: Learn how Data Governance practices change as the level of data sophistication changes.
number: -10
authors:
- _people/dave.md
reviewers:
- _people/matt.md
feedback_doc_url: ''
image: "/assets/images/data sopistication stack.png"
is_featured: false
img_border_on_default: false
is_under_construction: false
is_community_story: false
story_intro_blurb: ''
reading_time: 4

---
Modern companies run on and compete with data.  Historically businesses had all of the information they needed walking in and out of their store every day.  When customers had requests, or frustrations, or buying patterns - the owners and employees were there to ask about them and to directly observe trends.

Over time, companies scaled and most people work for larger, distributed organizations.  We've grown from single shop businesses, to having many locations, and increasingly even having no locations.  Decision makers don't have direct access to each customer, and must increasingly rely on their data to improve and compete.

Companies today are quite good at collecting data - but still very poor at organizing and learning from it.  Setting up a proper Data Governance organization, workflow, and data stack are essential if a buisness wants to gain visibility into it's information.

This book is for those organizations that want to gain best practices and visibility into their data.  It is a continually improving community driven book teaching Modern Data Governance techniques for companies at different levels of data sophistication. It progresses from the starting setup of a new startup to a mature data driven enterprise covering architectures, tools, team organizations, common pitfalls and best practices as your data needs expand.

The structure and starting chapters of this book were written by the leadership and Data Advisor teams at Chartio, from the experiences working with hundreds of companies over the past decade.  We continually work with companies, educating them through pitfalls and toward best practices as their needs evolve and have compiled our learnings and open sourced them in this book.


## The 4 Stages of Data sophistication

From this experience we recognized four distinct stages of data sophistication. These stages happen to be tied to a new  piece of the data stack needed at each stage, and so we have named these stages after those pieces.  

This book is organized by these 4 sequential stages which are:

1. Source
2. Lake
3. Warehouse
4. Mart

![Ideal data stack for effective data governance](https://lh3.googleusercontent.com/vG0lYBnPTtL9BCt4qn1lhoBvYvAWRAw21_R9C-U5Lu-q_5tmPzIBfdcuA2MGXF7CyX9VFM1OTKJp4rLoSCNJDuNHQpceM_CcihX1LefCw2tovbrhHtmQkYbZr56UEJctIBva9QbT)

Each vertical stage in the above diagram is a valid stack to operate from, depending on your resources, size, important and needs of data within your organization.

As a growing company's data needs expand, it will be incredibly valuable — and perhaps pivotal — to advance all the way through each of these stages to the Mart stage.

We'll start with an overview of each of these stages:

### Stage 1. Sources

![](https://lh4.googleusercontent.com/gQGOiX-JT7DSLZLlkT0fDUfdZm2nITUw6pSF2SrOrmac7mq7HxF-U2bYf5O8uDP-Id9Tay_1k8S1h87iHZLedkpJNYWJABORVnNw9v8AotkwEN1O2KXcsvkYR9IU4kbylh4G5CBE)

When you start working with data, you may only have a few sources of interest. Two common early sources are Google Analytics and your application data in whatever PostgreSQL or MySQL database your product runs on. If only a few people at your company need to work with these sources, you might set them up with direct access; it’s more simple and agile for them to just work with the data directly.

### Stage 2. Lake

As you start to rely on more data sources, and more frequently need to blend your data, you’ll want to build out a Data Lake—a spot for all of your data to exist together in a unified format.

![](https://lh6.googleusercontent.com/45iVlzJHp2uIt3rtQxu3KpIGoJIJ1iqTf25p3nU33reggsJDGm9JZyM908pA3x1ugaDWiDXYjSGg72uSRB1MyAKmcXLbT2hhz7jWlPkWp3pPXlav_fc80Vtko3lmgFLOjROkUNXZ)

Especially when you need to work with data from applications like Salesforce, Hubspot, Jira, and Zendesk, you’ll want to create a single home for this data so you can access all of it together and with a single SQL syntax, rather than many different APIs.

### Stage 3. Warehouse (Single Source of Truth)

In the Lake stage, as you bring in more people to work with the data, you have to explain to them the oddities of each schema, what data is where, and what special criteria you need to filter by in each of the tables to get the proper results. This becomes a lot of work, and will leave you frequently fighting integrity issues. Eventually, you’ll want to start cleaning your data into a single, clean source of truth.

![](https://lh3.googleusercontent.com/IIYi4iD4oQgw4CKdR5EAHWXx1MfEuRXCK7gFCx_9Ved3L5hhiSqoNV7p4iqYMwR2Dwfa5_nW4kN6Yx-iTNm_jz63tj0LURWpjiWhmhnkeoMyM5w6FK79z0yTxrXzPn50zDzAAm5G)

This stage—creating a data Warehouse—has historically been quite a nightmare, and there are many books written on how best to model your data for analytical processing. But these days it’s not that hard—and will not only spare you from having to explain all of your schemas’ oddities to new team members, but will also save you as an individual time in having to repeat, edit and maintain your own messy queries.

### Stage 4. Marts

When you have clean data and a good BI product on top of it, you should start noticing that many people within your company are able to answer their own questions, and more and more people are getting involved. This is great news: your company is getting increasingly informed, and the business and productivity results should be showing. You’re also less worried about integrity issues because you’ve modeled the data, and you’re continually maintaining it to be a clean, clear source of truth.

Eventually, however, you’ll have hundreds of tables in that source of truth, and users will become overwhelmed when trying to find the data that’s relevant to them. You may also discover that, depending on the team, department, or use case, different people want to use the same data structured in different ways. For these reasons, you’ll want to start rolling out Data Marts.

![](https://lh3.googleusercontent.com/1E7D3_diPh5wYiEElr6_sQeY6qIV0Ri5nkC4LIqm_x5O9jJV_5hODDbdOZWHa8nKl_VcR7CbT_nbXvhRuDkzrOOV3amkVdu41zSeAtHEd-r6yPOqTaRI09ISxDn1rvTOGqjqFdRa)

Data Marts are smaller, more specific sources of truth for a team or topic of investigation. For example, the Sales team may only need 12 or so tables from the main Warehouse, while the Marketing team may need 20 tables—some of them the same, but some different.