---
layout: pattern
title: Identity Map
folder: identity-map
permalink: /patterns/identity-map/
categories:  Object-Relational Behavioral
tags:
 - Relational
---

## Intent
Ensures that each object gets loaded only once by keeping every loaded object in a map. Looks up objects using the map when referring to them.
An Identity Map keeps a record of all objects that have been read from the database in a single business transaction. Whenever you want an object, you check the Identity Map first to see if you already have it.

## Class diagram

![uml](etc/map.png)

## Applicability
* The idea behind the **Identity Map** pattern is that every time we read a record from the database, we first check the Identity Map to see if the record has already been retrieved. This allows us to simply return a new reference to the in-memory record rather than creating a new object, maintaining referential integrity.

- A secondary benefit to the **Identity Map** is that, since it acts as a cache, it reduces the number of database calls needed to retrieve objects, which yields a performance enhancement.

## Credits

* https://www.sourcecodeexamples.net/2018/04/identity-map-pattern.html
