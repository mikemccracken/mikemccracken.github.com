<!--
.. title: The editing pass
.. date: 2007/10/09 00:41
.. slug: the-editing-pass
.. link:
.. description:
.. tags: programming
-->


Anything worth writing is worth re-writing. This applies to code as well as prose.

I give paper sections and important emails a while to sit after I write them, and they always benefit from another look with fresh eyes. I think that doing this with code is worth thinking about.

Once you get a piece of code to the point where you believe it works - it's passing its tests - go back over it and *edit it*. That is, go back and edit it for clarity, flow, and style. Just as if it were an essay.

This is particularly important for tests. If a test fails, it should tell a clear story that explains exactly what failed, and what it was expecting.

Things to consider editing out are vague variable or function names, and non-idiomatic shortcuts. Control flow can get tangled when working out a solution. Make it obvious. One-liners often don't tell the full story. When you come back to a piece of code, you know the chase. It's the first loose thread of a bug, a failed test, or an occurrence of a symbol you need to refactor. What you need is the story around it, and solid code will fill that in.

You can learn this by sharing your code or by waiting a while and reading it over again. It's easier said than done - I don't always do it, but I do know: an editing pass can do you good.

Something to think about: would a professional code editor help or hurt in the long run?
