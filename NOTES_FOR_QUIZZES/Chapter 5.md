Chapter 5
===
### Define the language HALTTM for the halting problem of TM.
HALTTM = {<M,w> | M is a TM that halts on input w}

### Prove that HALTTM is undicidable.
先假設 HALTTM R 是決定性問題，然後用 R 構造一個圖靈機 S 讓 ATM 也是決定性問題，矛盾！
S = "On input <M,w>:
1. Run TM R on input <M,w>
2. If R reject, reject.
3. If R accept, simulate M on w until it halt.
4. If M has accepted, accept; if M rejected, reject."
因此，如果 R 決定 HALTTM，則 S 決定 ATM；因為 ATM 是不可決定的問題，所以 HALTTM 也是不可決定的問題。

### What does it mean by saying that problem A is reducible to problem B?
The solution to B can be used to solve A.

### If problem A is reducible to problem B, what can we say about the decidability of A and B?
- B是決定性問題 → A是決定性問題
- A是不可決定性問題 → B是不可決定性問題
