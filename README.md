# polyfills-no-more

Many 3rd-party packages tend to overbloat your vendor directory with unnesessary polyfills.
Along of wasting extra disk space, your also have to deal with warnings like "Duplicate declaration of function ..."
in your IDE and broken autocompletion.

This is mostly common case with Symfony components (or packages, using Symfony components), but not only.
While the authors of such packages find "good enough" atguments to explain their approach, IMHO, it is doubtful
and outdated.
Today it is a very rare case, that your provider does not allow you to install mbstring or iconv extension, etc.
With modern containerization techniques you can create any environment nesessary for you project.
And arguments like "some projects run php 5.3 but want to use some features from php 8.5" are mostly ridiculous,
**You Arent Gonna Need It**. Rare real-world cases of usage of polyfills is not an excuse to explicitly put them into 
"require" section of that packages.

So, while you are probably will not be able to convince the authors of such packages, you can simply get rid of 
unnesessary dependencies.
