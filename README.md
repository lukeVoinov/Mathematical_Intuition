<h1 align="center"> Mathematical Intuition </h1>
<h3 align="center">Maximizing Water Stored in a Bottle Tilted at an Angle </h3>


<h2 align="center"> Story and Motivation </h2>

Some time ago I was at my school's gym playing a game of badminton when we decided to stop for a break. I went to the nearest water fountain to fill up my water bottle but encountered a problem: the only way I could fill my bottle was if I tilted it at an angle. This then led to water spilling out before the entire bottle could fill, leaving a substantial volume filled with air:

![IMG_3923](https://github.com/user-attachments/assets/b80ab266-33b5-4354-aad9-8386394fa838)

In computer science we are taught to implement efficient algorithms and data structures; to write efficient comments; to use AI to improve productivity. Entire studies on artificial intelligence and algorithms would be impossible to conduct without the foundational Big O notation. It is the job of colleges to engrain a desire for efficiency in their computer science students, which would explain the reason I set out to quantify how to optimize water storage under such conditions. Why make a second trip to the fountain where one would have sufficed?  

Whatever prompted me to do all this math and writing goes beyond just a simple annoyance: I wanted to do this project to try and understand what it looks like when physicists employ (albeit at a much more sophisticated level) critical and creative thinking. I also wanted to prove to myself that I am not wasting time in school: that I have learned something, in the first place, and that I am able to apply that something. This project is a very nice way to demonstrate (what seems to me) the conceptual process of a physicist without making it too complex or detached from personal experience. This project acted as a fun logic puzzle that demonstrated to me that I am actually able to apply what I have learned. I discuss some takeaways in the Conclusions section.  

---

<h2 align="center"> The Problem </h2>

<h2 align="center"> Given a water bottle, what angle must the bottle be oriented at with respect to the ground such that it will be maximally filled? </h2>

---

<h2 align="center"> Background + Logic </h2>

![image](https://github.com/user-attachments/assets/049c5155-43f6-4788-9462-692b599eab52) 


Imagine we have a water bottle that can store **L** liter of water, where **L** is the maximum the bottle can hold. Ideally, we always want it to be filled **L** liters. This can only happen if the maximum height of the stream is greater than the height of the bottle (only the fountain and bottle are involved (no cups, eg)). If the maximum height of the stream, which I will from now on refer to as the height of the stream, is less than the height of the bottle, it will splash against the side of the bottle and never get in.  

![image](https://github.com/user-attachments/assets/a349503b-9efc-430c-9e74-7a70d4a3b476)

Under these conditions, the watter bottle must be titled at some angle if any water is to enter. However, from physical observations, this will result in some of the water spilling out before the bottle can be filled with **L** liters.  

Mathematically, we can represent how many liters a bottle can be maximally filled with as such:  

- **s > b → l = L**, where **s** is the height of the stream, **b** is the height of the bottle, and **l** is a particular but arbitrary literage of water such that it satisfies the following conditions:  
  **0 ≤ l ≤ L.**  

When **s > b**, then, we can answer the question posed:  
**What angle must a bottle be oriented at with respect to ground such that it will be maximally filled?**  

At a **90-degree angle**!  

This leads to a key conclusion:  
**A bottle will always be filled maximally if it is at a 90-degree angle.**  

Further thought will show an important corollary of this fact:  
**The bottle will be filled maximally if it is the closest to 90 degrees as it can be.**  

If the bottle is upright, water can only spill out once the bottle is completely filled. Thus, if **s > b**, the bottle will stand at a 90-degree angle (the closest to 90 degrees the bottle can be is 90 degrees) to be filled with **L** liters.  

<h2 align="center"> ### Case: What If **s = b**? </h2>

Logically, if **s = b**, then the water bottle will also be maximally filled. The assumption here is that the stream has a certain width, part of it fills the bottle while the other part spills over. If we restrict the conditions to be such that the stream is not allowed to spill over the bottle—a "straight shot" into the bottle—then the results will be different to the extent that if **s = b**, then 90 degrees will no longer be the optimal solution.  

---

<h2 align="center"> Incomplete Theory </h2>

Our theory now covers a large portion of what angle a bottle must be leaned at such that it will be maximally filled with water. We know that if the height of the stream is either above or at the same height as that of the bottle, the bottle will maximally fill if it stands at a 90-degree angle with respect to the ground. If we only ever encounter water in such situations, then our theory is complete, and it would be difficult to even ask such a question in the first place.  

![image](https://github.com/user-attachments/assets/01429f4e-7090-4d23-a860-6ade80430478)

However, when I was filling my water bottle, I encountered the scenario where my bottle was taller than the stream.  

In this scenario, it is more difficult to say exactly what angle a bottle must be leaned at for it to maximally hold water. A few key observations are that no matter how many angles I experiment tilting the bottle at, water will eventually start to flow out of the bottle, making it impossible to ever fill the bottle with **L** liters.  

![image](https://github.com/user-attachments/assets/a20aa190-75d5-405a-ae89-2e7a6c578ad0)

This is where the application value of posing this question arises—it would be ideal if the bottle held all the water it can given certain constraints.  

---

<h2 align="center"> Towards a Partial Explanation </h2> 

The theory is now shown to be incomplete. We do not know how we should orient our water bottle if it is taller than the stream. A move in the right direction would be to provide a partial explanation. Such an explanation will not be able to accurately predict the specific conditions necessary to fill the bottle maximally (hence "partial") but it will impose tighter bounds on the range of possible outcomes and describe general behavior.  

A partial explanation would be the observation that since water will begin to pour out before the bottle fills to **L** (the maximum capacity when standing 90 degrees), the maximum amount of water the bottle will hold will be **l**, where **l < L**.  

This partial explanation then limits what values we should expect to detect under such conditions and describes that the general behavior of the bottle under the condition **s < b** is to have a lower capacity than in the previous conditions.  

---

<h2 align="center"> Transforming the Frame </h2> 

Another useful aspect of this partial theory is that we can now come to an important tool:  

A bottle in conditions **s < b** can be transformed into an **s = b** frame.  

This means that we no longer have to work with the bottle under **s < b** conditions—we can now work with bottles under **s = b** conditions.  

Why would we want to do this?  

Mainly because the **s = b** frame is much simpler. This part of the theory was the most straightforward to solve because it was so simple.  

This is partially where the "elegance" of a proof comes from—the bridge formed when modern ideas harken back to classical (less complex) ideas. We've been transforming to simpler frames ever since elementary school!  

For example, only variables are present in **y = x²**, which is centered at the origin. When the function is centered 5 units to the right of the origin, however, we "pull" it back to the origin by subtracting 5 units (or alternately create an effective new origin at this location; the two are equivalent).  

---

<h2 align="center"> Validation </h2>

Having established the value and uses behind this tool, one may wonder whether the conclusion we came to is even valid. How can we transform from an **s > b** frame to an **s = b** frame?  

Suppose two bottles exist, one of height **B** and the other of height **b**. Also suppose there is a stream of height **S**. Let **0 < b < S < B.**  

Because **B < S**, **B** must be tilted at an angle if it is to fill with any water at all, and because **b < S**, it can stand upright and fill maximally.  

If we will fill the bottle of height **B** with the maximum amount of water it can store when water begins to pour out at the same rate it's entering. Then, if we tilt the bottle to an upright position, it will be filled with a certain amount of air and water. Cutting off the part of the bottle filled with air, the resulting bottle is now an upright bottle filled, relative to itself, with **L** liters.  

This is of the same essence as the Intermediate Value Theorem. It is easy to see that the height of this resulting bottle will be the same as the distance from the ground to the lid of the bottle with height **B**.

![image](https://github.com/user-attachments/assets/fe5cb191-98ae-4e56-99f7-99813ee3579d)


---

<h2 align="center"> Calculations </h2>

The water will be shot as a parabola. To fill maximally, a bottle must be tilted such that the bottle's edge intersects the parabola's maximum. To see why, we can return to the s = b frame. If an upright bottle of the same height as that of a stream is shifted a little bit to the left of the maximu, the water will hit the wall of the bottle and never enter. The same will happen if the bottle is moved slightly to the right of the maximum. Thus, if in the frame s = b the bottle only fills at the heighest point of the stream, which is s, then it makes sense to conclude that the heighest point of the stream will always be the point in the stream the bottle can be maximlly fileld at.

![image](https://github.com/user-attachments/assets/6f277f45-e51d-4a1d-9a20-12a3c20105bb)


We will call the height of the stream, in this case, **y = s**, and the height of the bottle will be **h = s + delta_s**, where **delta_s > 0**. Leaning the bottle such that it interescts the stream, we form a right triangle, where the hypotenuse is **h** and the height is **s**. Then, to find the angle the bottle is tilted at with respect to the ground, we use trigonometry to find:

**sin(theta) = (s/h) **. Solving for theta, **theta = arcsin(s/h) = arcsin( s / (s + delta_s)**.

![image](https://github.com/user-attachments/assets/c4506439-a2b4-443d-9c94-7aa1eb7dbb6e)


<h2 align="center"> Testing the Equation </h2>

Before incorporating the result into our theory, we need to make sure it's correct. A good way to do this is to look at how it works at extremes. What happens when the height of the bottle approaches that of the stream? 

**lim delta_s -> 0 arcsin ( s / (s+ delta_s) ) = arcsin(1) = 90 degrees**. This is exactly what we predicted earlier. Now, what if the bottle is infinitely tall?

**lim delta_s -> infinity arcsin ( s / (s + delta_s) ) = arcsin(0) = 0 degrees**. Imagine a bottle titled at the point where it intersects the maximum height of the stream. Its two restrictions are 1) the ground and 2) the intersection. Then If we elongate the bottle, the ground will now interfere with the intersection point. To return the bottle opening to the intersection point, it must now be shifted down, which will in turn decrease the angle the bottle is titled at. DElongating the bottle to infinity, then, must reult in the bottle being bottle being at a 0 degree angle with respect to the groud; that is, it will be held parallel to the stream at its peak. What if the bottle is less than the height of the stream?

**arcsin ( s / (s - delta_s) )**. This means that the numberator will be larger than the denominator, which in arsin results in **undefined**. This also checks out because this tests when b < s, which is in contradiction to the condition that b > s. Notice that just because we found the solution to the problem under this condtions, it doesn't solve for every condition - it is undefined in the domain where b < s and we must examine that domain seperately. 

![image](https://github.com/user-attachments/assets/3c320ca9-5167-4760-a00a-f97c15e2189d)


---

## Conclusion  

### What did I learn:  
- Patience  
- Verifying solutions  
- What I enjoy  
- How to convert a concept/idea into math  
