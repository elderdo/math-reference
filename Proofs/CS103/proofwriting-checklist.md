# Proofwriting Checklist

---

Mathematical proofs have their own writing conventions. Over the quarter, you will internalize those conventions and learn to write like a theoretician.

The conventions used in mathematical proofs can generally be broken down into two areas. The first are rules on structure and writing style, which give rise to the charactistic language used in proofs. The second are rules that may initially appear stylistic, but which hit at deeper aspects of mathematical reasoning. Learning to write naturally while adhering to these rules thus ensures your writing will conform with mathematical writing expectations and, in many cases, automatically eliminate entire classes of mathematical errors.

We have distilled many aspects of mathematical proofwriting into eight specific items that we will look for when reading (and grading) your proofs. They are as follows:

- **_Clearly articulate your assumptions and “want-to-shows.”_**
- **_Make each sentence “load-bearing.”_**
- **_Scope and properly introduce variables._**
- **_Make specific claims about specific variables._**
- **_Don’t repeat definitions; use them instead._**
- **_Write in complete sentences and paragraphs._**
- **_Avoid quantifiers and propositional connectives._**
- **_Avoid the “contradiction sandwich.”_**

**_We will apply this checklist to the proofs that you submit._** We recommend you work through this checklist on every proof that you write. Doing so will help you improve your proofwriting and smoke out some underlying logic errors.

The remainder of this guide goes into more detail about what each of these rules mean.

## Clearly Articulate Your Assumptions and “Want-to-Shows.”

A proof lays out an argument explaining why some conclusion must be true given a set of starting assumptions. Therefore, most proofs will have the following general structure:

1. Introduce a set of starting assumptions, often introducing some variables in the process.
2. Articulate the overall goal of the proof.
3. Give some line of reasoning that reaches the goal.
4. State you've reached the goal and end the proof.

We refer to part (1) of the proof as the **_assumptions_** and part (2) of the proof as the **_"want-to-show"_**. When you are first learning to write proofs, it is important to explicitly include both of these steps in your proof, with exceptions noted below.

### Direct Proofs

In a direct proof, the proof should begin with the assumptions, want-to-show, and conclusion. For example:

**_Theorem:_** If m is odd and n is even, then mn is even.

**_Proof:_** Pick any odd integer m and even integer n.We will show that mn is even.

_(… logic goes here …)_

This means that mn is even, as required.◼

Here, our assumptions are that the reader has chosen an odd integer m and an even integer n, and our want-to-show is that mn is even. Note that the proof does not explicitly use the terms "assume" or "want-to-show," but still achieves the same result. The proof must end with the statement that mn is even, since that is what we explicitly stated we would prove in our want-to-show.

### Proof by Contrapositive

A proof by contrapositive will also include an assumption and want-to-show, which will follow the statement of the contrapositive of the implication. Here is an example:

**_Theorem:_** For all integers m and n, if mn is even, then m is even or n is even.

**_Proof:_** We will prove the contrapositive, namely, that if m is odd and n is odd, then mn is odd. So choose any odd integers m and n.We need to prove that mn is odd. \[…\]

_(… logic goes here …)_

This means that mn is odd, as required.◼

Note that the proof still ends by saying that we have proved what we set out to prove in our want-to-show.

### Proof by Contradiction

A proof by contradiction is different from the other proofwriting styles in that it always includes an assumption, but never includes a want-to-show. It is implicit in a proof by contradiction that the want-to-show is "a contradiction," so it's left out of the proof. Proofs by contradiction are also unusual in that the conclusion of the proof explains what the contradiction shows, which is often the theorem itself.

For example:

**_Theorem:_** For all integers m,n, and p, if mnp is odd, then at least one of m+n,n+p, and m+p is odd.

**_Proof:_** Assume for the sake of contradiction that there are integers m,n, and p where mnp is odd but m+n,n+p, and m+p are even. \[…\]

_(… logic goes here …)_

We have reached a contradiction, so our assumption must have been wrong. Thus for all integers m,n, and p, if mnp is odd, then at least one of m+n,n+p, and m+p is odd.

### Existential Statements

Sometimes, the statement you want to prove is a simple existentially-quantified statement with no universally-quantified parts. For example, you might want to prove that 56 is the sum of four cubes, or that 137 is the sum of two squares. In those cases, you will typically not have anything to assume, and your want-to-show will just be the statement of the theorem itself. In those cases, it's customary to not include an assume or want-to-show statement, since the "assume" bit would have nothing in it and the "Want to show" would be redundant.

### Exercises

These exercises are purely optional but will help reinforce the concepts covered in this point.

1. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For all integers m and n, if m is even and n is even, then m+n is even.

**_Proof:_** Since m is even and n is even, we know there are integers r and s where m=2r and n=2s. This means that m+n=2r+2s=2(r+s). Therefore, there is an integer t (namely, r+s) such that m+n=2t, so m+n is even. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-1)

This proof does not adhere to our style conventions. Specifically, it does not include an assume statement, nor does it include a want-to-show. Here is a better version of the proof:

**_Theorem:_** For all integers m and n, if m is even and n is even, then m+n is even.

**_Proof:_** Let m and n be arbitrary even integers. We will show that m+n is even.

Since m is even and n is even, we know there are integers r and s where m=2r and n=2s. This means that m+n=2r+2s=2(r+s). Therefore, there is an integer t (namely, r+s) such that m+n=2t, so m+n is even, as required. ◼

Note that we explicitly introduce m and n here, state that we are going to prove that m+n is even, and conclude once we have arrived at the statement that m+n is even.

---

2. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For all integers n, if n is even, then there exist even integers r and s where r+s=n2.

**_Proof:_** Let n be an even integer. Since n is even, as proved in lecture we know that n2 is even. Now let r=n2 and s=0. We know that r is even because n2 is even. We see that s is even because s=0=2⋅0. Moreover, r+s=n2+0=n2, as required. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-2)

This proof does not adhere to our style conventions. It does include an assume statement, but it does not have a want-to-show. Here is a better way to write this proof:

**_Theorem:_** For all integers n, if n is even, then there exist even integers r and s where r+s=n2.

**_Proof:_** Let n be an even integer. We need to show that there are even integers r and s where r+s=n2.

Since n is even, as proved in lecture we know that n2 is even. Now let r=n2 and s=0. We know that r is even because n2 is even. We see that s is even because s=0=2⋅0. Moreover, r+s=n2+0=n2, as required. ◼

---

3. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does. (For reference: an integer n is a multiple of three if there is an integer k where n=3k.)

**_Theorem:_** For all integers n, if n is a multiple of three, then n2 is a multiple of three.

**_Proof:_** Choose any n that is a multiple of three. We need to show that n2 is a multiple of three.

Since n is a multiple of three, we know there is an integer k where n=3k. We then see that

n2=(3k)2=9k2=3(3k2),

so there is an integer m, namely 3k2, such that n2=3m. This means that n2 is a multiple of three. Therefore, for all integers n, if n is a multiple of three, then so is n2.◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-3)

This proof does not adhere to our style conventions. It does include an assume statement and has an accompanying want-to-show. However, the proof does not conclude as soon as it has proved the want-to-show. Specifically, the want-to-show is that n2 is a multiple of three, so as soon as we reach that point, we should stop. This proof, on the other hand, continues onward to explain why this means that the full theorem is true, which is unnecessary. One of the main reasons for having a want-to-show is to have a well-defined endpoint for the proof, after which the reader knows that you have done everything you set out to do.

Here is a better way to write this proof:

**_Theorem:_** For all integers n, if n is a multiple of three, then n2 is a multiple of three.

**_Proof:_** Choose any n that is a multiple of three. We need to show that n2 is a multiple of three.

Since n is a multiple of three, we know there is an integer k where n=3k. We then see that

n2=(3k)2=9k2=3(3k2),

so there is an integer m, namely 3k2, such that n2=3m. This means that n2 is a multiple of three, as required. ◼

Notice that this proof is shorter than the previous one.

---

4. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For all integers m and n, if m+n is odd, then so is m−n.

**_Proof:_** We will prove the contrapositive, namely, that if m−n is even, then m+n is even as well.

Since m−n is even, there is an integer k where m−n=2k. This means that

m+n=m−n+2n=2k+2n=2(k+n),

so there is an integer s (namely, m+n) such that m+n=2s, so m+n is even. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-4)

This proof does not adhere to our style conventions. It begins (correctly) by stating the contrapositive of the implication, but then does not take that a step further by explicitly listing the assume and want-to-show steps for the proof. Here is a better way to write this:

**_Theorem:_** For all integers m and n, if m+n is odd, then so is m−n.

**_Proof:_** We will prove the contrapositive, namely, that if m−n is even, then m+n is even as well. So pick some integers m and n where m−n is even; we will show that m+n is even.

Since m−n is even, there is an integer k where m−n=2k. This means that

m+n=m−n+2n=2k+2n=2(k+n),

so there is an integer s (namely, m+n) such that m+n=2s, so m+n is even. ◼

Although this is written as a proof by contrapositive, there is no deep reason it needs to be. This could easily be structured as a direct proof if we wanted to. However, it's not wrong to prove this by contrapositive.

---

5. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For all integers m and n, if mn+1 is even, then m is odd or n is odd.

**_Proof:_** Assume for the sake of contradiction that there are integers m and n where mn+1 is even but m is even and n is even. We will show that this results in a contradiction.

Since m and n are even, there are integers r and s where m=2r and n=2s. This means that

mn+1=(2r)(2s)+1=2(2rs)+1,

which means there's an integer t (namely, 2rs) where mn+1=2t+1. Thus mn+1 is odd, which is impossible because we know that mn+1 is even.

We've reached a contradiction, so our assumption was wrong and if mn+1 is even, then m is odd or n is odd. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-5)

This proof does not adhere to our style conventions. It includes both an assume and want-to-show statement, which is normally correct, but in the context of a proof by contradiction we don't include the want-to-show. Here's a better way to write the proof:

**_Theorem:_** For all integers m and n, if mn+1 is even, then m is odd or n is odd.

**_Proof:_** Assume for the sake of contradiction that there are integers m and n where mn+1 is even but m is even and n is even.

Since m and n are even, there are integers r and s where m=2r and n=2s. This means that

mn+1=(2r)(2s)+1=2(2rs)+1,

which means there's an integer t (namely, 2rs) where mn+1=2t+1. Thus mn+1 is odd, which is impossible because we know that mn+1 is even.

We've reached a contradiction, so our assumption was wrong and if mn+1 is even, then m is odd or n is odd. ◼

Although this is written as a proof by contrapositive, there is no deep reason it needs to be. This could easily be structured as a direct proof if we wanted to. However, it's not wrong to prove this by contrapositive.

---

6. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** There is a natural number n where n2+56=60.

**_Proof:_** Pick n=2. We then see that n2+56=22+56=60, as required. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-6)

Yes, this adheres to our standards. Although there is no assume or want-to-show statement, that is correct because this is a purely existentially-quantified statement. We don't need to assume anything, and since the goal is to prove a number n exists with some properties, we can just give a choice of n that works.

---

## Make Each Sentence Load-Bearing

When you’re writing a proof, you are trying to convey a mathematical argument, and each step in what you write should advance your argument. As a general rule, every statement in a proof should do one of the following things:

- **_Set up a goal._** As mentioned in the preceding pages, your proof should start off with an introduction that clearly articulates a start and end point. In larger proofs, you might find yourself needing to prove an auxiliary result that you’ll use to build up to the larger result, and when you do that, you’ll similarly want to set up what it is that you’re trying to prove.

- **_Introduce a new variable._** Sometimes, in the course of a proof, you’ll need to introduce new variables. If you’re proving something universally-quantified, you might want to say something like “let x be an arbitrary bananafish,” and if you’re proving something existentially-quantified you might want to say something like “since n is even, we know there is an integer k such that n=2k.”

- **_Combine preceding results into something new._** Any sentence that doesn’t set up a new goal or introduce a new variable should make progress toward the result by taking some number of preceding statements and deriving some new, mathematically rigorous result from those preceding statements. For example, you might say something like “since n=2k, we see that n2=2(2k)2” or “since A⊆B and x∈A, we learn that x∈B.”

If you find yourself reading over a sentence that doesn’t accomplish any of these goals, it is likely unnecessary and should be eliminated. This is a great way to reduce the size of your proofs and to make sure that you’re being rigorous. Similarly, if you find yourself doing any of these three things in a way that does not make an appearance later in the proof, it likely means it is unnecessary and that you should remove it. This will make your proof easier to read.

This is a particularly useful check to apply to a proof after you’ve first finished a first draft. Often, in the course of solving a problem and writing up a first proof draft, you’ll go in a direction that ultimately ends up not being necessary, or write out some high-level lines of reasoning that you then make more rigorous later on.

### Exercises

1. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** There are no natural numbers m and n where m2n=1137 and m is odd.

**_Proof:_** Suppose for the sake of contradiction that m and n are natural numbers where m2n=1137 and where m is odd. The fraction m2n does not necessarily have to be in simplest form. We do know that 1137 is in simplest form, though. Cross-multiplying the previous equality gives us that 137m=2n.

- _Case 1:_ n=0. Then 2n=20=1, which is odd. Since 2n=137m, we see that 1=137m, which we rearrange to m=1137. This is impossible because m is a natural number and 1137 is not.

- _Case 2:_ n≥1. Then we can write n=r+1 for some natural number r, and we see that 2n=2r+1=2⋅2r. This means that 2n is even. It would not be even if n=0, though. However, 2n=137m and 137m is odd, since m is odd and 137=2⋅68+1 is odd. This means that 2n is both odd and even, which is impossible.

In either case, we reach a contradiction, so our assumption was wrong. Thus there are no natural numbers m and n where m2n=1137. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-7)

This proof does not adhere to our style conventions. There are several statements in this proof that are true but not used anywhere:

- "The fraction m2n does not necessarily have to be in simplest form." True, but not referenced anywhere in the proof.
- "We do know that 1137 is in simplest form, though." True, but not referenced anywhere in the proof.
- "Then 2n=20=1, which is odd." We do use the fact that 2n=20=1 in the next sentence, but the fact that 1 is odd is not needed anywhere.

There is one other sentence that is not needed, but for a different reason:

- "It would not be even if n=0, though." This statement is true, but it's unnecessary. Because we are in Case 2, where we assume n≥1, we already know that n≠0, and so statements about what would happen if n=0 aren't needed here. If it needs to be brought up at all, it can be brought up in Case 1 where n=0. Second, the fact that a statement would not be true in some other circumstance is not relevant to the argument.

After removing those statements, we're left with this slimmer, easier-to-read proof:

**_Theorem:_** There are no natural numbers m and n where m2n=1137 and m is odd.

**_Proof:_** Suppose for the sake of contradiction that m and n are natural numbers where m2n=1137 and where m is odd. Cross-multiplying the previous equality gives us that 137m=2n.

- _Case 1:_ n=0. Then we see that 2n=20=1. Since 2n=137m, we see that 1=137m, which we rearrange to m=1137. This is impossible because m is a natural number and 1137 is not.

- _Case 2:_ n≥1. Then we can write n=r+1 for some natural number r, and we see that 2n=2r+1=2⋅2r. This means that 2n is even. However, 2n=137m and 137m is odd, since m is odd and 137=2⋅68+1 is odd. This means that 2n is both odd and even, which is impossible.

In either case, we reach a contradiction, so our assumption was wrong. Thus there are no natural numbers m and n where m2n=1137. ◼

---

2. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For all integers m and n, if m is even and n is even, then m2+n2 is even.

**_Proof:_** Choose any even integers m and n. We need to show that m2+n2 is even.

Since m and n are even, we know there are integers r and s where m=2r and n=2s. Similarly, since m and n are even, as proved in lecture, we know that m2 and n2 are even. This means that there are integers j and k where m2=2j and n2=2k. We then see that m2+n2=2j+2k=2(j+k), so letting t=j+k we see that m2+n2=2t. This means that m2+n2 is even, as required. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-8)

This proof does not adhere to our style conventions. Although it's true that m and n are even and thus can be written as m=2r and n=2s for integers r and s, we never make use of this fact later in the proof. Those statements should be removed from the proof, reducing in a slimmer proof that includes only relevant details. Here's what this looks like:

**_Theorem:_** For all integers m and n, if m is even and n is even, then m2+n2 is even.

**_Proof:_** Choose any even integers m and n. We need to show that m2+n2 is even.

Since m and n are even, as proved in lecture, we know that m2 and n2 are even. This means that there are integers j and k where m2=2j and n2=2k. We then see that m2+n2=2j+2k=2(j+k), so letting t=j+k we see that m2+n2=2t. This means that m2+n2 is even, as required. ◼

---

## Scope and Properly Introduce Variables

In programming languages like C, C++, and Java, you’re required to declare variables before you use them. The type of the variable lets the compiler know what sorts of values the variable can hold. If you try to use a variable you haven’t declared, or if you try to treat a variable of one type as though it had a different type, you get a compiler error.

Variables in mathematical proofs obey similar conventions. When writing proofs, it’s important that you clearly articulate what each variable stands for and, additionally, where it comes from. When you use a variable in a proof, you should explicitly articulate

- the name of the variable,
- what value it represents, and
- where it comes from.

Those last two points are critical in writing proofs. Every variable that you use should be of one of the following types:

- **_A universally-instantiated value._** A variable like this has a value that the reader of the proof chooses, but which you as the proof writer don't get to control. Variables like these often arise in the context of proving universally-quantified statements. For example, if you want to prove the claim “for any natural number n, if n is even, then n2 is even,” you might introduce a variable n like this:

> Pick an even natural number n.
>
> Let n be an arbitrary even natural number.
>
> Consider an even natural number n.
>
> Let n be an even natural number.

Here, we’re indicating that the variable is named n, its value is some even natural number, and that the reader, not the writer, picks the value. This is called a **_universally-instantiated variable_** because in principle it could have any value.

- **_An existentially instantiated value._** Sometimes, you and the reader each know that some quantity exists, but you don't know its exact value. For example, if you know that n is an even natural number, you know that n must be twice some other natural number, and so you might give it a name, as shown here:

> Since n is even, there is some integer k such that n=2k.

It’s important to note that this number k is **_not_** chosen arbitrarily. That would imply that _any_ choice of k would work here, but that’s not true: there’s only one choice of k you can pick where n=2k. Rather, k is called an **_existentially instantiated variable_**, because we know that there exists some value with some property and we’re introducing the variable k as a way of saying what that value is.

- **_An explicitly chosen value._** Sometimes, you’ll introduce a variable simply as a simpler way of referring to some other quantity. For example, we might say something like this:

> Let m=2k2.

Or, we could say something like this:

> Consider the set D={x∈S\|x∉f(x)}.

Here, we’re just giving a name to an existing quantity, which functions like a constant in a language like C, C++, or Java.

When writing or reviewing a proof, make sure you can clearly tell whether which of these three sorts of values that variable has. Just like variables in C, C++, or Java, this helps you indicate what your variables mean, what they store, and where they’re coming from.

You might find it helpful to view a proof as a dialog between two people. The first is you, the writer of the proof, and the second is whoever is reading the proof. Whenever you introduce a variable, it will be one of three types:

- A variable whose value the **_reader_** picks. For example, if you say something like “pick a natural number n” or “consider an arbitrary set A,” then you are telling the reader “hey reader, you can choose whatever value you’d like for this variable.”

- A variable whose value **_you_** pick. For example, if you say something like “let r=k+1,” then you are telling the reader “hey reader, you do not have a choice here. I have selected the value k+1 for r.”

- A variable whose value neither of you pick. For example, suppose you say something like “since n is even, there is an integer k such that n=2k.” Here, you and the reader both agree that there is some choice of k that works here, and you’re agreeing that the value of k will be selected to meet that requirement. However, you yourself didn’t say “I want you to pick this value as k,” nor did you tell the reader “please pick a value of k for me.”

To see how these rules come into play, let’s look at one possible proof of this result:

> **_Theorem_**: For any integer n, if n is even, then n2 is even.

Here’s a not-so-great proof of this result:

**_⚠ Incorrect! ⚠ Proof:_** For every even integer n, there exists an integer k where n=2k. Therefore, for any even integer n and any integer k, we see that

n2=(2k)2=4k2=2(2k2),

so for any arbitrary integer m where m=2k2, we see that n2=2m. Thus for any even integer n and integer m we see that n2=2m, so n2 is even, as required. ◼

Let’s focus on a few of sentences. For starters, let’s look at this sentence from the first paragraph:

For every even integer n, there exists an integer k where n=2k.

The intent here is clear: we're trying to prove something about all integers n, so the proof talks about "every even integer n." However, this is not the correct way to do this. Specifically, this way of discussing n means n does not fall into any of the three aforementioned categories:

- It's not universally-instantiated: we haven't asked the reader to choose n, nor have we said something like "let n be an even integer."

- It's not existentially-instantiated: there is no value the reader and writer agree exists that we are just giving a new name to.

- It's not a specifically-chosen value: we are not giving a new name to an existing quantity.

If, in the course of writing a proof, you wish to make a claim that works for all choices of some value, the correct way to do it is to ask the reader to make the choice and then show the result works regardless of what that choice is. That's not done by saying "for every even integer n," but by saying something like "let n be an even integer" or "pick some even integer n."

Let's continue onward in this proof. In the next sentence, we see the following:

Therefore, for any even integer n and any integer k, we see that \[…\].

There are two issues here. The first is a repeat of the same error from earlier: we should not be talking about "any even integer n," but instead ask the reader to choose some value for n that we then use throughout the proof. The second is how we talk about k. As before, we should not say "for any integer k." That's generally not a good idea. More importantly, though, this is the wrong way to introduce k. In this proof, k should be existentially-introduced: we know n is even, so some integer k exists where n=2k. The value of k is not something that we the proof writer get to pick: we can't choose k to be whatever we want to be, since only one choice of k will make n=2k. We therefore should not be talking about "for all integers k."

Let's continue on in the sentence:

n2=⋯=2(2k2), so for any arbitrary integer m where m=2k2, …

Here, we've reached the point where we know n2=2(2k2). If we specifically pick m=2k2, then we can get some result. But the way we do that here is incorrect. Writing "for any arbitrary integer m where m=2k2" makes the same mistakes as before: avoid talking about "for any arbitrary integer m", and this doesn't work for every integer m but only the specific choice of m=2k2. It's like the famous quote attributed to Henry Ford: "the customer can have any color they want as long as it's black."

The last sentence of this proof makes the same mistake:

Thus for any even integer n and integer m we see that n2=2m, so n2 is even, as required.

We shouldn't be talking about "any even integer n" and should have, much earlier in the proof, asked the reader to choose n for us. Similarly, it's not the case that n2=2m for every integer m. Only one specific choice works.

1. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** There are no nonzero real numbers x and y where x+yx=yx+y.

**_Proof:_** Assume for the sake of contradiction that there are nonzero real numbers x and y where x+yx=yx+y. Then for all nonzero real numbers x and y we can cross-multiply to get (x+y)2=xy. We consider three cases:

- _Case 1:_ xy<0. We know (x+y)2≥0, which means that (x+y)2≥0>xy, so (x+y)2≠xy. This contradicts the fact that (x+y)2=xy.

- _Case 2:_ xy=0. This means that x=0 or that y=0, contradicting that x and y are nonzero.

- _Case 3:_ xy>0. In particular, this means that −xy<0. Notice that (x+y)2=x2+2xy+y2, so since (x+y)2=xy, we see that xy=x2+2xy+y2. In particular, this means that −xy=x2+y2. Because x2≥0 and y2≥0, we see that x2+y2≥0, so we have that x2+y2≥0>−xy, contradicting that x2+y2=−xy.

In all cases, we reach a contradiction, so our assumption was wrong. Thus for all nonzero real numbers x and y, we have x+yx≠yx+y. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-9)

This proof does not adhere to our style conventions. Notice that in the second sentence, we talk about "for all nonzero real numbers x and y," but in the previous sentence we already existentially-introduced x and y. In a sense, we're redefining variables that already exist, which is not permitted.

Notice that in the concluding sentence of the proof we talk about "all nonzero real numbers x and y." This is actually perfectly fine; the convention in a proof by contradiction is that after you reach a contradiction, you state what conclusion should be drawn from it. The conclusion really is that something holds for all real numbers x and y.

Here's a revised version of the proof that corrects the error:

**_Theorem:_** There are no natural numbers m and n where m2n=1137 and m is odd.

**_Proof:_** Suppose for the sake of contradiction that m and n are natural numbers where m2n=1137 and where m is odd. Cross-multiplying the previous equality gives us that 137m=2n.

- _Case 1:_ n=0. Then we see that 2n=20=1. Since 2n=137m, we see that 1=137m, which we rearrange to m=1137. This is impossible because m is a natural number and 1137 is not.

- _Case 2:_ n≥1. Then we can write n=r+1 for some natural number r, and we see that 2n=2r+1=2⋅2r. This means that 2n is even. However, 2n=137m and 137m is odd, since m is odd and 137=2⋅68+1 is odd. This means that 2n is both odd and even, which is impossible.

In either case, we reach a contradiction, so our assumption was wrong. Thus there are no natural numbers m and n where m2n=1137. ◼

---

### Exercises

1. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For all integers m and n, if m+n is even, then either m and n are even or m and n are odd.

**_Proof:_** We proceed by contrapositive and will prove that if one of m and n is even and the other is odd, then m+n is odd. We consider two cases:

- _Case 1:_ m is even and n is odd. Then for all integers r and s, we have m=2r and n=2s+1. We then see that m+n=2r+2s+1=2(r+s)+1. Now pick any integer t where t=r+s. We then see that m+n=2t+1, so for every even integer m and odd integer n, we see that m+n is odd.

- _Case 2:_ m is odd and n is even. Pick m=137 and n=106. We then see that m+n=243=2⋅121+1, so for every odd integer m and even integer n we see that m+n is odd.

In each case m+n is odd, as required. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-10)

This proof does not adhere to our style conventions. There are several errors here:

- After introducing the contrapositive of our implication, we never actually ask the reader to choose values for m and n. We need to do that for two separate reasons: we need to state our assumptions and want-to-show, and at present m and n have not been given values.

- In Case 1, we say "for all integers r and s, we have m=2r and n=2s+1. But this is not true: given m and n, there's exactly one choice of r and s that works. More fundamentally, we have universally-introduced r and s, which is what we do if want to prove something about all choices of r and s, rather than existentially-introduced r and s, which is what we do if we know values exist and just need to give names to them.

- In Case 1, we say "now pick any integer t where t=r+s." Asking the reader to make a choice is what we do for universal instantiation. Here, we are just giving a new name (t) to an already-existing quantity (r+s), so we shouldn't frame it as a choice to the reader. Instead, we should just say what t is.

- In Case 1, we conclude by talking about "every even integer m and odd integer n," which we should not do. We should treat m and n as though they have specific values, just one we didn't pick.

- In Case 2, we give specific values for m and n. This is not permitted: this proof needs to work regardless of what m and n are, so we should treat them as though they are chosen by the reader. Here, we're acting as though we get to pick them.

Here's a revised version of the proof that corrects the error:

**_Theorem:_** For all integers m and n, if m+n is even, then either m and n are even or m and n are odd.

**_Proof:_** We proceed by contrapositive and will prove that if one of m and n is even and the other is odd, then m+n is odd. So choose any integers m and n where one of m and n is even and the other is odd. We consider two cases:

- _Case 1:_ m is even and n is odd. Then there are integers r and s where m=2r and n=2s+1. We then see that m+n=2r+2s+1=2(r+s)+1. Thus there is an integer t (namely, t=r+s) where m+n=2t+1, so m+n is odd.

- _Case 2:_ m is odd and n is even. Then there are integers r and s where m=2r+1 and n=2s. This means that m+n=2s+1+2r=2r+2s+1, and by the reasoning from Case 1 we see that m+n is odd.

In each case m+n is odd, as required. ◼

---

2. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** There are no nonzero real numbers x and y where x+yx=yx+y.

**_Proof:_** Assume for the sake of contradiction that there are nonzero real numbers x and y where x+yx=yx+y. Then for all nonzero real numbers x and y we can cross-multiply to get (x+y)2=xy. We consider three cases:

- _Case 1:_ xy<0. We know (x+y)2≥0, which means that (x+y)2≥0>xy, so (x+y)2≠xy. This contradicts the fact that (x+y)2=xy.

- _Case 2:_ xy=0. This means that x=0 or that y=0, contradicting that x and y are nonzero.

- _Case 3:_ xy>0. In particular, this means that −xy<0. Notice that (x+y)2=x2+2xy+y2, so since (x+y)2=xy, we see that xy=x2+2xy+y2. In particular, this means that −xy=x2+y2. Because x2≥0 and y2≥0, we see that x2+y2≥0, so we have that x2+y2≥0>−xy, contradicting that x2+y2=−xy.

In all cases, we reach a contradiction, so our assumption was wrong. Thus for all nonzero real numbers x and y, we have x+yx≠yx+y. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-11)

This proof does not adhere to our style conventions. Notice that in the second sentence, we talk about "for all nonzero real numbers x and y," but in the previous sentence we already existentially-introduced x and y. In a sense, we're redefining variables that already exist, which is not permitted.

Notice that in the concluding sentence of the proof we talk about "all nonzero real numbers x and y." This is actually perfectly fine; the convention in a proof by contradiction is that after you reach a contradiction, you state what conclusion should be drawn from it. The conclusion really is that something holds for all real numbers x and y.

Here's a revised version of the proof that corrects the error:

**_Theorem:_** There are no nonzero real numbers x and y where x+yx=yx+y.

**_Proof:_** Assume for the sake of contradiction that there are nonzero real numbers x and y where x+yx=yx+y. We can cross-multiply to get (x+y)2=xy. We consider three cases:

- _Case 1:_ xy<0. We know (x+y)2≥0, which means that (x+y)2≥0>xy, so (x+y)2≠xy. This contradicts the fact that (x+y)2=xy.

- _Case 2:_ xy=0. This means that x=0 or that y=0, contradicting that x and y are nonzero.

- _Case 3:_ xy>0. In particular, this means that −xy<0. Notice that (x+y)2=x2+2xy+y2, so since (x+y)2=xy, we see that xy=x2+2xy+y2. In particular, this means that −xy=x2+y2. Because x2≥0 and y2≥0, we see that x2+y2≥0, so we have that x2+y2≥0>−xy, contradicting that x2+y2=−xy.

In all cases, we reach a contradiction, so our assumption was wrong. Thus for all nonzero real numbers x and y, we have x+yx≠yx+y. ◼

---

## Make Specific Claims About Specific Variables

Mathematical proofs work by taking specific quantities, represented as expressions of variables, and manipulating those quantities to arrive at a result. Therefore, statements made in a mathematical proof need to be made in reference to specific values rather than stated in the abstract. A common mistake when writing proofs is to instead describe, at a high level, why a result ought to be true, then conclude that the result is indeed true. Here's an example of this:

**_Theorem:_** For every integer n, if n is even, then n2 is even.

**_⚠ Incorrect! ⚠ Proof:_** Every divisor of a number is also a divisor of the square of that number. This means that if two divides a number, then two divides its square. Thus if n is even, then n2 is even. ◼

Notice that this entire proof discusses numbers in general at a high level. None of the statements here, except the very last one, reference any variables. As a result, while this proof may have some good ideas in it, it's written too abstractly to be rigorous. Unfortunately, there really isn't a way to salvage this proof. We pretty much have to scrap it and start over, operating at a lower level, and with a higher degree of precision.

In the example proof above, the statements made happen to be true. However, it's easy to reach incorrect conclusions when reasoning this way and not focusing on concrete, specific values. We'll see more examples of this later in the quarter.

When you’re first studying proof-based mathematics, you’ll likely have a number of intuitions about how different types of objects behave. Some of these intuitions are great, and you should keep using them. Other intuitions, on the other hand, can be at odds with what the math says, and when that happens, you should refine those intuitions so that they guide you in the right direction.

The only way to know which of your intuitions are good and which need tuning is to explicitly validate those intuitions by attempting to formalize them mathematically. To do so, we ask that you speak with mathematical precision and to show how specific applications of definitions give you your result. If you’re able to do this, great! It likely means your intuition is pointing you the right way. If not, that might indicate that your intuition might be suggesting something that the math says isn’t true, in which case it’s a good thing that you tried formalizing things! At that point, you should back up, pause, and see whether the result is still true for some other reason or whether you need to reshape your intuition for the future.

### Exercises

1. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

In what follows, we say that a natural number n is called a **_Hilbert number_** if there is a natural number k where n=4k+1.

**_Theorem:_** For all natural numbers m and n, if m and n are Hilbert numbers, then so is mn.

**_Proof:_** Let m and n be Hilbert numbers. We need to show that mn is also a Hilbert number.

When multiplying numbers together that have some property, the product also has that property. For example, the product of two even numbers is even, the product of two odd number is odd, the product of two numbers between 0 and 1 inclusive is between 0 and 1 inclusive, etc. Thus since m and n are Hilbert numbers, their product must be as well. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-12)

This proof does not adhere to our style conventions. The crux of this argument is the high-level statement "when multiplying numbers together that have some property, the product also has that property." This is both far abstract (what counts as a "property?") and is not true in general. For example, the product of two negative numbers will not be negative, the product of two numbers between 1 and 2 is not necessarily between 1 and 2, etc. Because this line of reasoning is not sufficient, rewriting this proof is a more difficult exercise. We essentially need to scrap the proof and start over.

There are many other issues here (e.g. we don't state our assumptions and want-to-show), but given that we need to rewrite the proof from scratch we won't go into those details here.

Here's a more proper way to prove this result:

**_Theorem:_** For all natural numbers m and n, if m and n are Hilbert numbers, then so is mn.

**_Proof:_** Let m and n be Hilbert numbers. We need to show that mn is a Hilbert number.

Since m and n are Hilbert numbers, there exist natural numbers r and s such that m=4r+1 and n=4s+1. We then see that

mn=(4r+1)(4s+1)=16rs+4r+4s+1=4(4rs+r+s)+1.

This means there is a natural number t, namely, 4rs+r+s, such that mn=4t+1. Thus mn is a Hilbert number. ◼

---

2. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** There exists a Hilbert number n>1 such that there are Hilbert numbers p,q>1 where n=pq.

**_Proof:_** We are asked to show that some Hilbert number is the product of two other Hilbert numbers (all excluding 1, which would make this trivial because 1⋅1=1.) Earlier we proved that the product of two Hilbert numbers is also a Hilbert number. Since there are infinitely many pairs of Hilbert numbers we could multiply together and infinitely many Hilbert numbers, there must be some Hilbert number n>1 where n=pq for Hilbert numbers p and q other than 1. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-13)

This proof does not adhere to our style conventions. This argument does not engage with the formal definition of a Hilbert number - it never talks about numbers of the form 4k+1 \- and so it can't be a rigorous proof. The argument works at a high level by restating other results we've already proved and talking about how there's infinitely many numbers of two different forms, so there must be some overlap. That isn't true: for example, there are infinitely many prime numbers, but the product of two prime numbers is never prime. As before, we pretty much have to start over from scratch here by throwing out this proof and writing a new one.

Finding numbers that work here is more or less an exercise in trial and error - or a quick Python script:

```
for i in range (1, 10):
       for j in range(1, 10):
           num1    = 4*i + 1
           num2    = 4*j + 1
           product = num1 * num2

           if product % 4 == 1:
               print(f"{num1} * {num2} = {product}")
```

This outputs a bunch of numbers that work. I personally like 21⋅37=777 and so that's what I've put in the revised proof.

**_Theorem:_** There exists a Hilbert number n>1 such that there are Hilbert numbers p,q>1 where n=pq.

**_Proof:_** Pick n=777,p=21, and q=37. We see by inspection that pq=n, and we also have n>1,p>1, and q>1. Finally, note that these are all Hilbert numbers: 21=4⋅5+1,37=4⋅9+1, and 777=4⋅194+1. ◼

---

## Don’t Repeat Definitions; Use Them Instead

When writing a proof, make sure that you do not restate definitions in the abstract. Instead, apply them to specific circumstances to draw specific conclusions.

For example, consider the following three (not good) excerpts from three (not good) proofs:

**_Incorrect Approach 1_**: We know that n is even. Every even number can be written as twice some integer. Therefore, we see that n=2k for some integer k.

**_Incorrect Approach 2_**: We know that n is even. Every even number can be written as 2k for some integer k. Therefore, we see that n=2k for some integer k.

**_Incorrect Approach 3_**: We know that n is even. Every even number m can be written as m=2k for some integer k. Therefore, we know that n=2k for some integer k.

In each of these cases, we begin with the fact that n is even, and we arrive at the endpoint that n=2k for some integer k. The issue is in the middle sentences. In each case, we're essentially restating the definition of what an even number is. This is unnecessary and makes our proof longer. Here's a much shorter, cleaner way to do this:

We know n is even, so there is an integer k where n=2k.

"But wait!," you might say, "don't I need to tell the reader where that integer k is coming from?" The answer is "no, you don't." When you're writing a proof, you should assume that the reader is familiar with all the relevant terms and definitions. Your goal isn't to say _what those definitions are_, but rather _how those definitions work together to give your result_. Think of it this way: the mathematical definitions we have are like the rules of a game. The proof should be you playing the game with the reader, rather than pausing every few minutes to remind the reader what the rules of the game are. (Imagine watching a sports match where the players keep interrupting the action to explain why they're allowed to do what they're doing!)

There's a further reason not to repeat definitions in your proof: you run the risk of violating other checklist rules. Let’s go one at a time through the three examples above that we advise against. The first one is far too general (“Every even number can be written as twice some integer”) and therefore breaks our advice of making specific claims about specific variables. The second one (“Every even number can be written as 2k for some integer k”) is a variable scoping error – k is a placeholder here for "the number that some abstract even integer is twice as big as." The third one is making specific claims about the variable m, but in that case m is a placeholder (you didn't pick it, the reader didn't pick it, and it isn't something already known to exist).

And one more reason to not restate definitions: it makes proofs shorter. Often, when we see students struggling with proofwriting, our advice is to write _less_ rather than _more_, and it's often because of this specific rule.

To summarize - avoiding restating definitions in the abstract makes the proof flow more clearly for the reader, avoids variable scoping errors, and reduces the amount of writing required. Isn't that great?

### Exercises

1. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For every odd natural number n, the sum of n and the next four natural numbers is odd.

**_Proof:_** Pick an odd natural number n. We need to show that the sum n+(n+1)+(n+2)+(n+3)+(n+4) is odd.

An odd natural number m is one where m=2k+1 for some integer k. Therefore, since n is odd, we can write n=2k+1 for some integer k.

Next, note that n+(n+1)+(n+2)+(n+3)+(n+4)=5n+10. We then see that

5n+10=5(2k+1)+10=10k+5+10=10k+15=2(5k+7)+1.

Thus there is an integer m, namely, 5k+7, such that 5n+10=2m+1. An odd number is one that can be written as twice an integer plus one, which means that 5n+10 is odd, as required. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-14)

This proof does not adhere to our style conventions. In particular, it restates the definition of an odd number in two separate places: the first sentence of the second paragraph, and the last sentence of the last paragraph. (The first sentence of the second paragraph could also be said to violate the "Scope and Properly Introduce Variables" rule, since m is a placeholder.)

Here is a better way to write this proof:

**_Theorem:_** For every odd natural number n, the sum of n and the next four natural numbers is odd.

**_Proof:_** Pick an odd natural number n. We need to show that the sum n+(n+1)+(n+2)+(n+3)+(n+4) is odd.

Since n is odd, we can write n=2k+1 for some integer k. Next, note that n+(n+1)+(n+2)+(n+3)+(n+4)=5n+10. We then see that

5n+10=5(2k+1)+10=10k+5+10=10k+15=2(5k+7)+1.

Thus there is an integer m, namely, 5k+7, such that 5n+10=2m+1. This means that 5n+10 is odd, as required. ◼

---

2. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

In the context of this theorem, a Pythagorean triple is a triple (a,b,c) of positive natural numbers where a2+b2=c2.

**_Theorem:_** For every odd natural number a>1, there exist natural numbers b and c where (a,b,c) is a Pythagorean triple.

**_Proof:_** Pick an odd natural number a>1. We need to find natural numbers b and c where (a,b,c) is a Pythagorean triple.

In lecture, we proved that the square of every odd number is odd. This means that a2 is odd, and therefore that there is a natural number k where a2=2k+1. Now, let b=k and c=k+1. We need to show that (a,b,c) is a Pythagorean triple.

First, notice that

a2+b2=(2k+1)+k2=k2+2k+1=(k+1)2=c2.$

In a Pythagorean triple, all terms must be greater than zero. We know that a>1, so a is positive. We also can see that c=k+1≥1, so c>0. To see that b≥0, suppose for the sake of contradiction that b=0. This means that a2=k=0, which means that a=0. This is impossible, since by assumption we know a>1. We've reached a contradiction, so our assumption was wrong and b>0.

Overall, we have shown that a2+b2=c2 and that a>0,b>0, and c>0, which means that (a,b,c) is a Pythagorean triple, as required. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-15)

This proof does not adhere to our style conventions. There are two spots worth focusing on:

1. The first sentence of the second paragraph ("In lecture, we proved that the square of every odd number is odd") restates a general result in the abstract. The proof is fine referencing that result, but it should apply it rather than just stating it a second time at a high level.

2. The first sentence of the penultimate paragraph ("In a Pythagorean triple, all terms must be greater than zero") restates a general property of Pythagorean triples. The proof has the right idea to say something about this because it's necessary to prove this, but the way in which this is done is incorrect. This should be introduced as a goal in which the proof states it will prove something about a,b, and c specifically.

Here's how to touch up this proof:

**_Theorem:_** For every odd natural number a>1, there exist natural numbers b and c where (a,b,c) is a Pythagorean triple.

**_Proof:_** Pick an odd natural number a>1. We need to find natural numbers b and c where (a,b,c) is a Pythagorean triple.

As we proved in lecture, since a is odd, we know that a2 is odd, and therefore that there is a natural number k where a2=2k+1. Now, let b=k and c=k+1. We need to show that (a,b,c) is a Pythagorean triple.

First, notice that

a2+b2=(2k+1)+k2=k2+2k+1=(k+1)2=c2.

Next, we will prove that a>0, that b>0, and that c>0. We know that a>1, which tells us a>0. We also can see that c=k+1≥1, so c>0. To see that b≥0, suppose for the sake of contradiction that b=0. This means that a2=k=0, which means that a=0. This is impossible, since by assumption we know a>1. We've reached a contradiction, so our assumption was wrong and b>0.

Overall, we have shown that a2+b2=c2 and that a>0,b>0, and c>0, which means that (a,b,c) is a Pythagorean triple, as required. ◼

---

## Write In Complete Sentences and Paragraphs

Although proofs convey mathematical arguments, they should be written in grammatically-correct English sentences and in paragraph form.

A good check for this is what we call the **_mugga mugga test_**. Take your proof and try reading it out loud, replacing all the mathematical content with the phrase “mugga mugga.” If what comes back is grammatically correct, then you’re on the right track. On the other hand, if what you write is hard to read aloud, or just plain doesn’t sound right, it means that you might need to go back and correct things. As an example, here’s an excerpt from a not-so-great proof that if n is even, then n2 is even:

**_⚠ Incorrect! ⚠ Proof:_** Since n is even, n=2k. n2=4k2, which is 2(2k2). 2k2∈Z, so n2 is even. ◼

Let’s apply the mugga mugga test to this proof, one sentence at a time. Here’s the first sentence:

- **_Original_**: Since n is even, n=2k.
- **_Mugga Mugga Version_**: Since n is even, _mugga mugga_.

The mugga-muggaified version of this sentence isn’t grammatically correct – it has no subject and no verb. The reason for this is that the subject of the original sentence is n and the verb is “equals,” but since we’ve written out the equality using the equals sign, it got mugga-muggified in the updated version of the sentence.

More generally:

> **_Tip:_** Avoid writing sentences where mathematical notation must be treated as the verb in the sentence.

So what should we do instead? Let’s begin with what you shouldn’t do. Don’t rewrite the sentence like this in order to pass the mugga mugga test:

⚠ Since n is even, n equals 2k. ⚠

This technically passes the mugga mugga test, but it’s doing so by taking a clear mathematical statement (n=2k) and rendering the unambiguous, precise mathematical symbol = in English. The whole reason for having mathematical symbols in the first place is so that we can be precise with our notation, and this is a step in the wrong direction.

Instead, consider rewriting the sentence in a way that introduces a new subject and a new verb. There are many ways that we can do this. Here are a few options to choose from:

- **_Option 1_**: Since n is even, we can write n=2k.

**_Mugga Mugga Version_**: Since n is even, we can write _mugga mugga_. _(The subject is "we" and the verb is "can write")_

- **_Option 2_**: Since n is even, we see that there is some integer k such that n=2k.

**_Mugga Mugga Version_**: Since n is even, we see that there is some integer k such that _mugga mugga_. \*(The subject is "we" and the verb is "see")

- **_Option 3_**: Since n is even, there is some integer k where n=2k.

**_Mugga Mugga Version_**: Since n is even, there is some integer k where _mugga mugga_. (The subject is the integer k and the verb is "is.")

Notice how in each sentence we’ve introduced an explicit subject and verb in a way that passes the mugga mugga test.

Let’s look at this second sentence:

- **_Original_**: n2=4k2, which is 2(2k2).
- **_Mugga Mugga Version_**: _Mugga mugga_, which is _mugga mugga_.

This sentence has no subject and no verb, since the verb here is again the equality between n2 and 4k2. To fix this, let's restructure the sentence to include a new subject and new verb. Here are some options:

- **_Option 1:_** Notice that n2=(4k2), which we can rewrite as n2=2(2k2).

**_Mugga Mugga Version_**: Notice that _mugga mugga_, which we can rewrite as _mugga mugga_.

- **_Option 2:_** We see that n2=4(k2), which means n2=2(2k2).

**_Mugga Mugga Version_**: We see that _mugga mugga_, which means _mugga mugga_.

A common theme in the mugga mugga test is that you should avoid using math notation as the verb in a sentence. Similarly, you should avoid using mathematical notation or shorthands to abbreviate parts of sentences. There are a number of shorthands that have been developed over the years, primarily for use on blackboards where writing out longhand can take a while. For example, the word “therefore” is often abbreviated ∴, and the word “because” is often abbreviated ∵. These shorthands are just that – they’re shorthands – and should not be used in mathematical proofs except if you’re trying to write something up quickly and on a blackboard. For example, please, please, please don’t write the following:

∵n is even, n=2k for some integer k, ∴n2=4k2=2(2k2),∴n2 is even ∵n2=2m for m=2k2.

This one really, really, really fails the mugga mugga test:

_Mugga mugga_ n is even, _mugga mugga_ for some integer k, _mugga mugga_, _mugga mugga_ n2 is even _mugga mugga_ for _mugga mugga_.

This almost reads like a parody of a terrible math lecture. So please don’t write proofs like this. ☺

Just as you’re expected to write in complete sentences, you’re expected to write in complete _paragraphs_. This means that your proofs should not consist of bulleted or numbered lists of statements. For example, please don’t write proofs like these:

**_Proof_**:

- Let n be an even integer.
- Since n is even, we can write n=2k for some integer k.
- Then n2=4k2.
- So n2=2(2k2).
- Let m=2k2.
- So n2=2m.
- So n2 is even.

Although we can see what this proof is saying, this just isn’t the format that’s expected and so you shouldn’t structure things this way.

**_Why we enforce this rule:_** We primarily enforce this rule because this is the standard convention in mathematical writing and we’re hoping to train you to communicate mathematics effectively. Additionally, this rule makes proofs much easier to read by requiring you, the writer, to link your ideas together in a way that helps the argument flow.

### Exercises

1. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

In the context of this theorem, a perfect square is a natural number n where there is a natural number k such that n=k2.

**_Theorem:_** For all natural numbers n≥1, the number n(n+1) is not a perfect square.

**_Proof:_** Assume for the sake of contradiction that there is a natural number n that is ≥1 and where n(n+1) is a perfect square. Because n(n+1) is a perfect square, there is a natural number k where n(n+1)=k2.

n(n+1)=k2n2+n=k2

Also, n2+n<n2+n+1≤n2+2n+1=(n+1)2. So k2<(n+1)2, so k<n+1.

Because n≥1,n(n+1)=n2+n≥n2+1>n2. So k2>n2 so k>n.

Collectively, this means that n<k<n+1, which is impossible because k is an integer. We have reached a contradiction, so our assumption was wrong. Thus if n≥1 is a natural number, then n(n+1) is not a perfect square. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-16)

This proof does not adhere to our style conventions. Here's what this reads as if we apply the mugga mugga test. Each instance in red is a sentence with no subject or verb. Each instance in blue is not a sentence at all. Each instance in purple is a spot where a mathematical operator was used as a verb.

**_Proof:_** Assume for the sake of contradiction that there is a natural number n that is _mugga mugga_ and where _mugga mugga_ is a perfect square. Because _mugga mugga_ is a perfect square, there is a natural number k where _mugga mugga_.

_mugga mugga_

_mugga mugga_

Also, _mugga mugga_. So _mugga mugga_, so _mugga mugga_.

Because _mugga mugga_, _mugga mugga_. So _mugga mugga_.

Collectively, this means that _mugga mugga_, which is impossible because k is an integer. We have reached a contradiction, so our assumption was wrong. Thus if _mugga mugga_ is a natural number, then _mugga mugga_ is not a perfect square. ◼

Correcting each of these errors gives the following proof, which is a lot easier to read:

**_Theorem:_** For all natural numbers n≥1, the number n(n+1) is not a perfect square.

**_Proof:_** Assume for the sake of contradiction that there is a natural number n≥1 and where n(n+1) is a perfect square. Because n(n+1) is a perfect square, there is a natural number k where n(n+1)=k2.

First, notice that

k2=n(n+1)=n2+n<n2+n+1≤n2+2n+1=(n+1)2,

which shows overall that k2<(n+1)2. This in turn means that k<n+1.

Next, notice that

k2=n(n+1)=n2+n≥n2+1(since n≥1)>n2,

which means that k2>n2. This tells us that k>n.

Collectively, this means that n<k<n+1, which is impossible because k is an integer. We have reached a contradiction, so our assumption was wrong. Thus if n≥1 is a natural number, then n(n+1) is not a perfect square. ◼

---

2. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

This proof makes use of the following theorem: there are no integers p,q where q≠0 and where p2=2q2. It also makes use of the following definition: a rational number is a real number x for which there are integers p and q where q≠0 and x=pq.

**_Theorem:_** 2112 is not a rational number. (This means it's [not possible to precisely tune a piano](https://www.youtube.com/watch?v=1Hqm0dYKUx4).)

**_Proof:_** Assume for the sake of contradiction that 2112 is rational. Then 2112=pq,p∈Z,q∈Z, and q≠0.

(2112)12=(pq)122=p12q122q12=p12

Now let q′=q12 and p′=p12.q≠0⇒q12≠0⇒q′≠0, same with p and p′. But 2q′≠p′ with q′≠0,∴ contradiction. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-17)

This proof does not adhere to our style conventions. Here's what this reads as if we apply the mugga mugga test. Each instance in red is a sentence with no subject or verb. Each instance in blue is not a sentence at all. Each instance in purple is a spot where a mathematical operator was used as a verb.

**_Proof:_** Assume for the sake of contradiction that _mugga mugga_ is rational. Then _mugga mugga_, _mugga mugga_, and _mugga mugga_

_mugga mugga_

_mugga mugga_

_mugga mugga_

Now let _mugga mugga_ and _mugga mugga_. _mugga mugga_, same with p and p′.But _mugga mugga_ with _mugga mugga\_\_mugga mugga_ contradiction. ◼

Beyond the fact that this proof fails the mugga mugga test, it also violates the "scope and properly introduce variables" rule when introducing p and q in the top paragraph, the "clearly articulate your assumptions and want-to-shows" by not restating what the contradiction entails, and the "make each sentence load-bearing" rule by stating that p′≠0 even though this is not used anywhere.

Correcting each of these errors gives the following proof:

**_Theorem:_** 2112 is not a rational number.

**_Proof:_** Assume for the sake of contradiction that 2112 is rational. Then there exist integers p and q where 2112=pq and q≠0.

We can manipulate our original equality to see that

(2112)12=(pq)12,

which means that

2=p12q12

or, equivalently, that

2q12=p12.

Now let q′=q12 and p′=p12. Since q≠0, we know that q12≠0, so q′≠0. However, this means that there are integers q′ and p′ where q′≠0 and where 2q′=p′, which we know is impossible.

We've reached a contradiction, so our assumption was wrong and 2112 is not rational. ◼

---

## Avoid Quantifiers and Propositional Connectives

Related to our requirement above that proofs be written in grammatically correct English sentences and in paragraph form, we do not allow the use of quantifiers (∀ and ∃) or propositional connectives (→, ∧, ∨, ¬,  etc.) in written proofs.

If you're reading this requirement early in the quarter, you might be unfamiliar with those symbols. Don't panic! We don't expect you to have seen them before. Just mentally bookmark that when you encounter those symbols later this quarter, they shouldn't find their way into the proofs you write in this class. They'll be useful tools for expressing mathematical concepts concisely and precisely, but they'll be used _outside_ of your proofs in order to manipulate and explore the truthiness of statements before writing formal proofs about them.

So, for example, the following proof violates this rule (including the way the theorem is written):

**_Theorem:_** ∀m,n∈Z. (m is even ∧n is odd →m+n is odd)

**_Proof:_** (…) Since m is even, ∃k∈Z where m=2k. And similarly, since n is odd, we know ∃r∈Z such that n=2r+1. Then we see that

m+n=2k+2r+1=2(k+r)+1.

This means ∃s∈Z (namely, k+r) such that m+n=2s+1, so m+n is odd. (…) ■

Notice that our corrected version of this proof removes _all_ quantifiers and propositional connectives:

**_Theorem:_** For any integers m and n, if m is even and n is odd, then m+n is odd.

**_Proof:_** (…) Since m is even, there is an integer k where m=2k. And similarly, since n is odd, we know there’s an integer r such that n=2r+1. Then we see that

m+n=2k+2r+1=2(k+r)+1.

This means there is an integer s (namely, k+r) such that m+n=2s+1, so m+n is odd. (…) ■

Notice also that our corrected version of the proof still has algebraic symbols (such as =, +, −, and so on). Those are perfectly acceptable (and will be necessary in many of your proofs this quarter!), as long as sentences with algebraic expressions still pass the mugga mugga test.

**_Why we enforce this rule:_** As with the previous rule about writing in complete sentences and paragraphs, we primarily enforce this rule because this is a standard convention in mathematical writing, and we’re hoping to train you to communicate mathematics effectively. Writing in English also makes proofs clearer and easier to follow; this rule frees the reader from having to disentangle line after line of incredibly dense, symbolic logic – a process that might be more tedious and error-prone than parsing a proof that is written in English and follows common proofwriting conventions.

## Avoid the “Contradiction Sandwich”

Consider the following proof:

**_Theorem:_** For any integers m and n, if m is even and n is odd, then m+n is odd.

**_⚠ (Poor Style!) ⚠ Proof:_** Assume for the sake of contradiction that there are integers m and n where m is even, n is odd, but m+n is even. Since m is even, there is an integer k where m=2k. And similarly, since n is odd, we know there’s an integer r such that n=2r+1. Then we see that

m+n=2k+2r+1=2(k+r)+1.

This means there is an integer s (namely, k+r) such that m+n=2s+1, so m+n is odd. But this is impossible, since earlier we assumed that m+n is even.

We’ve reached a contradiction, so our assumption must have been wrong. Therefore, if m is even and n is odd, then m+n is odd. ■

This proof, as written, is logically correct. We begin by assuming the negation of our theorem, obtain some values m and n to work with, and reach a contradiction between what we show and what we assumed.

All would be right and well in the universe if not for one key fact. Look at the central part of this proof, with the first and last sentences removed. That gives this:

**_Theorem:_** For any integers m and n, if m is even and n is odd, then m+n is odd.

**_Proof:_** (…) Since m is even, there is an integer k where m=2k. And similarly, since n is odd, we know there’s an integer r such that n=2r+1. Then we see that

m+n=2k+2r+1=2(k+r)+1.

This means there is an integer s (namely, k+r) such that m+n=2s+1, so m+n is odd. (…) ■

This is almost literally a complete and correct direct proof of the theorem we’re trying to prove. (We’re missing our assume and want to show steps, but those can be added in pretty easily.)

Because the core line of reasoning in this proof works just as well as a direct proof, we call the original proof a **_contradiction sandwich_**. Essentially, the proof proceeds like this:

1. Assume, for the sake of contradiction, that the theorem is false.
2. Prove the theorem using a direct proof.
3. This contradicts that the theorem is false, so the theorem is true.

Here, the “meat” of the proof is in step (2), the actual direct proof. That’s “sandwiched” between the start and end of a proof by contradiction, which doesn’t add anything substantial to the proof.

The takeaway here is that if you finish writing a proof by contradiction, take a minute or two to read over your proof. Is it a contradiction sandwich? If so, simply remove the contradiction bits and present the direct proof on its own.

This is not to say that you shouldn't write proofs by contradiction, or that you're expected to use direct proofs whenever possible. Rather, we ask that after writing a proof you pause, reflect on what you've written, and see whether there is a clear way to simplify it in the specific case that it's a contradiction sandwich.

### Exercises

1. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For all real numbers a and b, we have \|a+b\|≤\|a\|+\|b\|.

**_Proof:_** Assume for the sake of contradiction that there exist a,b∈R where \|a+b\|>\|a\|+\|b\|.

First, we note that a≤\|a\| and that b≤\|b\|. To see this, note that if a≥0 then a=\|a\|, and that if a<0 then a<0≤\|a\|; similar reasoning establishes this for b as well.

We now consider two cases:

- _Case 1:_ a+b≥0. In that case, we see that
  \|a+b\|=a+b≤\|a\|+\|b\|.
- _Case 2:_ a+b≤0. In that case, we see that
  \|a+b\|=−(a+b)=−a+−b≤\|−a\|+\|−b\|=\|a\|+\|b\|.

In each case, we see that \|a+b\|≤\|a\|+\|b\|. But this is impossible, since we know that \|a+b\|>\|a\|+\|b\|.

We have reached a contradiction, so our assumption was wrong and for all a,b∈R we have \|a+b\|≤\|a\|+\|b\|. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-18)

This proof does not adhere to our style conventions because it's a contradiction sandwich. We assume the theorem is false and, without relying on that assumption, reach the conclusion that the theorem is true. We can thus remove the contradiction layer like this:

**_Theorem:_** For all real numbers a and b, we have \|a+b\|≤\|a\|+\|b\|.

**_Proof:_** Let a and b be real numbers. We need to show that \|a+b\|≤\|a\|+\|b\|.

First, we note that a≤\|a\| and that b≤\|b\|. To see this, note that if a≥0 then a=\|a\|, and that if a<0 then a<0≤\|a\|; similar reasoning establishes this for b as well.

We now consider two cases:

- _Case 1:_ a+b≥0. In that case, we see that
  \|a+b\|=a+b≤\|a\|+\|b\|.
- _Case 2:_ a+b≤0. In that case, we see that
  \|a+b\|=−(a+b)=−a+−b≤\|−a\|+\|−b\|=\|a\|+\|b\|.

In each case, we see that \|a+b\|≤\|a\|+\|b\|, as required. ◼

---

2. Does the following proof adhere to the style expectation outlined in this section? If not, rewrite it so that it does.

**_Theorem:_** For all integers n, if n2 is even, then n is even.

**_Proof:_** Assume for the sake of contradiction that there is an integer n where n2 is even but n is odd.

Since n is odd, there is an integer k where n=2k+1. This means that

n2=(2k+1)2=4k2+4k+1=2(2k2+2k)+1.

This means that there is an integer m, namely 2k2+2k, such that n2=2m+1. This means that n2 is odd, contradicting the fact that n2 is even.

We have reached a contradiction, or our assumption was wrong and if n2 is even, then n is even. ◼

[Solution](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist#solution-collapse-19)

This proof does adhere to our style requirements. This is not a contradiction sandwich: the proof actively relies on the assumption that n is odd to reach a contradiction, and we could not assume n was odd in a direct proof.

That being said, this _could_ be rewritten as a proof by contrapositive, and indeed I personally think it's more elegant when written out that way. However, there's no requirement that we use a proof by contrapositive here.

---

---

[source](https://web.stanford.edu/class/archive/cs/cs103/cs103.1268/proofwriting_checklist)
