---
layout: post
title: Introduction to Sets
---

กำหนดให้ $M = (\{q_0, q_1\}, \{0, 1\}, \{X, Z_0\}, \delta, q_0, Z_0, \emptyset)$ โดยที่ $\delta$ อธิบายดัวต่อไปนี้

$\delta(q_0, 0, Z_0) = \{(q_0, XZ_0)\}$
$\delta(q_0, 0, X) = \{(q_0, XX)\}$
$\delta(q_0, 1, X) = \{(q_1, \epsilon)\}$
$\delta(q_1, 1, X) = \{(q_1, \epsilon)\}$
$\delta(q_1, \epsilon, X) = \{(q_1, \epsilon)\}$
$\delta(q_1, \epsilon, Z_0) = \{(q_1, \epsilon)\}$

เริ่มต้นเรากำหนดให้ CFG $G = \{V, T, P, S\}$ (โดยที่ S เป็นตัว non-terminal ตัวแรกของ CFG $G$)

ฉะนั้น $V$ จะเป็นเซตดังต่อไปนี้ 

$V = \{S , [q_0, X, q_0], [q_0, X, q_1], [q_1, X, q_0], [q_1, X, q_1], [q_0, Z_0, q_0], [q_0, Z_0, q_1], [q_1, Z_0, q_0], [q_1, Z_0, q_1] \}$

เราจะเริ่มต้นที่ $S$ ซึ่งจะเกิดขึ้นจาก state ตั้งต้นของ PDA คือ $q_0$ โดยที่ ค่าบนสุดของ Stack คือ $Z_0$ $(\{q_0, q_1\}, \{0, 1\}, \{X, Z_0\}, \delta, q_0, Z_0, \emptyset)$

$S \rightarrow [q_0,Z_0, q_0]$
$S \rightarrow [q_0,Z_0, q_1]$

เราไม่รู้ว่าเมื่อ pop $Z_0$ จาก Stack แล้วจะไปหยุดที่ state ไหน เลยจำเป็นต้องใช้ ทั้ง $[q_0, Z_0, q_0]$ และ $[q_0, Z_0, q_1]$ เราจะเริ่มพิจารณาจาก $[q_0,Z_0, q_0]$

จาก $[q_0,Z_0, q_0]$ เราทราบว่า การทำงานของ PDA จะเริ่มที่ $q_0$ โดยที่ ค่าบนสุดของ Stack คือ $Z_0$ และ เมื่อ $Z_0$ ถูก $pop$ ออกจาก Stack PDA จะไปอยู่ที่ $q_0$ ฉะนั้น จาก $\delta$ ของ PDA เราจะหาการทำงานที่เริ่มจาก $q_0$ และมีค่าบนสุดของ Stack คือ $Z_0$ ซึ่งมีแค่ตัวเดี่ยวคือ $\delta(q_0, 0, Z_0) = \{(q_0, XZ_0)\}$

จากการรูปแบบการทำงานของ PDA $\delta(q_0, 0, Z_0) = \{(q_0, XZ_0)\}$ จะถูกใช้ทำงานเมือมีค่าของ input เป็น 0 ณ $q_0$ โดยค่าบนของ Stack คือ $Z_0$ โดยการทำงานจะเปลี่ยนสถานะเป็น $q_0$ พร้อมทั้งเปลี่ยนค่าบนสุดของ Stack เป็น $XZ_0$ แทน ฉะนั้นเราสามารถอธิบายได้เป็นโครงสร้าง $[qZp]$ ดังต่อไปนี้

$[\color{blue}{q_0}, \color{green}{Z_0}, q_0] \rightarrow \color{red}{0} [  \color{orange}{q_0}$

ณ state $\color{blue}{q_0}$ และ ค่าบนสุดของ Stack คือ $\color{green}{Z_0}$ ถ้ามี input เป็น  $\color{red}{0}$ จะมีการเปลี่ยน state เป็น $\color{orange}{q_0}$ เนื่องจากการทำงาน PDA ที่คำนึงถึงอยู่ มีการ push $XZ_0$ เข้าไปใน Stack ฉะนั้น

$[\color{blue}{q_0}, \color{green}{Z_0}, \color{purple}{q_0}] \rightarrow \color{red}{0} [  \color{orange}{q_0}, X, q_x][q_x,Z_0, \color{purple}{q_0}]$

โดยที่ $q_x$ เป็น state ใด ๆ ใน PDA เนื่องจาก เราไม่รู้ว่า หลังจากที่ $X$ ถูก pop ออกจาก Stack แล้ว การทำงานของ PDA อยู่ที่ state ไหน ฉะนั้นเราจะได้ CFG production rules ดังต่อไปนี้

$S \rightarrow [q_0,Z_0, q_0]$
$S \rightarrow [q_0,Z_0, q_1]$
