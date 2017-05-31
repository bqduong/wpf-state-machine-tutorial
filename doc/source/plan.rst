Always have a Plan
******************

.. epigraph::

   Weeks of programming can save you hours of planning. |br|
   -- unknown

So let's make one. First on the meta layer we want to create a solid_, MVVM_ structured application with our development being `driven by tests <https://en.wikipedia.org/wiki/Test-driven_development>`_. In the spirit of `single responsibilities <https://en.wikipedia.org/wiki/Single_responsibility_principle>`_ I prefer the view models to be just decorating_ the models. And to have a nice story from the use cases/activities to the tests, I like to focus on behaviors_. I know, with all that we have a full plate – and to make things worse: I am a lazy developer: `I like the compiler to do the work for me so I make fewer mistakes <http://www.aristeia.com/Papers/IEEE_Software_JulAug_2004_revised.htm>`_.

.. _solid: https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)

.. _MVVM: https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel

.. _decorating: https://en.wikipedia.org/wiki/Decorator_pattern

.. _behaviors: https://en.wikipedia.org/wiki/Behavior-driven_development

As we have no customer waiting and the GUI is not that important, we can be relaxed and build the app from the bottom up. So we safe the time to create a visual prototype. Thus, let’s focus on the models – where the actual work is done!

What not to Achieve
===================

|yinyang|

In :doc:`goal` we talked about what we want to achieve – and when. But a good programmer should be an optimistic pessimist, a good natured realist. A pure optimist will produce an app with a very narrow happy path. A pure pessimist wouldn’t get anything done; and if it got done, it would be dull. Now we swap our hats and think about what could go wrong.

What definetly shouldn't happen is that the app crashes when it hits a bump. Also mutating into a zombi on a hickup is also a no no. Off the top of my head, I can think of the following undesirables:

* File not found
* File not an image
* Image has differing size
* Save location is not writable
* Save location has not enough disk space
* Out of memory (tough)

After this quick brain storming session we can prepare and incorporate failure into our design!

Models
======


.. |br| raw:: html

   <br />

.. |yinyang| raw:: html

   <center><a title="By Gregory Maxwell [Public domain], via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File%3AYin_yang.svg"><img width="64" alt="Yin yang" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/Yin_yang.svg/64px-Yin_yang.svg.png"/></a></center>