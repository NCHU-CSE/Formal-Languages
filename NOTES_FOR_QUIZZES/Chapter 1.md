Chapter 1
===
### Regular language can be recognized by which three computational models with same computation capabilities？
- Deterministic Finite automata（DFA）決定性有限自動機
- Nondeterminism Finite automata（NFA）非確定有限自動機
- Regular Expression（RE）正規表達式

### Please compare DFA and NFA.
- same
    - 兩者計算能力相同
- differences
    - DFA: 每一次transition function會到唯一一個狀態，也就是: δ(Q1, A)-> Q2
    - NFA: 每一個transition function不一定只會指向一個狀態，所以: δ(Q1, A)-> {Q2, Q3, ...}

### Write the theorem that states the relationship between DFA and NFA.
Every DFA is a NFA.

### What is regular language？
The language which can be recognized by some finite antomaton.
可被有限自動機接收的字串

### The Regular Operations 正則算子
= Write the theorems that state the closure properties of the class of regular languages under three regular operations.
- 聯集 Union 
    - A∪B={x | x∈A or x∈B}
- 字串串接 Concatenation
    - A。B={xy | x∈A and y∈B}
- Star
    - A∗={x1x2...xk | k≥0 and xi∈A}
    - A∗=ϕ∪A∪A2∪∪A3...
    - A∗={ε}∪A∪AA∪AAA∪··
    - 字串可以隨意串接0-n次(平方表示自己跟自己串接)

### Formal definition of FA 有限自動機定義
- Q 狀態集
    - a finite set called the states
- Σ 字母集
    - a finite set called the alphabet
- δ 轉移函式
    - Q×Σ→Q, is the transition function
- q0∈Q 開始狀態
    - the start state
- F⊆Q 接受/結束狀態
    - the set of accept states or final states

### Write down the theorem that states the equivalence of computational power between regular expressions and finite automata.
Regular language and finite automata is equialent in their descriptive power.
Regular language is one that is recognized by some finite automata.

### What is regular expression?
Expressions (desbribing language) which used regular operation to build up.

### Formal definition of a regular language.
- a∈Σ
- ε
- Φ
- R1∪R2
- R1。R2
- R1*

### Write the theorem that states the relationship between regular language and regular expression.
A language is regular if and only if some regular expressions describe it.

### What is a formal language over an alphabet Σ?
A formal language over Σ is a subset of Σ*

### What is the famous open problem in comlpexity theory that is worth one million US dollars for the ans?
P=NP?

### What is the pumping lemma for regular language?
If A is regular language, then there exist a number p(pumping length).
If s is any string in A of length at least p, then s may be devided into three pieces, s=xyz.
Satisfying three condiction.
1. for each i>=0, xy<sup>i</sup>z∈A
2. |y|>0
3. |xy|<=p


