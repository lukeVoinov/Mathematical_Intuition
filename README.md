# Maximizing Water Stored in a Bottle Tilted at an Angle

## Story and Motivation

A few days ago, I was at my school's gym playing the best game of badminton of my life. During a break, I went to the nearest water fountain to fill up my water bottle but encountered an obstacle: the only way I could fill my bottle was by tilting it at an angle. This caused water to spill out before the bottle could be fully filled, leaving a substantial volume filled with air (insert photo of fountain with description: *"Water fountain in gym"*).

In computer science, we are taught to implement efficient algorithms and data structures, write efficient comments, and use AI to improve productivity (in other words, efficiency). Entire studies on artificial intelligence and algorithms are based on the foundational concept of Big O notation. It is the job of colleges to instill a desire for efficiency in computer science students, which might explain why I was annoyed that my bottle wasn’t completely filled. Why make a second trip to the fountain when one would suffice?

This project goes beyond a simple annoyance: I wanted to understand what it looks like when physicists employ critical and creative thinking (albeit at a much more sophisticated level). I also wanted to prove to myself that I am not wasting time in school, that I have learned something meaningful, and that I can apply that knowledge. This project served as a fun logic puzzle and demonstrated the conceptual process of a physicist without being overly complex or detached from personal experience. I discuss my takeaways in the *Conclusions* section.

---

## The Problem

**Given a water bottle, what angle must the bottle be oriented at with respect to the ground such that it will be maximally filled?**

---

## Background + Logic

Imagine we have a water bottle that can store **L** liters of water, where **L** is the maximum the bottle can hold. Ideally, we always want it to be filled with **L** liters. This can only happen if the maximum height of the stream (**s**) is greater than the height of the bottle (**b**). If **s** is less than **b**, water will splash against the side of the bottle and fail to enter. Under these conditions, the water bottle must be tilted at some angle for any water to enter. However, from physical observations, this results in some water spilling out before the bottle is filled to capacity.

Mathematically, the conditions can be represented as follows:

- If **s > b**, the bottle will be filled with **L** liters:  
  **l = L**, where **0 ≤ l ≤ L**.
- If **s > b**, the optimal angle for maximum filling is **90°** (upright).  
  This leads to a key conclusion:  
  **A bottle will always be filled maximally if it is at a 90° angle.**  
  The closer the bottle's angle is to 90°, the more likely it will fill completely without spilling.

What happens when **s = b**?  
If **s = b**, logically, the water bottle can still be filled maximally. Since the stream has a certain width, part of it enters the bottle while the rest spills over. However, if we restrict conditions so that the stream cannot spill over the bottle (a "straight shot" into the bottle), then the results change: 90° may no longer be optimal.

---

## The Incomplete Theory

The situation becomes more complex when **s < b** (the stream is shorter than the bottle). In this case:
- Water begins to spill out before the bottle is filled with **L** liters.
- The maximum water the bottle can hold will be **l**, where **l < L**.

To simplify this scenario, we can transform the **s < b** condition into an equivalent **s = b** frame. Why?  
- The **s = b** frame is simpler and avoids unnecessary complexity in calculations.  
- This transformation is analogous to centering a function (e.g., shifting **y = x²** by subtracting 5 units when the vertex moves 5 units right).

---

### Validation of the Transformation

Consider two bottles, one with height **B** and another with height **b**, and a stream of height **S** where:  
**0 < b < S < B**

- Bottle **B** must tilt to fill with water because **B > S**.  
- Bottle **b** can remain upright and fill maximally because **b < S**.

If we tilt bottle **B** such that water enters at the same rate it spills, the bottle will fill partially. By cutting off the part of the bottle filled with air, we effectively reduce **B** to a new bottle with height equal to the distance from the ground to the water level. This new bottle behaves as if **s = b**. (Insert diagram here.)

---

## Calculations

(*Placeholder for mathematical derivations.*)

---

## Conclusion

### Key Takeaways:
- Patience and the importance of verifying solutions.
- The process of converting a concept or idea into mathematical terms.
- An appreciation for what I enjoy and how to make theoretical ideas applicable.

This project was a practical exercise in logic and creative thinking, reminding me that the principles we learn in class can have real-world applications.
