The Red Spider Project
----------------------

[https://github.com/the-xkcd-community/the-red-spider-project]


In this file:

 -  __Why__
 -  __Who__
 -  __How__
 -  __When__
 -  __What__
 -  __Howto's__
 -  __Credits__


### Why ###

Because we like to combine our love for the xkcd comic with our love for coding, and we want to share the experience.


### Who ###

Currently, "we" are all members of the [xkcd forums](http://forums.xkcd.com). However, anyone is welcome to join in.


### How ###

By keeping an ongoing project to which people can add programs at will. By "program", we mean *any* program. It may be any size and it may be written in any programming language, though preferably portable. Most of the programs in our project will probably be amusing, interesting, touching or a combination of those, either because of the source code, because of the output, or both. Likely, most programs will also be small. Anything is welcome except malware.

We put some emphasis on command line programs. The programs may be interconnected with basic plumbing. We'll put some guidelines and infrastructure in place to keep things smooth, as we see the need. Other than that, it's basically liberty above all things!


### When ###

We only just started out, really. (Perhaps this section will contain more interesting historical information in the future.)


### What ###

__License__: we have a liberal license which might strongly remind you of the MIT license (that's not a coincidence). See License.txt for more information.

__Platform support__: for the time being we'll just try to make sure that our stuff runs on the most popular platforms.

__Testing__: we use the issue tracker from GitHub to ask each other a favour. See Platforms.md for more information.

__Branching__: `master` is our sacred branch: it's supposed to contain only reasonably well-behaved programs (say, stable, portable and easy to quit). Nonetheless you're encouraged to merge often into `master`. Do whatever you want in the other branches, but please do observe some common rules of sensibility. For example, don't merge everything into everything.

__Building__: currently there is no build system yet, but we're looking for something portable. Apart from compiling things, it should also just copy interpreted scripts straight to the binary directory (and strip off their file extensions on Unixy systems). Perhaps CMake.

__Directory layout__: we chose `src`, `include`, `doc`, `test`, `build`, `lib`, `bin`, `config` and `work` (if the names don't tell you what they're meant for, don't hesitate to ask). Programs will be pooled enjoyably together unless a single program consists of many files within the same directory (for some subjective value of "many"), in which case we'll give it a dedicated subdirectory.

__Programs__: so far concrete work has been done on `rsshell`, which is supposed to launch a convenient environment for other Red Spider programs, as well as on an xkcd comic fetcher, an xkcd comic regex searcher, an adventure shell and an adventure web browser. More ideas are waiting to be implemented.

__Communication__: we have our little [thread at the xkcd forums](http://forums.xkcd.com/viewtopic.php?f=11&t=81969) for updates, discussion and archaeology, and there's the [issue tracker](https://github.com/the-xkcd-community/the-red-spider-project/issues). Some of the many other options are to comment on commits or to write something on the wiki.


### Howto's ###

Here's the place to find, submit or edit guidelines, rules of thumb, suggested procedures, and so on and so forth.


#### Obtaining the project ####

Easy. Either download the source tree as a zip file from the GitHub project page, or install Git (if you don't have it yet) and run the following command in the directory of your choice:

    git clone git://github.com/the-xkcd-community/the-red-spider-project.git

Alternatively, if you plan to contribute to the project you may create a GitHub account (if you don't have one yet), fork the project and clone your fork to your computer instead.


#### Installing the software ####

There's nothing to be installed yet.


#### Running the software ####

For now, you'll probably just `cd` your way to the `src` directory and execute something like the following, assuming that you want to run `programX` (you can leave out the `./` parts in Windows):

    ./rscall.py ./programX

You'll at least need to have Python installed. If you want to run the (unfinished) `advbrowser` you'll also need PHP. Things will almost certainly change so we'll keep this updated.


#### Creating something of your own ####

Pull in the latest changes to `master`, fork a new branch and hack away. Take your time, we don't do deadlines. :-)

In source code files, please add something like the following in a comment at the top:

    Copyright YYYY __authors_of_major_contributions__
    Licensed under the Red Spider Project License.
    See the License.txt that shipped with your copy of this software for details.

    Acknowledgements: X provided idea A, Y provided idea B.
    Minor contributions were made by Z/by several authors;
    please refer to the Authors.txt that shipped with your copy of this software.

Where `YYYY` starts off as the current year and `__authors_of_major_contributions__` starts off as you, by definition. More years and authors may be added later. The lines with acknowledgements are optional, of course.


#### Integrating your stuff with the rest of the project ####

Finally, here's the really exciting stuff. You'll need to do some or all of the following:

 -  Push your branch to your public fork of the project.
 -  If you edited any Markdown files, check that they render correctly on GitHub.
 -  Ask your fellow project participants for their opinions, if relevant.
 -  Submit a test request to the issue tracker, for the platforms that you couldn't test by yourself. See what happens.
 -  Once your branch works on all platforms, pull in the latest changes to `master` and merge your own branch into it. Push that to your public fork and request that it be pulled into the main repository.
 -  Somebody will probably grant your request.

Once your branch has been fully merged into the master branch, others can start using your work. Of course, nothing stops you from forking another branch to add more features in the meanwhile!

**Note**: merging other unfinished branches into your own is *not* "integrating your stuff with the rest of the project". In fact, it makes it harder. Read the second page of the xkcd forums thread if you need clarification.


#### Editing somebody else's stuff ####

First of all, please either make sure that the original author isn't working on it, or that they like to cooperate with you.

If they're not working on it: fork a new branch, edit, have it tested, have it pulled. Business as usual.

If they want to cooperate with you: add their public fork as a remote, have them add your public fork too, discuss, and push/pull your changes back and forth. Other than that, business as usual.

Depending on the nature of your contributions, you should probably either add your name to the copyright notices of the files you edited or include it in the Authors.txt. For program source files, a guiding question could be the following: "Did I contribute to the program logic?"


### Credits ###

Julian coined the idea, qubital set up the GitHub repository and Neil wrote most of the initial infrastructure code. Please also refer to the copyright notices in the source files and to the Authors.txt, which lists all the authors who decided not to add their name to some file they edited.

Please add your name to the Authors.txt if it isn't in there while it should.
