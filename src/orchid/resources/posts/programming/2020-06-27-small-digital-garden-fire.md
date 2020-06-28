---
    title: "Putting Out A (smol) Digital Garden Fire."
    tags:
        - programming
        - bugs
---

<div class="article-container" style="line-height:23px;">
    <h1 class="spacing">
        This is a story all about how JDK got flip turned upside-down..
    </h1>
    <h2>
        TL;DR:
    </h2>
    <blockquote class="spacing blockquote">The version of Gradle and the version of JDK I was running weren't compatible, because I'd updated and switched to a newer one, in order to run Clojure, because I'd deleted the old one while cleaning up disk space. I took a few strolls around Google, and honestly nope'd, because I was not prepared to context switch into config spelunking. </blockquote>
    <p>
        So, June 11th, I woke up with the urge to do some digital gardening, add some notes, links, thoughts, etc, and being ADHD brained, when I <i>wake up</i> with something like this on my mind, it's usually a opportunity to knock something out right away, that would otherwise take several rounds of coffee, Twitter, YouTube, music playlists and responding to texts.
        So, I opened up my laptop, and ran the command to build and serve a local version of my blog and got met with: 
        <blockquote class="spacing blockquote" style="font-size: 20px;">
            Could not initialize class org.codehaus.groovy.runtime.InvokerHelper
        </blockquote>
    <p>The static site generator I use is written in Java (at least partially), and uses Gradle as a build tool, and either Gradle, or the SSG itself (though I believe Gradle), requires Groovy (which is Java <i>compatible</i>), and thus must initialize the runtime in order for Groovy code to be executed.
    Further, it seemed that specifically, the version of Java I was running, was a key player in the in the reason Gradle, could not find the necessary file to initialize a Groovy runtime- because that version of Java was incompatible with Gradle, which meant Gradle couldn't fully run, and thus never initialized the required class. Whew. </p>
    <p> "But wait a minute.." you ask, "If you couldn't run the build tool, then how was your blog ever running?" </p>
    <p> I'm glad you asked. A few days prior to June 11th, I was working on a 
        <a href="https://github.com/LorenzoEvans/kurogane_os"> 
            Rust Project 
        </a>, guided by <a href="https://os.phil-opp.com">Phil Opperman</a>
        when I got a disk space error from the compiler, saying there wasn't enough room to store the binary executable I was building. 
         Needless to say, this notification about the status of my hard drive was news to me, and so I set about fixing it. I opened up Daisy Disk, cleaned out some caches, old apps, files/directories, and at some point, <b>I deleted the entirety of JDK 7.</b></p>
    <p> This fact, went unknown to me, until a few days after that, where I decided to tweak my portfolio a bit, which is written in Clojurescript, and was notified via Leiningen, that there wasn't a Java JDK on my machine, which I found odd, but the terminal output provided a command to run, which would grab the latest version of Java and put it where it was supposed to be, so I figured, why not? A little while later, I had JDK 14, my portfolio changes were made, and I thought nothing of it.
    </p>
    <p> Which brings us back to the present day, where I run the command, and I mean, post breakfast, a good espresso, sat right in front of my computer, ran my command, and bupkis. The version of Gradle and the version of the JDK I was running weren't compatible, because I'd updated or switched to a newer one, in order to run ClojureScript, because I'd deleted the old one while cleaning up disk space. I took a few strolls around Google, and honestly nope'd, because I was not prepared to context switch into config spelunking.</p>
    <p>
    After a few days, I returned to my computer and wiped every version of Gradle/JDK and reinstalled the new ones, as directed by a Stack Overflow or Github Issue, and ran my build command, and still got  the error about the Groovy package that can't be found. 
    So, I switched back to the SO/GH tabs, following the conversation after the solution I'd tried, and someone pointed out that Gradle might still be pulling down an old version of Gradle even if the new one is installed on your machine.
    </p>
    <p>
        So, after a few result-less cache and usr/local/bin hunts, I remembered that there were a few Gradle files lying around my project folder, and decided to check them one by one, and lo and behold, one of them was a wrapper config file that was pulling in Gradle 5.6, as opposed to 6.3. I swapped out the old link for the new one, ran my command, and this time !bupkis. 
        It took a while for the new binary to download and install and rebuild the project, but boom, my static site was running in localhost.
    </p>
    <h3>
        Didn't get any digital gardening done, but I did put out a small garden fire.
    </h3>
    <blockquote class="spacing blockquote"> Moral of the story? Make sure you know what you're deleting, before you delete it, and make sure the version of something your machine is depending on/running isn't a cached version. 
    </blockquote>

</div>