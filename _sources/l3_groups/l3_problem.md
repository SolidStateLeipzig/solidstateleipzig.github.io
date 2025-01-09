---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.4
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Example problem

```{code-cell} ipython3
:tags: [remove-cell]

import sys

sys.path.append("../pycode")

from multiplechoice import MultipleChoice

```


```{code-cell} ipython3
:tags: [remove-input]

question = (
    "How would the topological degeneracy of the ground state that comes from the loop configurations "
    "change if we put it on a torus (donut) with two holes?"
)

answers = [
    "Since there is still an infinite number of loop configurations, the degeneracy would be infinite.",
    "Since there is one additional hole there are two more distinct cycles. "
    "So  the number of ground states increases by a factor of 4.",
    "It still remains 4 since the loops is topologically forbidden from going around the extra loops.",
    "Since there is one additional hole the loops can go around this hole an even or an odd number of time, "
    "so the degeneracy increases from 4 to 8.",
]

explanation = ("Explanation")

MultipleChoice(
    question=question, answers=answers, correct_answer=1, explanation=explanation
)
```