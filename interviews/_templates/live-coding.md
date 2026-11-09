# Live coding — method

## Five steps, out loud

1. **Understand** (2–3 min max): rephrase, ask about input sizes and edge cases, make one own example and one edge case that breaks a wrong reading.
2. **Naive**: write the literal brute force (plain nested loops if that's what it is), fast. Say its cost. Aim for a running version well before half of the time.
3. **Check**: trace one example by hand, run the edge cases.
4. **Improve**: the sentence that leads to the better idea (what is recomputed? what can be remembered?). Before trusting a greedy idea, look for a counter-example.
5. **Cost**: time and space, saying what they depend on (n, m, k separately).

## Before starting

- Ask the time limit. Keep a clock in sight.
- Use the names from the given signature.

## Practice format

- 20–30 minutes alone (40 max), no hints.
- Then a video solution.
- Then Claude writes the correction: naive version, the sentence to the better one, code, trace, cost, the reusable skeleton.

## My recurring errors

| Error | Fix |
| --- | --- |
