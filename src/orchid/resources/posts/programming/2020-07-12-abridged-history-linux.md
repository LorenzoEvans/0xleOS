---
title: 'The Semi-Abridged History Of Linux.'
tags:
    - systems
    - programming
---
<head>
<meta property="og:image" content="/assets/media/topology.jpeg">
<div class="article-container">
    <p >So, you’ve used a computer or two in your day, I’m sure, and you’ve been learning to code, or delving into the murky world of hacking (cue ominous music), and then, one day you find yourself wanting more control over your machine- more flexibility, more customizability, more freedom.
    </p>
    <p >Clicking, dragging and dropping files becomes a chore, and someone, somewhere, said real programmers use CLI’s, because GUI’s are for <i>t3h n00bz</i> (Yeah, I’m from <b><i>that</b></i> era of the internet, deal with it), or maybe you’ve had it with new versions of your current OS completely doing away with utilities or hot-keys that you really depended on, either way, dadgummit you are tired of it. You’ve decided it’s time for a change. Well, all of this sounds fine and dandy, but where does one gain the ability to surpass the mundanity? Where does one go to shed such novice ways?
    </p>
    <h1 style="margin:0 auto;margin-bottom:15px;">1. Enter Linux</h1>
    <img src="/assets/media/tuxnix.jpg" 
     alt="A goofy eyed, cartoon penguin sitting down in front of a gray background"
     style="height:50%;width:50%;margin: 0 auto;"
    />
<p style="line-height:23px;margin-top:15px;">The penguin is your friend. His name is Tux. He's the mascot for Linux.</p> 
<p>Now, before we dive into this thing, we need to get a little backstory going, if you will, because, Linux is cool but, well, what the hell <i>is</i> it?</p>
<p>Put simply, it's <b>an operating system</b>.
</p>
<p style="display:flex;flex-directon:column;justify-content:space-evenly;font-size:22px;"> Well.. what is that?
</p>
 <h3 style="margin:0 auto;"><i><b>The Slightly Abridged & Winding History of Operating Systems</b></i></h3>
 <img src="/assets/media/osdiagram.jpg" style="height:50%;width:50%;align-items:center;align-content:center;align-self:center; margin: 5px 5px;"/>
 <p>An operating system is a well known example of system software, that manages the lower level responsibilities of your computer, such as scheduling tasks, processor time, communicating with I/O hardware (keyboard + mouse), et cetera, so that you don’t have to. Believe it or not, there was once a world with computers, wherein there existed no OS, often referred to as mainframes, or more colloquially, <i>big iron </i> (Totally naming a VM that one day). Back when mainframes were all the latest rage in technology, how did people use them to compute tasks, if there was no operating system?</p>
<img src="/assets/media/gracehopper.jpg" style="height:50%;width:50%;align-items:center;align-content:center;align-self:center; margin: 5px 5px;"/>
<p>The answer is, they carried all of their programs, and the data necessary for the program to accomplish whatever task it was designed to do, on punch cards/magnetic or paper tape. Those days are long gone, so we don’t often appreciate how effort intensive and grueling programming used to be (Yes, those magnetic spools are the JavaScript, your JSON, your database, and there was absolutely no git revert --commit-hash for when you messed up).
</p>
<p class="ttf spacing" style="font-size:22px;line-height:26px;">I would be remiss if I didn’t point out that in this picture is the woman, the myth, the legend, <a href="https://en.wikipedia.org/wiki/Grace_Hopper">Grace Hopper</a>, who wrote the first compiler, and invented <a href="https://en.wikipedia.org/wiki/FLOW-MATIC"><b><i>FLOW-MATIC</i></b></a>, the first english-like data processing language, as well as being directly involved in the creation of<a href="https://en.wikipedia.org/wiki/COBOL"><b><i>COBOL</i></b></a>. Talk about being <i>accomplished</i>.</p>
<p>As mainframe computers became more powerful, software, even in it’s infancy, began to eat the world. There were no longer queue’s of people waiting in line with their punch cards, and the programmers didn’t run their own programs anymore, but rather passed the punch cards off to machine operators. Security features began to be implemented to track what “code” accessed what file, and to limit what files certain software could access.</p>
<p>Time progressed, and these features, along with many other ones, began to coagulate into a program that would be started before the first “job program” the computer would run, that would do things such as signal when tapes needed to be changed, count the number of cards read, pages printed, etc. These programs and their ilk were referred to as “monitors”, before the term operating system was coined.</p>
<p>Circa 1956, the first operating system, <b>GM-NAA I/O</b>, was produced by the research division of GM, for use on an IBM mainframe, and brought about an era of vendor/hardware specific operating systems, each equipped with it’s own syntax, debugging tools, commands, meaning every time a new machine was released, all of the applications would have to be manually altered, refactored if you will, tested, and then “re-installed”, so that they would work properly. This is pretty much how it was, until 1960, when IBM began developing a series of machines that all had the same instructions and I/O design. While this particular venture wasn’t successful due to complications with hardware differences and that lovely habit of software development to take longer than you expect, it put an idea in the air, and signaled the end of an era.</p>
<h3 style="margin:0 auto;"><i><b>2. Enter Multics</b></i></h3>
<img src="/assets/media/multics.jpg" style="height:50%;width:50%;align-items:center;align-content:center;align-self:center; margin: 5px 5px;"/>
<p>Multics (<a href="https://en.wikipedia.org/wiki/Multiplexing">Multiplexed</a> Information and Computing Service), was born circa 1965, as a joint project between Bell Labs, GE and MIT. It was capable of using things like tree structured file systems, user and system documentation, segmented memory addresses, virtual memory, and a supervisor program that managed all of the necessary hardware resources. Towards the end of the 60’s, Bell Labs withdrew from the project, and GE sold it’s computer business to Honeywell, a conglomerate company, which turned Multics into a commercial product, which which did relatively well until 1985, when it was cancelled. (We’re almost there I promise you). </p>
<p>In 1969, something interesting happened, be it fate, fluke or chance, that would forever change the future of operating systems, and computation, for ever. Ken Thompson and Dennis Ritchie wanted to play a game, so, amongst the many other things they were working on at Bell Labs as the leads of a team of engineers, such as desiging the entire C language, they decided to rework the Multics OS into a system that would allow them to play the game as they desired. A colleague of theirs, unknowingly coined the phrase, and subsequent term that would be integral to the software community for decades to come: the Uniplexed Information and Computing Service, now commonly known as Unix.
<i>A fun bit of trivia is that no one is sure where the spelling with an x came from.</i> </p>
<p>By 1973, the Unix (<a href="https://en.wikipedia.org/wiki/Kernel_%28operating_system%29">kernel</a> was written entirely in C, and was an OS like no other, sporting a hierarchical file system, a CLI/shell, and most important, portability
At this point, as the academic community began to flock towards Unix, and modify it for their various needs, at the same time, in different places around the country, perhaps world, even. Versions of the system made their way to computer science departments of various universities, with the most resultful being the University of California (Berkeley), in 1975. They went on to release their own implementation of the Unix system through their distribution arm, Berkeley Software Distribution, which ended up being the basis of a project ran by Darpa, in the late 70's.
With the Unix system becoming popular among computer-philes, scientists and programmers, it became obvious that the sprawling community of Unix users needed a standard upon which they could base further development, to alleviate the difficulties of figuring out which iteration of the system would actually support the software they developed, in a way that would allow them to keep innovating and evolving the kernel as they desired. This lead to a duopoly based on either System V (lead by AT&T/Bell Labs), or BSD (lead by Berkely Software Distribution). We’re almost there, I promise you. Really, I mean it this time.</p>
<h3 style="margin:0 auto;"><i><b>3. Welcome to Gnu (Pronounce the "G").</b></i></h3>
<img src="/assets/media/gnuox.jpg" style="height:50%;width:50%;align-items:center;align-content:center;align-self:center; margin: 5px 5px;"/>
<p class="ttf spacing" style="font-size:22px;line-height:26px;margin:0 auto;">Just look at that smug Gnu grin.</p>
<p style="margin-top:10px;">So, as the seventies wound up, we find ourselves again, at a moment not very much unlike the moment that Ken Thompson and Dennis Ritchie decided they were’ going to develop the Unix kernel, however, the star player this round is an individual by the name of Richard Stallman, and he would change the world of software development forever, just as did those before him. Whereas Unix was developed out of a more technical set of circumstances, the events that lead to the creation of GNU by Stallman, were largely cultural. In short, as software became more popular, companies began to not only withhold source code, in attempts to stymie the success of rival companies, but they began to utilize copyrights and licenses as well, which was throttled the creativity of the programming community. The best part of this is that, the thread that broke the gnu’s back was being denied access to the source code for a printer that was being used <i>at the lab he was working in</i>. Stallman had modified a prior machine to notify users if their requested print job was finished, or if there was a jam and wanted to replicate this for a new device.</p>
<p>Not very long after this event, several ARPANET mailing lists received a message, stating the plan for the development of the GNU operating system, with the following quote:
    <ul>
    <li style="font-size:22px;line-height:26px;margin:0 auto;margin-bottom:10px;width:75%;margin-left:10"> 
    <b>Why I Must Write GNU:</b>
    I consider that the golden rule requires that if I like a program, I must share it with other people who like it. I cannot in good
    conscience sign a nondisclosure agreement or a software license agreement. So that I can continue to use computers without violating my principles, I have decided to put together a sufficient body of free software so thatI will be able to get along without any software that is not free.</li></p>
<p>The GNU (which stands for “Gnu’s Not Unix”), kernel was created with the intention for it to be compatible with Unix programs, and to contain all of the usual utilities found on Unix systems, such as shells, C compilers, spreadsheets, in fact, GNU gave us Emacs, gdb, <i>and</i> gcc. In order to help fund the development of the GNU OS, and future pieces of software like it, Stallman created the Free Software Foundation, published the Free Software Definition through the FSF, thus bringing forth the foundation for the vibrant and productive OSS development community that all programmers benefit from today.
<i>It should be noted that Stallman didn’t necessary mean free as in software should cost zero dollars, but rather free as in having the freedom to share software, to access the source code, the freedom to change that code, and then share it some more.</i>
</p>
<p>While GNU gave us many things, it unfortunately fell victim to Xanadu syndrome, or Sagrada Família disorder, in that the hurd kernel, which drives the GNU OS has never quite reached completion to a degree that would allow it to be a standalone option for programmers, or users. This is likely due to the fact that the OS uses a particular type of architecture, known as server-client, as opposed to the monolithic architecture used by Unix and like systems.
Now, lets fast forward three or four years, and travel across the pond to the Netherlands, where we meet our next installment in the history of *nix:
<h3 style="width:100%;display:flex;flex-direction:row;justify-content:center;"><i><b>4. Enter Minix/Linux.</b></i></h3>
</p>
<img src="/assets/media/Minix318.jpg" style="height:50%;width:50%;display:block; margin-left: auto; margin-right: auto;"/>
<p style="margin-top:10px;">MINIX is a portmanteau of mini and Unix, developed originally by Andrew S. Tanenbaum in 1987, to express some of the concepts in Operating Systems: Design and Implemenetation, a textbook he wrote while teaching Computer Science at Vrije Universiteit. The textbook contained the MINIX source code in the back ( roughly ~12k lines of C), and it was also available on a set of floppy disks. This lead to the creation of a Usenet group, comprised of a very large number of developers/subscribers, a number of which were students, dedicated on expanding and developing the software system. One of these students, was Linus Torvalds.</p>
<p>Torvalds was attending college, studying computer science in the late 80's/early 90's, when he stumbled upon the book written by Tanenbaum, containing all of the information about the inner workings of the MINIX OS. Similar to Stallman, Torvalds found himself up against the wall of proprietary software and copyright licenses, staring down an exorbitant price for even the cheapest available UNIX system. Faced with the desire to use a UNIX system on an IBM computer, and no way to gain access to one, Linus had only one option: create an operating system himself. Being familiar with the MINIX OS, he used it as a conceptual launch pad for his own OS, a free unix-like operating system for the masses. Thus began the development of the Linux kernel, as a side project.</p>
<p>Originally titled “Freax”, Linus ended up switching to the name “Linux”, due to the fact that a colleague had already set up an FTP (File Transfer Protocol) server under that name. In the face of the hard work soon to be undertaken, for that small moment, a bit of laziness prevailed.
The most pivotal moment, in the history of Linux, is August 25th, 1991, the day that Linus send out a Usenet post to other developers, about a project he was working on, a unix-like system, based on Minix:
    <ul>    
    <li style="font-size:22px;line-height:26px;margin:0 auto;margin-bottom:10px;width:75%;margin-left:10">
   <b>Hello everybody out there using minix:</b>
   I'm doing a (free) operating system (just a hobby, won't be big and
   professional like gnu) for 386(486) AT clones.  This has been brewing
   since April, and is starting to get ready.  I'd like any feedback on
   things people like/dislike in minix, as my OS resembles it somewhat
   (same physical layout of the file-system (due to practical reasons)
   among other things).
   I've currently ported bash(1.08) and gcc(1.40), and things seem to work.
   This implies that I'll get something practical within a few months, and
   I'd like to know what features most people would want.  Any suggestions
   are welcome, but I won't promise I'll implement them :-)
                 Linus (torvalds@kruuna.helsinki.fi)</li>
    </ul>   
                 </p> 
 Over the next few years, over a hundred developers set to work developing the first functional version of the Linux OS, built around the Linux kernel, with the first release taking place a little over a year after the original Usenet post, sometime in 1992. Linux was now, officially an Operating System.
 </div>
 </head>