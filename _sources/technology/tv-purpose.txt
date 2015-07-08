Technology Viewpoint - Implementation choices
#############################################

Modular Software
----------------

The TEP system is built with several building bricks developed as inter-dependent modules integrated together to provide with the complete platform. The WebServer provides with most of the basics functionalities. Such a division ensure the modularity and the flexibility of the whole system.


Long Lifetime Software
----------------------

The Web Server software high-level (as opposed to machine-level) programming language uses the `mono framework <http://www.mono-project.com/>`_, which is a multi-platform open source implementation of Microsoft's .NET framework. Mono is widely compatible with .NET and provides compilers for the C# programming language, the most important of the .NET programming languages, translating it into an intermediate language (defined by .NET). The byte code of this intermediate language is executed by a Virtual Machine. By abstracting the machine-level aspects like memory, processor and operating system, it brings portability to the developed software. Unlike .NET, the mono framework runs not only on Windows, but also on Linux and Mac OS X operating systems.
MVC computational model presents many advantages for maintaining the software in a long lifetime. User interface logic tends to change more frequently than business logic, especially in Web-based applications. For example, new user interfaces may be added, or existing interfaces may be shuffled around.

