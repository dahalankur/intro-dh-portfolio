---
layout: post
title: "Using Voyant Tools"
date: 2022-10-06
categories: jekyll update
---

According to their [about page](https://voyant-tools.org/docs/#!/guide/about), Voyant 
is a "web-based text reading and analysis environment designed to facilitate reading and interpretive practices for digital humanities students and scholars as well as for the general public." In my opinion, Voyant is much more powerful and flexible than that, for the set of tools it provides access to is more than enough to perform complex textual analysis, data cleaning,
statistics gathering, and even pre-processing to feed into powerful NLP language models. In this blog post, I will be reflecting on using this powerful tool on a corpus of my choice -- William Shakespeare's __The Tragedy of Hamlet__. I wanted to explore this play since it was one of the first works of Shakespeare I was introduced to. This is the screen I was greeted
with initially after I entered the URL to Hamlet:

<img src="../assets/hamlet.png" alt="hamlet voyant tools welcome screen" width="650"/>

The first thing I noticed is the word cloud, which showed that the words "hamlet", 
"lord", and "king" are the most prominent words in the corpus, which was expected. I am 
surprised that I was not greeted with stop words in the word cloud (like I was when I tried 
creating my own word cloud in Python without pre-processing the text), which leads me to 
believe that Voyant tool automatically performs some level of textual pre-processing 
on every text it is fed. This is wonderful news for people who want to directly dive into the 
analysis of the corpus but there should have been an option (that is easily findable) to 
view stop words as it may be helpful in some textual analysis. Nevertheless, the initial
screen shown by Voyant is a gold mine of information. The summary at the bottom left 
confirmed the depiction of the words in the word cloud, and I was amazed to see 
keywords in context shown as well on the bottom right pane. This was interesting to me because
I completed a [Programming Historian Lesson on Keywords in Context](https://dahalankur.github.io/intro-dh-portfolio/lessons/n_grams.html).

I was interested in what exactly "ham" was referring to when it was shown as the most frequent 
word in the corpus. After browsing the text file it downloaded from the URL, I saw that the 
word was "Ham." (notice the period, indicating shortening of the name "Hamlet"). This is an interesting
example of tokenization by automatic tools like Voyant where they tokenize everything without 
analyzing the context of the words in the corpus. In this case, "Ham." was simply referring to the 
dialogues by Hamlet, which explains its high frequency. Ideally, if I was analyzing Hamlet and 
using Voyant to help me pre-process this corpus for NLP, I would not be interested in "Ham."
being the most frequent word. In fact, I'd argue that it carries the same weight as a stop-word in this case.

Otherwise, the tool is very powerful and I was impressed by the "Links" and "Bubblelines" 
visualization in Voyant. Moreover, the ability to view trends for individual keywords is a 
great feature and it reminded me of Hathitrust Bookworm. Here's an example of the word "king" and 
its trend across the corpus -- Shakespeare fans can let me know the reason for the spike in 
relative frequency of "king" in segment eight of the text!

<img src="../assets/king.png" alt="hamlet voyant tools welcome screen" width="650"/>


Overall, Voyant Tools is an incredibly powerful tool. I also tried uploading a PDF document 
to the website and I was surprised to find out that it can also analyze PDFs. OCR is most 
probably being used to read the text but this increases the versatility of the tool immensely.
I did wonder about some shortcomings of the tool as I was using it, and that was the lack of 
usability in that finding and changing settings (setting custom stop words, removing stop words, etc.) is not too intuitive. Moreover, when a word cloud is displayed, would the relative weighted
frequency be a good indicator of the importance of words in a corpus compared to simply using 
raw frequencies? Sometimes, this may lead to biased visualization which may subconsciously 
bias the analysis of the text.