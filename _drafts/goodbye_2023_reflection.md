---
layout: post
title: "Reflection: Codeforces Goodbye 2023 Contest"
---

As this is a reflection, this will primarily concern my thoughts during and after the contest. As such, it will by no means be a complete editorial: one is provided [here].

Why my thoughts? Well... a common plight in almost any discourse on the art of problem-solving is that everyone jumps to describe the destination -- much fewer go into detail on the journey to get there. So, I guess my hope is that documenting my own journey through a problem forces a level of self-evaluation (and maybe value to a reader who stumbles upon it).

That being said, this contest was logistically... [kind of a trainwreck]. Don't need to pile on more than what's been said, but you'll see my frustrations peek out here and there.

### Problem A
**Statement**: Given $n, k \leq 5$, and an array of $n$ positive ntegers at most 2023, find a way to add $k$ elements to the end of this array such that the product becomes 2023 (or report that it's impossible).

### Problem B
**Statement**: Given $a, b \leq 10^9$, find an integer $x$ such that $a$ and $b$ are the two largest proper divisors of $x$ (one will always exist).

**Reflection**: Yeah, not too much to say... maybe took me a few minutes longer than I'd like for a problem B.

**Solution**: $\lcm(a, b)$ if $b$ is not divisible by $a$, $\frac{b^2}{a}$ otherwise. I don't think this is the only solution.

### Problem C
**Statement**: You have an array of $n \leq 100,000$ positive integers. In a move, you take out two integers $x$, $y$ and replace them with $2\lfloor\frac{x+y}{2}\rfloor$. Two players alternate doing this until there's only one number left: the first wants to minimize it, the second wants to maximize it. What is the final value if both play optimally?

**Reflection**: Games... why did it have to be games. Well, that replacement expression looks kind of funky: let's reword it: $x + y - [x % 2 != y % 2]$... ah... the only thing that matters is the parity of each number. What a common trope for game problems. After a few more minutes of thinking I kind of fudged a formula. Oof... there's too many edge cases though. I don't know if it will pass. Oh, it passed pretests. Yay... I think.

**Solution**: In other words, the sum of all numbers remains almost invariant... except one is subtracted every time you pick two numbers with opposite parity. So this is clearly what player 2 wants to do, and what player 1 does not want to do (or let player 2 do).

-----
Intermission: By this point: I took one look at problem D and it looked unappealing. [Scoreboarding] is an inevitable component of strategizing in most programmong contests, and a very unique tool that once can use for CF scoreboarding is [rainboy], who always goes for the hardest problems first.

In particular, I saw he got his first AC 19 minutes in -- almost unheard of in a div1 round. So, I took a look at problem H... math. In particular, finite field math -- something I'd been reading up on for use in research.

Counting matrices of fixed rank in a finite field.... ahhhh [counting subspaces]... I'd seen this kind of thing before! Surely it had to be doable. Ah well, too soon.

-----

### Problem D
**Statement**: Given an odd integer $n$ up to 99, come up with a set of $n$ $n$-digit perfect squares that are all anagrams of each other.

**Reflection**: I took one look at this statement and it... had to be constructive. Why's n up to 1000? Oh... I guess you'd have to output n^2 characters. Why's n odd? Hmmm......

**Solution**: 

-----
Intermission 2: That took me a while! Oh well, next problem. Problem E... tree DS (Data Structures). Seems like a safe bet. Problem H.... ahhhh.... I want to. Look at the timer... 1 hour left. Ah cmon, why'd they make this round so short..... not too much room to gamble a hard problem. I'll go safe. If only...
-----

### Problem E
**Statement**: You're given a rooted tree of $n \leq 200,000$ vertices, where each vertex $v$ is given a value $a_v$. Now, define the score of a pair of vertices $u$ and $v$ to be 

**Reflection**: Pretty contrived statement! I guess a lesson you learn after doing enough "tree query" problems: the tree version of the problem is almost never too much harder than the array version of that problem (going between paths in a tree and ranges in an array is usually a matter of just adding another data structure). So... simpler... distinct values over ranges in an array. Harkening back to [this problem], I immediately knew the direction in which to think.

I'll spare the details here

**Solutoin**: 

Didn't look much at problem F or G. But apparently F is [standard] and G is broken. So... yeah.

### Problem H
**Statement**: Given n, k, p: count the number of $n \times n$ matrices over $\mathbb{F}_p$ that have rank $r$ (for all $r$ from 0 through $k$).

**Reflection**: I'm sort of still kicking myself about this... looked at thie p

**Solution**: 