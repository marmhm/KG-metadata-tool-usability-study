# Introduction to Turtle (TTL) for Knowledge Graphs

When we talk about the **Semantic Web** and **Knowledge Graphs**, we often need a way to describe data in a simple, structured form. One of the most widely used formats is **Turtle (TTL)**.

Turtle is short for *Terse RDF Triple Language*. Despite the long name, the idea is actually straightforward: it lets us write down information as **triples** — a subject, a predicate, and an object. Think of it as saying:

👉 **Thing – has property – value**

---

## 1. Describing Data as Triples

Let’s start small. Here’s a single triple in Turtle:

```ttl
ex:Book1  ex:title  "The Hobbit" .
```

This line says: **Book1 has the title “The Hobbit.”**

Notice the period (`.`) at the end — every triple ends with one.

---

## 2. Using Prefixes

Writing full web addresses (URIs) every time would be painful. That’s why Turtle uses **prefixes** to shorten them.

```ttl
@prefix ex: <http://example.org/> .

ex:Book1 ex:title "The Hobbit" .
```

Here, `ex:` stands for `http://example.org/`. So `ex:Book1` is just a shorthand.

---

## 3. Declaring Types

We often want to say *what kind of thing* something is. In Turtle, we use `a` for that.

```ttl
ex:Book1 a ex:Book .
```

This simply means: **Book1 is a Book.**

---

## 4. Adding More Details

A subject usually has more than one property. Turtle allows us to stack them neatly with semicolons:

```ttl
ex:Book1 a ex:Book ;
         ex:title "The Hobbit" ;
         ex:author "J.R.R. Tolkien" .
```

The semicolon (`;`) keeps the subject the same, so we don’t need to repeat `ex:Book1`.

---

## 5. Multiple Values

Sometimes one property has multiple values. For example, a book may belong to more than one genre:

```ttl
ex:Book1 ex:genre "Fantasy" , "Adventure" .
```

The comma separates multiple values for the same property.

---

## 6. Typed Values: Dates and Numbers

Not all data is plain text. Dates and numbers can be written with datatypes.

```ttl
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

ex:Book1 ex:published "1937-09-21"^^xsd:date ;
         ex:pages 310 .
```

Here:
- `"1937-09-21"^^xsd:date` means a date value.
- `310` is a number (no quotes needed).

---

## 7. A Complete Knowledge Graph Example

Now let’s put everything together. We’ll describe a dataset, the person who created it, and a related publication.

```ttl
@prefix ex:  <http://example.org/> .
@prefix dct: <http://purl.org/dc/terms/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

# A dataset
ex:Dataset1 a dct:Dataset ;
    dct:title "Air Quality Data Berlin 2021" ;
    dct:creator ex:Person1 ;
    dct:dateCreated "2021-09-10"^^xsd:date ;
    dct:subject "Environmental Data" ;
    dct:relation ex:Publication1 .

# The person who created it
ex:Person1 a dct:Agent ;
    dct:title "Dr. Anna Müller" .

# A related publication
ex:Publication1 a dct:BibliographicResource ;
    dct:title "Air Pollution Trends in European Cities" ;
    dct:issued "2022"^^xsd:gYear .
```

---

✨ That’s Turtle in a nutshell: triples, prefixes, types, and a few handy separators (`.`, `;`, `,`).  
With these basics, you can describe almost anything in a structured, machine-readable way.
