# main
Maximizing Water Stored in a Bottle Tilted at an Angle

# Story and Motivation

A few days ago I was at my school's gym playing the best game of badminton in my life when we decided to stop for a break. I went to the nearest water fountain to fill up y water bottle but encountered an obstacle: the only way I could fill my bottle was if I tilted it at an angle. This then led to water spilling out before the entire bottle could fill, leaving a substantial volume filled with air (insert photo of fountain, description "water fountain in gym"). In computer science we are taught to implement efficient algorithms and data structures; to write efficient comments; to use AI to improve productivity (another words for efficiency). Entire studies on artificial intelligence and algorithms would be impossible to conduct without the foundational Big O notation. It is the job of colleges to engrain a desire for efficiency in their computer science students, which would explain the reason I was annoyed that my bottle was not completely filled. Or maybe I'm just lazy and do not want to have to make a second trip to the fountain where one would have sufficed. Whatever prompted me to do all this math and writing goes beyond just a simple annoyance: I wanted to do this project to try and understand what it looks like when physicists employ (albeit at a much more sophisticated level) critical and creative thinking. I also wanted to prove to myself that I am not wasting time in school: that I have learned something, in the first place, and that I am able to apply that something. This project is a very nice way to demonstrate the conceptual process of a physicist without making it too complex or detatched from personal experience. Therefore this project acted as a fun logic puzzle that demonstrated to me that I am actually able to apply what I have learned. I discuss some things I learned in the Conclusions section.

# The problem

Given a watter bottle, what angle must the bottle be oriented at with respect to the ground such that it will be maximally filled?

# Background + Logic

  Imagine we have a water bottle that can store L liter of water, where L is the maximum the bottle can hold. Ideally, we always want it to be filled L liters. This can only happen if the maximum height of the stream is greater than the height of the bottle (only the fountain and bottle are involved (no cups, eg)). If the maximum height of the stream, which I will from now on refer to as the height of the stream, is less than the height of the bottle, it will splash against the side of the bottle and never get in. Under these conditions, the watter bottle must be titled at some angle if any water is to enter. However, from physical observations, this will result in some of the water spilling out before the bottle can be filled with L liters. 
  Mathematically, we can represent how many liters a bottle can be maximally fileld with as such: s > b -> l = L, where s is the height of the stream, b is the height of the bottle, and l is a particular but arbitrary literage of water such that it satisfies the following conditions: 0 <= l <= L. When s > b, then, we can answer the question posed: What angle must a bottle be oriented at with respect to ground such that it will be maximally filled? At a 90 degree angle! This leads to a key conculsion that a bottle will always be filled maximally if it is at a 90 degree angle. Further thought will show an important corollary of this fact: the bottle will be filled maximally if it the closest to 90 degrees as it can be. Given the condition s > b, nothing limits this theorem, resulting in the closest the bottle can be to 90 degrees is 90 degrees.
  Will anything change under a new circumstance? What if s = b? Logically, if s = b then the watter bottle will also be maximally filled. This reveals to us that some of our definitions have been assumed up till now and only now will problems arise if we don;t quickly agree upon them!


# From one perspective the bottle "wants" to be filled maximally because that's what we're looking for. The bottle's tendency towards "uprightness" will always be unexplained until we acknowledge that given s > b, it will always be upright, but given b < s, it will, when looking for a maximum, always lean towards being upright.

A quick proof of the fact that a bottle at an angle is effectively the same as a bottle of height_spillover is as follows:


# Conclusion

What did I learn: patience, verifying soultions, what I enjoy, how to convert a concept/idea into math
