# Motivation

Data surrounds us every day. Scientists, cities, and companies all collect data (e.g. about weather, traffic, books, or research).  
But before we can use any of this data for experiments, analysis, or machine learning, we have to **find it** and **understand what it contains**.  
Sometimes that is harder than it sounds. Many datasets are shared online with very little explanation. Without knowing who made them, what they describe, or whether we can reuse them, they remain hidden and unused.

---

## What Is a Knowledge Graph?

A **knowledge graph** is a specific type of dataset that stores information as connections between things.
Each piece of information is a small fact that links one thing to another.

Look at the example below:
![Knowledge Graph Example](graph_example.png)

In this graph:

Leonardo da Vinci painted The Mona Lisa.

The Mona Lisa is located in the Louvre Museum.

Leonardo da Vinci was born on April 15, 1452, and is an Artist.

Each arrow represents a relationship between two things, forming a network of linked facts.
When many of these small connections come together, they create a web of knowledge that computers can also understand and search.

So, a knowledge graph is simply a way to organize data as relationships, not just as rows and columns. It helps both humans and machines explore how pieces of information are related.

---

## Why Metadata Matters

To make a dataset useful, we need to describe it clearly. This description is called **metadata**.  
Metadata tells others the **title**, **creator**, **language**, **keywords**, and **purpose** of the dataset.  
For knowledge graphs, it can also include special details such as example queries or links to related data.

> Good metadata helps others — and even search engines — discover and reuse datasets.  
> Without it, valuable work can be lost or overlooked.

---

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

In this study, you will work with **three different tools** to describe a few knowledge graphs. We provide you three documents that they describe the Knowledge graphs in natural language format.  
Each tool approaches the same task in a different way.

### Tool 1
Describe a knowledge graph directly in **Turtle syntax**.  
This helps you see how machines read structured data.

### Tool 2
Fill out a simple **form** to describe the same information without writing any code.

### Tool 3
Upload a **document**, and the tool will show you **AI-generated suggestions** for each field.

After trying each tool, you will complete a short **questionnaire** to share your experience — how easy it was to use, what you liked, and what could be improved.

---

## Why Your Participation Matters

Your feedback will help us understand how ow users perceive, use, and benefit from each tool and to what extent AI assistance is helpful in metadata creation. 

> Thank you for being part of this study.  

