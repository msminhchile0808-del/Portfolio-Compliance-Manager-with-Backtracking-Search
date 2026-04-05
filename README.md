# Portfolio-Compliance-Manager-with-Backtracking-Search

Robert Morris University - Intro to AI - Homework 3

### Problem Description

Assuming we are an investment firm that needs to assign a rating to a set of stocks for a new fund.

#### Variables (X): 
        A set of stocks - Apple Inc. (AAPL), Microsoft (MSFT), Xylem (XYL), Intel (INTC), Exxon Mobil (XOM), Chevron (CVX), ConocoPhillips (COP).

#### Domains (D): 
        The allowable ratings for each stock: {Buy, Hold, Sell}.

#### Constraints (C):
        1. Sector Risk: No more than two "Buy" ratings in the Tech sector.
        2. Competitor Conflict.  
        3. ESG Mandate: At least one "Buy" must be a designated high-ESG (Environmental, Social, and Governance) stock.

### Why I chose this algorithm:

  I used Backtracking Search because this problem is a Constraint Satisfaction Problem (CSP). In investment analysis, finding a "path" of moves (like in A*) is often less important than finding a compliant state. Institutional funds must follow a web of complex rules (sector limits, ESG mandates, and diversification requirements). CSPs are specifically designed to solve these types of logical puzzles by treating the state as a set of variables.

### Advantages over other algorithms:

  Backtracking uses pruning. If a partial assignment fails a constraint early, it eliminates thousands of impossible outcomes instantly. On the other hand, Breadth-First Search would look at all possible combinations. Minimax is for two-player adversarial games. The rules are fixed and do not "play back." A CSP is a suitable mathematical tool for a statical environment.

### Limitations:

Complexity: As the number of stocks grows, simple backtracking can become slow. To solve this for the entire S&P 500, I would need to implement the Minimum Remaining Values (MRV) heuristic or Arc Consistency (AC-3).

Hard vs. Soft Constraints: This algorithm treats all rules as "Hard" (must be met). In reality, some investment rules are "Soft" (preferences). To handle those, I would need to use Local Search (Chapter 4) or Linear Programming.
