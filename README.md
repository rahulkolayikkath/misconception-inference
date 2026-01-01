# misconception-inference
This is a repo to measure how effectively Frontier LLMs can capture student misconception from Image of student answer.
For probelms in maths and science.

Q) Why language models can't always capture incorrectness in student reasoning ?
Ans: 
LLMs are trained with high quality reasoning traces that lead to correct answer. In our scenario , we require models to figure out how reasons can be wrong. 
In simple terms if you want to understand the incorrectness in student answer you should also know how to think like them and know its wrong at the same time.
Knowing the correct answer alone is not enough to judge the misconception..
Language models can maybe solve it, but it doesn’t make them good evaluators 

Q) Why does language models bad at verifying complex math? 
Ans: 
LLMs struggle at calculating. Modern Agents have access to tools like a calculator but native base models just predicts the next token. Lack of verifiers. Verification can be done with tool use like calculators or programatically using Math modules in code. 

Idea of Math-Varify
When asked to verify 
5x + 2x = 14
7x  = 14 
x = 2

| Exp 1      | Exp 2   | Verify   | Result |
| ---------- | ------- | -------- | ------ |
| 5x+2x = 14 | 7x = 14 | 5+2 = 7  | True   |
| 7x = 14    | x = 2   | 14/7 = 2 | True   |
|            |         |          |        |
