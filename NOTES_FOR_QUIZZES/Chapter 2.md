Chapter 2
===
### what is context-free language(CFL)?
The language generated by context-free grammer(CFG).

### Formal definition of CFG
A context-free grammer is 4-tuple (V,Σ,R,S), where 
1. V 狀態集合
    - A finite set of variables
2. Σ 轉化字元集合
    - A finite set of terminals
3. R 移動原則
    - A finite set of rules
4. S 開始狀態
    - start variable

### Define the Chomsky normal form(CNF) of CFL
CNF 符合兩條規則：
1. A → BC
2. A → a

A 只能轉換成兩個變數(variable) B 跟 C，且 B 跟 C 不得為起始變數
A 只能轉換為單一字元(termanal) a，且 a 不得為 ε 除非 A 是起始變數

### Formal definition of a pushdown automaton
A pushdown automaton is a 6-tuple (Q,Σ,Γ,δ,q0,F), where Q, Σ, Γ, and F are all finite sets, and 
- Q 狀態集
    - the set of states
- Σ 輸入字母集
    - the input alphabet
- Γ 堆疊字母集
    - the stack alphabet
- δ 轉移函式
    - δ = Q×Σε×Γε→P(Q×Γε)
    - the transition function
- q0∈Q 開始狀態
    - the start state
- F⊆Q 結束狀態
    - the set of accept states

### pumping lemma for context-free language
If A is a context-free language, then there exist a number p (pumping length).
If s is any string in A of length at least p, then s may divided into five pieces s=uvxyz satisfying the conditions:
1. for each i>=0, uv^i^xy^i^z∈A
2. |vy|>0
3. |vxy|<=p

### Prove that every RE is a CFL
PDA可以辨識CFL; DFA可以辨識RE
而DFA可以視為PDA(忽略PDA的stack)
所以RE也是CFL
(因為RE可以被DFA辨識，而DFA屬於PDA，所以RE也可以被PDA辨識，所以RE是CFL)