Chapter 4
===
### Give a language that is not Turing-recongnizable (Turing-unrecongnizable language).
(ATM)'

### Give a language that is Turing-recongnizable, but not Turing decidable.
ATM = {<T,w> | T is a Turing machine that accepts string w}

### How to solve the computational problem of testing weather a DFA B accepts an input w?
It's same with the problem of testing weather <B,w> is member of the language ADFA.

### Define the acceptance problem for DFA, i.e. ADFA
ADFA = {<D,w> | D is a DFA that accept string w}

### Is ADFA decidable? If yes, present a Turing machine that decides it.
Yes.
ADFA="
On the input <D,w>
1. simulate (模擬) D on string w
2. if D ended on accept state, accept; otherwise, reject."

### Define the acceptance problem of Turing machine, i.e. ATM
ATM = {<T,w> | T is a Turing machine that accepts string w}

### Is ATM Turing-recongnizable? If yes, present a Turing machine that recognizes it.
Yes.
ATM="
On the input <T,w>
1. simulate T on input w
2. if T ever accept v, accept; if T reject, reject."

### What does it mean by saying the set is countable?
A set is countable if the set either is finite state or it has the same size of N (the set of normal numbers).

### Show that the set of real numbers is uncountable.
假設實數集可數，則可以找到 ono-to-one and onto function from N
N | f(N)
=-=-=-=-=-=
1 | 0.1111
2 | 0.2222
3 | 0.3333
4 | 0.4444
現在用一個方法產生實數 x
x 的小數點後的第 i 個數會不同於第 f(i) 的小數點後的第 i 個數
因為 x 與集合中每個實數皆有不同的地方，所以 x 不在實數集合中，矛盾假設。
所以實數是不可數的。
