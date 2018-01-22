Chapter 3
===
### Formal Definition of Turing Machine
A turing machine can be defined as a 7-tuple (Q,Σ,Γ,δ,q0,qaccept,qreject)
1. Q 狀態集合
    - a set of the state
2. Σ 輸入字母表 (不包含特殊的空白符□)
    - input alphabet, not cantaining the blank symbol, U
3. Γ 紙帶字母表 (□∈Γ且Σ⊂Γ)
    - tape alphabet, where U∈Γ and Σ⊂Γ
    - 紙帶字元集要有空，來表示沒寫的部分
    - 輸入的字元集屬於紙帶上的字元集，因為輸入要放到紙帶上
4. δ 轉移函式
    - Q×Γ→Q×Γ×{L,R}，其中L,R表示讀寫頭是向左移還是向右移
    - 會根據當前機器的狀態，和讀寫頭所指的格子中的符號來轉移。
    - 磁針向左/右，磁針移動前指向的符號可做改變。
5. q0∈Q 起始狀態
    - the start state
6. qaccept∈Q 接受狀態
    - the accept state
7. qreject∈Q 拒絕狀態
    - the reject state
    - qreject ≠ qaccept

### Configuration of a Turing machine 圖靈機的組態
For a state q and two strings u and v over the tape alphabet Γ, we write uqv for the conﬁguration, where
- q is current state 當前狀態
- uv is current tape contents 當前磁帶上的字母
- the first symbol of v is current head location 當前狀態右邊的第一個字母

### C1 yields C2 圖靈機的轉移
From configuration C1 to configuration C2
- ua(qi)bv yields u(qj)acv if δ(qi,b)=(qj,c,L)。磁針向左，磁針移動前所指向的符號可改變。
- ua(qi)bv yields uac(qj)v if δ(qi,b)=(qj,c,R)。磁針向右，磁針移動前所指向的符號可改變。

### What is the language of turing machine?
Turing-recongnizable language

### What is a Turing-recongnizable language?
A language which turing machine can recongnize it.

### What are three possible outcomes for a Turing machine that processes an input?
- loop
    - the machine doesn't halt(停機)
- accept
- reject

### What is decider?
The machine will halt for any input.
That is, the machine will only accept or reject for it's input.

### What is a Turing-decidable language?
Call a language Turing-decidable or simply decidable if some Turing machine decides it.
A language which Turing machine recongnizes it and only accepts or rejects it.

### what is Church-Turing Thesis?
Church used a notational system called the λ-calculus to deﬁne algorithms. Turing did it with his “machines.” These two deﬁnitions were shown to be equivalent.
一般定義演算法的方式分成 Church 的 λ 演算和 Turing 的圖靈機，兩者的運算能力是等價的，任一演算法皆可用兩者其一表達。

### What is Hilbert's tenth problem?
D = {P|P is the polynomial with a internal root}
是否有一個演算法可判斷該多項式是否有整數解。

### Show that Hilbert's tenth problem is Turing-recongnizable.
D = {P|P is the polynomial with a internal root}
P = c1x1+c2x2+...+c0
P 的解為 {x1,x2...} 是一個 set，沒有 range 限制，故須用暴力法逐一求解。
所以 D is Turing-recongnizable

### Convert the Hilbert's tenth problem into a language/decision problem.
D = {P|P is the polynomial with a internal root}
D1 = {P|P is the polynomial over x with a internal root}
D and D1 both Turing recognizable language.
因為 D1 有 range 限制，所以逐一帶入必定有解，所以 D1 is Turing-decodable language.
The output of D1 exist between ±k(cmax/c1)

### Corresponding to the above question ,is the decision problem Turing-decidable?
Yes.