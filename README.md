# 🎓 AI Project – Degrees(BFS)

## 🧩 Overview

This project explores the concept of "Six Degrees of Separation" in Hollywood, where any actor can be connected to another through shared movie appearances. Using **Breadth-First Search (BFS)**, the program finds the shortest path between two actors based on their co-starring roles.

## 📂 Files

- `degrees.py`: Main program to run the search
- `util.py`: Contains the QueueFrontier and Node classes
- `data/`: Contains CSV files with actor and movie data

## 🚀 Usage

Requires **Python 3** to run.

### Run with Small Dataset

```bash
$ python degrees.py small
```
## Run with Large Dataset
```
$ python degrees.py large
# OR
$ python degrees.py
```
## 🧠 Problem Description
```
$ python degrees.py large
Loading data...
Data loaded.
Name: Emma Watson
Name: Jennifer Lawrence
3 degrees of separation.
1: Emma Watson and Brendan Gleeson starred in Harry Potter and the Order of the Phoenix  
2: Brendan Gleeson and Michael Fassbender starred in Trespass Against Us  
3: Michael Fassbender and Jennifer Lawrence starred in X-Men: First Class
```
## 🔍 Search Model  
States: Actors  
  
Actions: Movies connecting actors  
  
Initial State: Source actor  
  
Goal State: Target actor  

## 📐 Specification  
Implement the shortest_path(source, target) function to return the shortest path from the actor with ID source to the actor with ID target.  

### Return Format  
A list of (movie_id, person_id) tuples representing each step in the path.
```
[(1, 2), (3, 4)]
```
### This means:

- Source starred in movie `1` with person `2`  
- Person `2` starred in movie `3` with person `4`  
- Person `4` is the target  

---

### Edge Cases

- If multiple shortest paths exist, return any one.  
- If no path exists, return `None`.  

---

## 🛠️ Helper Function

You may use:

```
neighbors_for_person(person_id)
```
Returns a set of `(movie_id, person_id)` pairs for all people who starred in a movie with the given person.

> ⚠️ Only modify the `shortest_path` function. You may write additional helper functions or import standard Python modules.
---
Jai Hanuman
