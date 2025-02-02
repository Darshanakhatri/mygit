
# Detecting video game-specific bad smells in unity project

## Author
ANTONIO BORRELLI, VITTORIA NARDONE, GIUSEPPE DI LUCCA, GERARDO 
CANTORA, MASAIMILIANO DI PENTA

## Track: 
 MSR 2020 Technical Papers

>When: Mon 29 Jun 2020 12:00 - 12:10 at MSR:Zoom - Code Smells
Chair(s): **_Alessandro Garcia_**


[summmary3 link](http://www.ing.unisannio.it/mdipenta/papers/unitysmells.pdf)

https://www.youtube.com/watch?v=kztzixMoUZw

## Introduction and motivation

In this paper we propose unity linter, a static analysis tool that supports unity video game 
development. Such smell types pertain to performance, maintainability and incorrect behavior 
problems. The largest portion of video game market is targeting mobile devices and 
streaming services for increasing the complexity. Unity linter is a tool to detect bad smells 
in video games and pertain to performance maintainability and performance issues. Result 
of our empirical investigation indicates that developers well received performance and 
behavioral and maintain related issues are more controversial.

## Research methodology 

Video game development industry is largest share of software development industry in 
2018 the increasement in videogame development ratio is 10% in one year now a days 
videogame industries are changing their platform from console and computers to mobile 
devices even the video game streaming is a top trend correct time. video game market is a 
kind of niche on stack overflow over 1.2 million tags are about android and only 50ks are 
related to unity this is now clear that in this context developers need a huge support. 
Static code analysis tools SCAT like linter first develop by Johnson for C language to analyze
the problems in code, SCAT general propose is to find bugs in many programming 
languages. Unity linter statically analyzes the code and other artifacts of a unity videogame, 
and can detect 7 types of bad smells such smells covers different quality aspects of 
videogame development, namely performance, maintainability, and correct behavior.
Unity is a framework for developing the 2D and 3D games. This framework is based on 
graphics, the plot of games like objects and area and movements are graphically designed 
with the Unity, Unity allows developers to decorate an object with different kind of various
components.

## Result

Result of the study indicates that overall developers well perceive the smells we defined in 
particular, those related to performance and game behavior while maintenance related smells 
are more controversial. Our manual validation indicates that unity linter achieves for different 
smells types 86%-100% precision and 50%-100% recall. Depending on the type the presence of 
the studied smells in the analyzed projects various between 39% and 97% of the analyzed 
projects.

