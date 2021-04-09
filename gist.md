# **RegEx Tutorial**

RegEx (Regular Expressions) can be one of the many steps apps take to validate information users are entering into the database. At first glance, they may look like a toddler got a hold of a keyboard, but there is a method to the expressions that can be easy to understand with the right resources along with some practice.

## **Summary**

In this tutorial, we will be looking at regex expressions that validate emails. 

These could look like:
* /([a-z0-9_.-]+)@([\da-z.-]+).([a-z]{2,3})/
* /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/
* /^[a-zA-Z0-9_-]{0,}([.]?[a-zA-Z0-9]{1,})@(gmail|hotmail|yahoo).com$/

If interested in testing these out, check out [regexr.com](regexr.com). This is a great tool for testing out regex in real time. It comes with a very helpful cheatsheet! If testing multiple examples like this image, checking the "global" and "multiline" flags and selecting the "List" tool is recommended.

![screenshot of regexr](./assets/regexrscreenshot.png)

## **Table of Contents**

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)


## **Regex Components**


### **Anchors**
"^" At the start (Example: ^hot will match any string that starts with "hot")

"$" At the end (Example: mail$ will match any string that ends with "mail". This could include "hotmail" or "gmail", etc.)

**In the second example in the summary**
* /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/

The "^" requires a word to follow signified by the "\w"

The "$" at the end requires one or more "(\.\w{2,3})" which is a grouping that would include something like ".com", ".org" or ".co"; the "+" following the group in parenthesis is a quantifier and will be covered in that section.

**In the third example in the summary**
* /^[a-zA-Z0-9_-]{0,}([.]?[a-zA-Z0-9]{1,})@(gmail|hotmail|yahoo).com$/

We use the "$" to be extra specific requiring the user to have a gmail, hotmail or yahoo email account.



### **Quantifiers**
**"*", "+", "?", "{}"**\

"*" Will match zero or more of the preceding value. "{0,}" Will do the same, so these values are interchangeable. For example "com{0,}" will match a string that has "co" followed by zero or more "m". If we were to remove the comma, "com{0}", this would contradict the "m" and would only match "co". So the comma is the "or more" expression here.

"+" Will match one or more of the preceding value. "{1,}" Is interchangable in this case. For example "com+" or "com{1,}" would match "com", "comm" or even "commmmmmm", but not "co".

"?" or "{0,1}" Will match zero or one of the preceding value. "com?" Would match either "com" or "co", but not "commm" in this case.

**We use a combination of all of these in the summary codes, but here are a couple key examples
* "([a-z]{2,3})" will match lowercase strings like "com", "co", "org" and "net", but not "c" or "nett"
* "\w+" will match lowercase letters with one or more lowercase letters after



### **OR Operator**

### **Character Classes**

### **Flags**

### **Grouping and Capturing**

### **Bracket Expressions**

### **Greedy and Lazy Match**

### **Boundaries**

### **Back-references**

### **Look-ahead and Look-behind**

## **Author**

**Alex Christopherson**

Full Stack Developer

* GitHub: [albenchris](https://github.com/albenchris)
* LinkedIn: [Alexander Christopherson](https://www.linkedin.com/in/alexander-christopherson-2b32085a/)
* Email: albenchris00@gmail.com