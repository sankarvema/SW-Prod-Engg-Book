# DRY (Don't repeat yourself)

The DRY principle is stated as "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system".

Violations of DRY are typically referred to as WET solutions, which is commonly taken to stand for either "write everything twice", "we enjoy typing" or "waste everyone's time". WET solutions are common in multi-tiered architectures where a developer may be tasked with, for example, adding a comment field on a form in a web application. The text string "comment" might be repeated in the label, the HTML tag, in a read function name, a private variable, database DDL, queries, and so on. A DRY approach eliminates that redundancy by using frameworks that reduce or eliminate all those edit tasks excepting the most important one, leaving the extensibility of adding new knowledge variables in one place.
