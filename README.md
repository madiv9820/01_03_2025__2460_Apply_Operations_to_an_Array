# [2460. Array-mazing Operations: Let’s Have Some Fun! 🎉🔢😜](https://leetcode.com/problems/apply-operations-to-an-array)

**Difficulty:** Easy 😌 <br>
**Topics Covered:** Array 📊, Two Pointers 👉👈, Simulation 🎮
<hr>

### Problem Explanation 🧐

Alright, hold onto your calculators because it’s time for some *array surgery*—let’s get this algorithm party started! 🎉

You're given a **$0$-indexed array of non-negative integers** (no drama here 😎), and we need to apply **$n-1$** **operations** on it. Let’s break it down:

- #### The Operation Rules ✨:
    On the **$i^{\text{th}}$ operation** (starting at $0$, because math doesn’t care about your feelings 🙄):
    - You take a look at the element at **index $i$**.
    - If **$nums[i] = nums[i+1]$** (oh look, they’re matching! 👯‍♀️), then:
        - You **double** the value of **$nums[i]$** (because why not? If they’re the same, make it BIGGER 💥).
        - You **set $nums[i+1]$ to $0$** (poof! Like magic 🎩✨).
    - If **$nums[i] \neq nums[i + 1]$** (no match, no magic ✋), you just skip the operation. Move along, nothing to see here! 😅

- #### The Grand Finale 🎆:
    After all the operations are done, we perform a little **zero cleanup**:
    - **Shift all the zeros to the end** of the array (because they’ve been **hanging out** in the middle way too long, and it’s time to send them to the back of the bus 🚍). 

- #### Example Time 🔍: 
    Let’s say you start with this party of numbers: $[1,0,2,0,0,1]$
    - After performing your operations (poof!✨), you end up with: $[1,2,1,0,0,0]$
    What happened? 🤔
    - **$1$ and $0$ didn’t match**? So, nothing fancy there.
    - But those **two zeros**? They got *shuffled to the back*, like they’re the *awkward guests* who don't know where to stand at the party. 🎉 

- #### Your Mission 🦸‍♀️:
    After all the *superhero operations*, you return the **new array**. Ready to perform some magic? Let’s gooooo! 💥🔄 <br>
    (Oh, and make sure you don’t get distracted by shiny objects in the array while doing this. 👀)

### Examples 🧮
- **Example 1:**
    - **Input:** $nums = [1,2,2,1,1,0]$
    - **Output:** $[1,4,2,0,0,0]$
    - **Explanation:**
        - **$i = 0$**: **$nums[0]$** and **$nums[1]$** are not twinsies $(1 \neq 2)$, so... nothing happens. We just chill and move on. 😎 <br>
        **Array so far:** **$[1,2,2,1,1,0]$**
        - **$i = 1$**: **$nums[1]$** and **$nums[2]$** are like, "Hey, we're twins!" ${2=2}$, so we make **$nums[1]$** double its value (because twins deserve a boost 💪), and we turn **$nums[2]$** into a zero (they’re out of the game, sorry!). <br>
        **Array now:** **$[1, 4, 0, 1, 1, 0]$**
        - **$i = 2$**: **$nums[2]$** and **$nums[3]$** don’t match **$0 \neq 1$**, so we skip this round. Maybe next time, 0. 🙅‍♂️ <br>
        **Array still:** **$[1, 4, 0, 1, 1, 0]$**
        - **$i = 3$**: **$nums[3]$** and **$nums[4]$** are matching **$1=1$**! We double **$nums[3]$** (because one’s company, but two’s a party 🎉), and make **$nums[4]$** a zero. <br>
        **Array now:** **$[1, 4, 0, 2, 0, 0]$**
        - **$i = 4$**: **$nums[4]$** and **$nums[5]$** match **$0 = 0$**. We double **$nums[4]$** (**$0 \times 2$** is still **$0$**, but let’s pretend that didn’t happen 🤔), and set **$nums[5]$** to zero. <br>
        **Array stays the same:** **$[1, 4, 0, 2, 0, 0]$**

- **Example 2:** 
    - **Input:** $nums = [0,1]$
    - **Output:** $[1,0]$ 
    - **Explanation:** No operation can be applied, we just shift the 0 to the end.

### Constraints 🛑
- **$2 \leq nums.length \leq 2000$**:-  The array is not too big, not too small... just like Goldilocks' porridge 🥣
- **$0 \leq nums[i] \leq 1000$**:- Every number is in a chill range, nothing too wild—unless you're counting zeros, those can be a bit extra 😜

### Hints 💡
- Iterate over the array and simulate the described process. Basically, you're going to walk through the array like you're on a mission. Each step, you check the numbers and perform the necessary action.