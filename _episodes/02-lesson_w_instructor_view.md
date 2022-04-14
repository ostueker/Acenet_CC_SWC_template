---
title: "Episode with instructor notes"
teaching: 1
exercises: 0
questions:
- "Can we combine longer texts for self-study with concise instructor notes for presentation?"
objectives:
- "Add a toggle-switch to flip between two modes."
- "Create a lesson that has both full-length text and bullet-lists with talking points."
- "Some paragraphs, code and diagrams should remain visible in both modes."
keypoints:
- "We can have custom elements to mark paragraphs as either 'self_study_text' or 'instructor_notes'."
- "A toggle switch can switch between them."
- "Adding some additional CSS and JavaScript to the template will facilitate this feature."
---

## Section 1
Some lessons are rather complex and require a lot of information.

This is a long text that describes a complex topic in detail. 
This contains information that the instructor explains in detail. 
However, large blocks of text make it difficult to use these pages instead of slides during a lesson
or workshop as there is too much text for the attendees to read and for the instructor to pick out
the talking points.  
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut_
_labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris_
_nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate_
_velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non_
_proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
{: .self_study_text :}

* talking points for instructor
* easier to read during the workshop
{: .instructor_notes :}

Some text should be visible in both modes.

~~~
$ echo "Code will stay the same"
~~~
{: .language-bash }


<div class="mermaid">
graph LR
    A[Complex topic] -->|convert to| B(Lesson material)
    B --> C{How is<br />the material<br />used?}
    C -->|for self-study| D[present whole text<br />with links to further reading.]
    C -->|within workshop| E[present a short version<br />with bullet points]
</div>


* Toggle switch is in the navbar and only visible if the page contains at least
  one element of either 'self_study_text' or 'instructor_notes'.

* Store state of toggle-switch as a cookie and restore the state from there.
  (The cookie should have a relatively short lifetime of maybe a few days only.)

{% include links.md %}
