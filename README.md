<h1 align="center"> Mathematical Intuition </h1>
<h1 align="center">Maximizing Water Stored in a Bottle Tilted at an Angle </h1>


<h2 align="center"> Story and Motivation </h2>

Some time ago I was at my school's gym playing a game of badminton when we decided to stop for a break. I went to the nearest water fountain to fill up my water bottle but encountered a problem: the only way I could fill my bottle was if I tilted it at an angle. This then led to water spilling out before the entire bottle could fill, leaving a substantial volume filled with air:

![IMG_3923](https://github.com/user-attachments/assets/5f2d0a93-6bfe-41d2-8041-3f0277522418)

In computer science we are taught to implement efficient algorithms and data structures; to write efficient comments; to use AI to improve productivity. Entire studies of algorithms would be impossible to conduct without the foundational Big O notation. It is the job of colleges to engrain a desire for efficiency in their computer science students, which would explain the reason I set out to quantify how to optimize water storage under titled conditions. Why make a second trip to the fountain where one would have sufficed?  

Whatever prompted me to do this math and writing goes beyond just a simple annoyance: I wanted to do this project to try and understand what it looks like when physicists employ (albeit at a much more sophisticated level) critical and creative thinking. I also wanted to prove to myself that I am not wasting time in school: that I have learned something, in the first place, and that I am able to apply that something. This project is a very nice way to demonstrate (what seems to me) the conceptual process of a physicist without making it too complex or detached from personal experience. This project acted as a fun logic puzzle that demonstrated to me that I am actually able to apply what I have learned. I discuss some takeaways in the Conclusions section.  

---

<h2 align="center"> The Problem </h2>

<h4 align="center"> Given a water bottle, what angle must the bottle be oriented at with respect to the ground such that it will be maximally filled? </h4>

---


<h2 align="center"> Background + Logic </h2>

Water Bottle               |  Abstraction
:-------------------------:|:-------------------------:
![Inspirational water bottle next to water fountain](https://github.com/user-attachments/assets/43aeba15-0f60-4272-b58b-d999ea3bdf1d)  |  ![Abstraction of a water bottle where the dark blue edge is a further abstraction of the entire bottle](https://github.com/user-attachments/assets/049c5155-43f6-4788-9462-692b599eab52) 


Imagine we have a water bottle that can store **L** liters of water, where **L** is the absolute maximum the bottle can hold. Ideally, we want it to be filled **L** liters. We know from experimental (in essence personal) observation that this happens when the maximum height of the stream is greater than the height of the bottle (only the fountain and bottle are involved - no cups, e.g.). If the maximum height of the stream, which I will from now on refer to as the height of the stream, is less than the height of the bottle, it will splash against the side of the bottle and never get in.  

![image](https://github.com/user-attachments/assets/a349503b-9efc-430c-9e74-7a70d4a3b476) 

Mathematically, we can represent how many liters a bottle can be maximally filled with as such:  

- **s > b → l = L**
  
Let **s** be the height of the stream, **b** the height of the bottle, and **l** a particular but arbitrary literage of water such that it satisfies the following conditions:  **0 ≤ l ≤ L.**  

When **s > b**, then, we can answer the question posed:  

Q: **What angle must a bottle be oriented at with respect to ground such that it will be maximally filled?**  
A: At a **90-degree angle**!  

We can rephrase the answer quantitatively:  
**If the height of the stream is greater than the height of the bottle, a bottle will always be filled maximally if it is at a 90-degree angle.**  

Further consideration will show an important corollary of this fact:  
**The bottle will be filled to its fullest possible capacity the closer it is to standing at a 90 degree angle with respect to the ground.**  

The first statement is a specific instance of the general corollary. This statement makes intuitive sense - the less the bottle is tilted, the less water will spill out, meaning the bottle can hold more. For the s > b case, there's nothing limiting the bottle's orientation, meaning the nearest the bottle can be to 90 degrees is 90 degrees.

From this corollary we can imagine a concept of "tilt" - a way to quantify how much tilting the bottle affects the bottle's capacity. This observation-thought process is similar to how ideas such as "potential" come about - they're useful symbols that we can manipulate to quantify how certain conditions (e.g. distance) affect objects. 

<h2 align="center"> Case: What If s = b? </h2>

We must also examine an edge-case (literally): what if the stream is the same height as the bottle? Logically, if **s = b**, the water bottle will also be maximally filled. The assumption here is that the water stream has a certain width that we have up until now abstracted away. Part of it fills the bottle while the other part spills over. If we restrict the conditions to be such that the stream is not allowed to spill over the bottle—a "straight shot" into the bottle—then the results will be different to the extent that if **s = b**, then 90 degrees will no longer be the optimal solution (thought it'll be near it).  

---

<h2 align="center"> Incomplete Theory </h2>

Our theory now covers a large portion of what angle a bottle must be tilted at such that it will be maximally filled with water. We know that if the height of the stream is either above or at the same height as that of the bottle, the bottle will fill maximally if it stands at a 90-degree angle with respect to the ground. 

If we only ever encounter water in such situations, then our theory is complete, and it would be difficult in the first place to even pose this question. Why inquire of something so obvious? Obviousness blinds us, other than for psychological reasons, because we "don't fix what's isn't broken". If the feature is common enough to be shrouded in obviousness then it must already work pretty well - how much more efficiently can we expolit it? However, many important breakthroughs come not just from exploiting some property, as engineers do, but also from illuminating the obvious.  


<img width="619" alt="image" src="https://github.com/user-attachments/assets/4ca281ff-e1d0-4a65-b06e-037c1c1d6822" />

These's aren't the only two scenarios we encounter: when I was filling my water bottle, I encountered the scenario where my bottle was taller than the stream.  

In this scenario, it is more difficult to say exactly what angle a bottle must be tilted at for it to maximally hold water. A few key observations are that no matter how many angles I experiment tilting the bottle at, water will eventually start to flow out of the bottle, making it impossible to ever fill the bottle with **L** liters, the absoulute capacity.  

![image](https://github.com/user-attachments/assets/a20aa190-75d5-405a-ae89-2e7a6c578ad0)

This is where the application value of posing this question arises—it allows us to find the most time and energy efficient option for filling a bottle. Granted, in reality people can achieve this by tilting the bottle as far back as they possibly can while allowing water to constantly flow over. Then, via simple and harmless brute force they fill the bottle to nearly the maximum. But if we don't want to get the bottle wet or allow water to be wasted, these results are useful.  

---

<h2 align="center"> Towards a Partial Explanation </h2> 

Before examining this new condition, I'll take an aside into understanding the process that allows us to 1) keep ideas in check (e.g., not contradicting), 2) examine further aspects of a phenomenon (e.g., could we suspect that that the bottle has other conditions that we must examine), and 3) ultimately describe and predict the phenomenon's behavior - this process is the "theory". Our theory is shown to be incomplete. We can explain the ideal orientation necessary for filling a bottle maximally under two situatuions. We do not know, though, how we should orient our water bottle if it is taller than the stream. If we cannot yet solve this scenario (see "Calculations" for the solution), a move in the right direction would be to provide a partial explanation. Such an explanation will not be able to accurately predict the specific conditions necessary to fill the bottle maximally (hence "partial") but it will impose tighter bounds on the range of possible explanations and describe general behavior.

A partial explanation would be:

- Since water will begin to pour out before the bottle fills to **L** (the maximum capacity when standing at 90 degrees), the maximum amount of water the bottle will hold will be **l** liters, where **l < L**.  

This partial explanation limits what values we should expect to detect when **s < b** and describes that the general behavior of the bottle under the condition **s < b** is to have a lower capacity than in the previous conditions. The usefulness of limiting possible theoretical explanations can be seen in the following example. Suppose there were cavemen who lived in an environment surrounded by mountains and these cavemen wanted to know why there is wind. One theory could propose that there are giants beyond the mountains whose job is produce wind by blowing. Anothr theory could be the theory we currently hold of wind. For the cavemen, both theories could be equally vaild - they have no way to acquire data to prove one or the other. If, however, the cavement somehow produced a partial explanation that wind is produced inorganically, they would drop the giant-wind theory. Such a theory strays beyond reasonably established bounds that narrow onto the truth. Classification "models" used in artificial intelligence are an excellent visalization of how data affect theories, models.

![image](https://github.com/user-attachments/assets/da07a87d-b1d6-4c0f-b486-e15f7f18ec5d)
"Classification Model Challenges, Under-fitting, Over-fitting." infoDiagram, www.infodiagram.com/slides/classification-model-challenges-under-fitting-over-fitting/. 


---

<h2 align="center"> Transforming the Frame </h2> 

Another useful aspect of this partial theory is that by being able to describe general behaviour, can now come to an important tool:  

A bottle in conditions **s < b** can be transformed into an **s = b** frame.  

This means that we no longer have to work with the bottle under **s < b** conditions—we can now work with bottles under **s = b** conditions.  

Why would we want to do this?  

Mainly because the **s = b** frame is much simpler. This part of the theory was the most straightforward to solve because it was relatively simple.  

This is partially where the "elegance" of a proof comes from—elegance is the bridge formed when modern (more complex) ideas harken back to classical (less complex) ideas. E = mc^2 is elegant because it opens up a door to many new ideas while still relying on the classical idea of energy. 

In fact, we've been transforming to simpler frames ever since elementary school! For example, the equation **y = x²** is centered at the origin. Performing calculations at the origin makes calculations as simple as possible. When the function is centered 5 units to the right of the origin we essentailly "pull" it back to the origin - we subtract 5 units from x (or alternately create an effective new origin at this location; the two are equivalent).  

---

<h2 align="center"> Validation </h2>

Having established the value and uses behind this tool, one may wonder whether the conclusion we came to is even valid. Can we even transform from an **s > b** frame to an **s = b** frame?  

Suppose two bottles exist, one of height **B** and the other of height **b**. Also suppose there is a stream of height **S**. 
Let **0 < b < S < B.**  

Because **B > S**, **B** must be tilted at an angle if it is to fill with any water at all, and because **b < S**, it can stand upright and fill to the absolute maximum.  

The bottle of height **B** will fill to maximum capacity when water begins to pour out at the same rate it's entering. Then, if we tilt the bottle to an upright position, it will be filled with a certain amount of air and water. Cutting off the part of the bottle filled with air, the resulting bottle is now an upright bottle filled, relative to itself, with **L** liters.  

This is of the same essence as the Intermediate Value Theorem. It is easy to see that the height of this resulting bottle will be the same as the distance from the ground to the lid of the bottle with height **B**.

![image](https://github.com/user-attachments/assets/fe5cb191-98ae-4e56-99f7-99813ee3579d)


---

<h2 align="center"> Calculations </h2>

Now I return to answering the question posed. 

The water will be shot as a parabola. To fill maximally, a bottle must be tilted such that the bottle's edge intersects the parabola's maximum. To see why, return to the corollary: the more upright a bottle is, the more water it can store. If the bottle is filled from a point any lower than the highest point in the parabloa, it is forcing itself to tilt more than needed, thus automatically being excluded from being maximally filled.

![image](https://github.com/user-attachments/assets/6f277f45-e51d-4a1d-9a20-12a3c20105bb)


We will call the height of the stream, in this case, **y = s**, and the height of the bottle will be **h = s + delta_s**, where **delta_s > 0**. Tilting the bottle such that it interescts the stream, we form a right triangle, where the hypotenuse is **h** and the height is **s**. Then we use trigonometry to find the angle the bottle is tilted at with respect to the ground:

**sin(theta) = (s/h) **. Solving for theta, **theta = arcsin(s/h) = arcsin( s / (s + delta_s)**.

![image](https://github.com/user-attachments/assets/c4506439-a2b4-443d-9c94-7aa1eb7dbb6e)


<h2 align="center"> Testing the Equation </h2>

Before incorporating the result into our theory, we need to make sure it's correct. A good way to do this is to look at how it works at extremes. What happens when the height of the bottle approaches that of the stream? 

**lim delta_s -> 0 arcsin ( s / (s+ delta_s) ) = arcsin(1) = 90 degrees**. This is exactly what we predicted earlier. Now, what if the bottle is infinitely tall?

**lim delta_s -> infinity arcsin ( s / (s + delta_s) ) = arcsin(0) = 0 degrees**. Imagine a bottle titled at the point where it intersects the maximum height of the stream. Its two restrictions are 1) the ground and 2) the intersection. Then If we elongate the bottle, the ground will now interfere with the intersection point. To return the bottle opening to the intersection point, it must now be shifted down, which will in turn decrease the angle the bottle is titled at. DElongating the bottle to infinity, then, must reult in the bottle being bottle being at a 0 degree angle with respect to the groud; that is, it will be held parallel to the stream at its peak. What if the bottle is less than the height of the stream?

**arcsin ( s / (s - delta_s) )**. This means that the numerator will be larger than the denominator, which in arsin results in **undefined**. This also checks out because this tests when b < s, which is in contradiction to the condition that b > s. Notice that just because we found the solution to the problem under this condtions, it doesn't solve for every condition - it is undefined in the domain where b < s and we must examine that domain seperately. 

![image](https://github.com/user-attachments/assets/3c320ca9-5167-4760-a00a-f97c15e2189d)


---

## Conclusion  

### What did I learn:  
- Patience  
- Verifying solutions  
- What I enjoy  
- How to convert a concept/idea into math  
