# 1. which problem(s) gave you the most trouble? Did you avoid any problem that is too challenging to finish by deadline? Did you ask questions to AI/instructor?
The part that gave me the most trouble was differentiating the difference between a DFA and an NFA. Problem 13 displayed this question for me because the first design had only one possible next state for each symbol. I asked AI to clarify the difference if the drawing was a DFA or NFA because I wasn't fully understanding the difference. I learned that a DFA technically qualifies as an NFA under definition.

I focused on smaller problems to build a strong foundation understanding first what each state remembered before trying to keep track of several conditions at once.

I ask AI to help explain to me what each state remembers and how it travels to confirm that my own answers were correct.
# 2. which problem(s) surprised you with a "gold-st-ring"? Which next state(s) did you not account for in the subset of next states? why? How to make sure you avoid such errors in your future flight/traffic/compiler state controller tasks, or in the near future, the course projects/exams?

The problem string that helped me understand branching was 110 for problem 11. This string should accept because its second to last bit is 1 by logic. A branch that guesses at the first 1 reaches q2 after reading 11, but there is still a 0 left. That branch fails because q2 has no outgoing transitions. Another branch guesses at the second 1 and reaches q2 after the final 0, so the whole NFA accepts. The state I need to be especially careful not to lose is q0. After reading a 1 at q0 in problem 11, both q0 and q1 are possible. If I focus only on the arrow to q1, I lose the branch that keeps searching and can make a better guess later. Writing the full set of active states after each symbol helps me keep track of this.

Two other useful practice strings are 111 for problem 13 and 1011011 for problem 15. 111 should accept because "at least two" includes three 1s. 1011011 should reject for problem 15 because it has five 1s. I chose the longer string to practice following more branches. It reaches q0 after reading 101 and again after 101101, but there is input left both times. The final 1 moves the machine out of q0, so stopping early would give the wrong result.

For future assignments and controller or compiler problems, I would start by writing a short meaning for every state. I would list all possible next states after each symbol and check that the entire input has been read before deciding whether it accepts. I would also test the empty string, short strings, and strings just outside the language. If I find a mistake, I would keep that input as a test and rerun the full test set after making a correction.

# 3. Other insights/comments/questions that you want the grader/instructor to know.
Will problems like these be used in the exam, and will we need to make up our own test strings or have some given.