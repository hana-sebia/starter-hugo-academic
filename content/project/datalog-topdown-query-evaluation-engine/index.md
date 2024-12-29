---
title: The Top Down Query Evaluation Engine for DataLog
summary:  A Top down recursive query processing method for DataLog, implemented in Java.
tags:
  - Deductive reasoning
date: '2021'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption:
  focal_point: Smart

url_code: 'https://github.com/hana-sebia/datalog-topdown-query-evaluation-engine'
url_pdf: 'uploads/datalog_recursive_query_processing.pdf'
url_slides: 'uploads/datalog_slides.pdf'
url_video: ''

---

Recursive query processing methods can be broadly categorized as either bottom-up methods, or top-down methods. Bottom-up methods
answer a query by applying all rules of a program to ground tuples, deriving tuples that satisfy rule bodies into predicates in rule heads.
The minimal model for the given program and ground tuples is explicitly materialized as a new database instance; the answer to the query is
then obtained through a simple select/project/join operations over the materialized database instance. In contrast, top-down methods answer
a query by pushing selection criteria (i.e. constants) from the query down into rules that may answer the query (i.e. rules deriving into
predicates being queried), creating more (sub)queries from the atoms of these rules’ bodies; the subqueries are in turn answered in a sim-
ilar, top-down fashion. In this project, we implement a representative method for the top-down evaluation : query/subquery (QSQ).