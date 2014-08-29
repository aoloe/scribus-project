- pierre's branch
- the indic scribus version
- http://wiki.scribus.net/canvas/Complex_Script_Functionality


- for comments use https://github.com/aoloe/scribus-project/issues/1
- fork, branch and pull request to edit the project description


~~~~
12:25 < prp-e> OK, How can I add support RTL Persian and Arabic support to Scribus text frame?
12:25 < a-l-e> but you could also look for share/editorconfig/ in your installed version
12:26 < a-l-e> prp-e: some time ago christoph wrote that a team is working on it...
12:26 < a-l-e> there have been a few tries to implement it, but none of them has lead to something usable.
12:27 < prp-e> Oh, I see.
12:27 -!- PaulePan1er [~paul@mail.gw90.de] has joined #scribus
12:28 < a-l-e> if you have the skills to work on it, what i can suggest you, is to do small patches that go in that direction.
12:28 < prp-e> I am a native Persian speaker, I can help, if you would like.
12:28 < a-l-e> well, a c++ native speaker would be more helpful, there :-)
12:28 < a-l-e> you need some math skills too
12:29 < a-l-e> and you need lot lot of patience, too...
12:29 < prp-e> :D
12:30 < a-l-e> so, how good are you in c++ and maths?
12:31  * a-l-e is leaving for lunch very soon
12:32 < prp-e> a-l-e, I know C/C++.
12:32 < prp-e> But math is the problem :D
12:32 < a-l-e> well, if you want to give it a try, you're welcome!
12:33 < a-l-e> you should read about what has already been done, and try to find out what are the small changes that can be done to get it there...
12:34 -!- rethus [rethus@madison.bouncerstation.com] has quit [Ping timeout: 244 seconds]
12:34 -!- PaulePanter [~paul@mail.gw90.de] has quit [Ping timeout: 244 seconds]
12:34 < a-l-e> there are two sources of code you will have to read: the indic version of scribus (which does work, but is not integrated into the main scribus code) and the work pierre did a few years ago.
12:35 < prp-e> OK, if there's a git or launchpad repository, I would read sources.
12:36 < a-l-e> very soon, i'm going to create a platform for describing projects where the community can help...
~~~
