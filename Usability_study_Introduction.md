# Motivation

Data surrounds us every day. Scientists, cities, and companies all collect data (e.g. about weather, traffic, books, or research).  
But before we can use any of this data for experiments, analysis, or machine learning, we have to **find it** and **understand what it contains**.  
Sometimes that is harder than it sounds. Many datasets are shared online with very little explanation. Without knowing who made them, what they describe, or whether we can reuse them, they remain hidden and unused.

---

## What Is a Knowledge Graph?

A **knowledge graph** is a specific type of dataset that stores information as connections between things.
Each piece of information is a small fact that links one thing to another.

Look at the example below:
![Knowledge Graph Example](https://github.com/marmhm/KG-metadata-tool-usability-study/blob/main/graph_example.jpg?raw=true)


In this graph:

Leonardo da Vinci painted The Mona Lisa.

The Mona Lisa is located in the Louvre Museum.

Leonardo da Vinci was born on April 15, 1452, and is an Artist.

Each arrow represents a relationship between two things, forming a network of linked facts.
When many of these small connections come together, they create a web of knowledge that computers can also understand and search.

So, a knowledge graph is simply a way to organize data as relationships, not just as rows and columns. It helps both humans and machines explore how pieces of information are related.

---

## Metadata

To make a dataset useful, we need to describe it clearly. This description is called **metadata**.  
Metadata tells others the **title**, **creator**, **language**, **keywords**, and **purpose** of the dataset.  
For knowledge graphs, it can also include special details such as example queries or links to related data. The complete list of these elements are listed and describes in Knowledge graph metadata specification.

> Good metadata helps others and even search engines discover and reuse datasets.  
> Without it, valuable work can be lost or overlooked.

---

## The metadata specification you will use

For this study you will receive a specification that lists the elements we expect you to fill. Think of it as a checklist. It keeps everyone consistent and makes the descriptions machine readable.

Typical elements in the schema:

Title

Description

Keywords

Languages

Creator and publisher details

Roles (role type and the agent, for example name and email or agent IRI)

Access rights and license

Theme or category (as an IRI where possible)

Sources and linked resources (IRIs for external datasets)

Distribution information (download and access URLs, media type)

SPARQL endpoint information (endpoint URL, identifier, title, short description, status)

Example resource (a concrete URI that shows the pattern)

Example queries (short SPARQL examples where relevant)

The schema states which elements are required and which are optional. It also shows the expected value type. For example, a title is free text, a theme is an IRI, a date follows the date format, and a distribution has specific subfields.

## How We Describe a Knowledge Graph

Traditionally, people write metadata using a simple data language called **Turtle**.  
It looks a little like short sentences that a computer can read, such as:

```turtle
@prefix ex: <http://example.org/> .

ex:HarryPotter a ex:Book ;
    ex:title "Harry Potter and the Sorcerer’s Stone" ;
    ex:author "J.K. Rowling" .
```

This means:  
“Harry Potter is a book. Its title is *Harry Potter and the Sorcerer’s Stone*. Its author is *J.K. Rowling*.”

Writing in Turtle makes metadata **machine-readable**, so other systems can automatically find and understand datasets.

---

## What You Will Do in This Study

In this study, you will work with **three different tools** to describe three knowledge graphs (KGs).  

We provide you with:
- **Three short documents** written in natural language. Each one describes a different knowledge graph and includes all the information needed to create its metadata.  
- **A metadata specification** (schema) that lists the elements you should describe, such as title, description, keywords, languages, creator, access rights, and other KG-specific details like example queries or linked resources.

You will use the three tools to transform the same information from the natural language document into a **machine-readable format** (Turtle).  
Each tool lets you do this in a different way.

---

### Tool 1 – Turtle Editor

This tool provides a **text editor** with Turtle syntax validation.  
Here, you will manually create the metadata in Turtle format.

**Steps:**
1. Skim the KG documentation to understand what it describes.  
2. Open the metadata schema checklist and note which elements you must include.  
3. Gather exact values, such as IRIs for themes, sources, and linked resources when available.  
4. Map each element from the schema to a simple Turtle statement, keeping the format short and consistent.  
5. Use the editor’s validation to check that your Turtle is syntactically correct.

*Example screenshot of Tool 1:*
![Tool 1 Screenshot](images/tool1_editor.png)

---

### Tool 2 – Form Interface

In this tool, you will describe the same KG using a **web form**.  
You do not need to write any Turtle syntax — the form automatically converts your answers into valid Turtle.

**Steps:**
1. Skim the KG documentation.  
2. Fill in the field values according to the metadata specification.  
3. Review how the form displays your data as generated Turtle code.

*Example screenshot of Tool 2:*
![Tool 2 Screenshot](images/tool2_form.png)

---

### Tool 3 – LLM-Assisted Form

The third tool uses **AI assistance** to help you fill the metadata form.  
You will upload the natural-language KG document, and the tool will generate **AI suggestions** for each metadata field.

**Steps:**
1. Upload the KG documentation.  
2. Click on each metadata field to view the AI suggestions.  
3. Review the suggestions, and either accept or edit them before adding them to the form.  
4. When the form is complete, the system will produce the machine-readable Turtle version automatically.

*Example screenshot of Tool 3:*
![Tool 3 Screenshot](images/tool3_llm.png)

---

### After Completing the Tasks

After trying each tool, you will complete a short questionnaire about your experience.  
You will be asked how easy each tool was to use, how helpful it felt, and what could be improved.  

Your feedback will help us understand which approach makes metadata creation most efficient and user-friendly.


After trying each tool, you will complete a short **questionnaire** to share your experience — how easy it was to use, what you liked, and what could be improved.

---

## Why Your Participation Matters

Your feedback will help us understand how ow users perceive, use, and benefit from each tool and to what extent AI assistance is helpful in metadata creation. 

> Thank you for being part of this study.  

