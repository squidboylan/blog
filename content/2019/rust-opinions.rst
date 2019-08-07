My thoughts on Rust: hate, love, and cautious optimism
======================================================

:Title: My Thoughts on Rust: Hate, Love, and Cautious Optimism
:Date: 2019-08-6 18:00
:Modified: 2019-08-6 18:00
:Category: Programming
:Tags: Rust, Languages, Programming
:Slug: my-thoughts-on-rust
:Authors: Caleb Boylan

I've been having mixed feelings about Rust as of lately so I decided I would
write about it to capture how my opinions of the language have changed over
time.

My journey with Rust started a few years ago when I was about half way through
my CS undergrad. A friend had mentioned he was playing with this somewhat new
language that made all these great guarantees about safety and has a great
community backing it up. I didn't quite understand
what that meant, but I went ahead and downloaded the compiler
(which felt like a painful process as I had to go further than the package
manager to do so), gave it a couple hours of my time and decided it wasnt for
me. The borrow checker was too hard to please and after having trouble with
getting the right toolchain I decided the language wasn't worth my time.

A year or two later I had taken my Operating Systems class and was inspired to
do systems development. One of the other systems classes offered at my
university is a Rust class, however I was unable to get into the class the
subsequent term so I decided to pick up the text book (`Programming Rust: Fast,
Safe Systems Development <http://shop.oreilly.com/product/0636920040385.do>`_)
and teach myself the language. With my new found inspiration (and the help of
Blandy and Orendorff). I had the
motivation to overcome the common Rust hurdles and quickly fell in love with
the language. I wrote a `GameBoy emulator
<https://github.com/squidboylan/corroboy>`_ and began to think Rust was the
future of systems development. Once you get over the borrow checker it felt like I
was able to make software with far more ease than any systems language I had
worked in before (C/C++) and with the memory guarantees of a GC'd language.
Rust also gives me the confidence that once it compiles I can be fairly
confident the code works as intended. This confidence isn't on the same level
as a language like Haskell, but is more confidence than I have when writing C
or other unsafe languages.

While I do still think highly of Rust, the honeymoon phase has worn off and I
have been able to analyze the language more objectively. Rust
does have problems, and the community is fairly good at acknowledging them.
Most Rustaceans would agree that Rust...

 - is slow to compile
 - is lacking when it comes to building GUIs
 - is lacking when it comes to async
 - is still pretty immature when it comes to 3rd party libraries
 - is still somewhat immature in general

Some of these problems are more important than others. The slow compilation is
really not the end of the world, while it's not ideal, it doesn't really
prevent new users from picking up the language or make rust unusable in certain
environments (maybe it does and I'm not aware of it). There are also efforts
to speed up the compiler. However, when it comes to
building fast, resilient software -- which is what Rust aims to do -- it is
extremely painful to leave a project for a couple months and come back only to
have the compiler refuse to build your project. This happened to me as recently
as last year, and while it's not common, it's rough that it happens at all.

The lack of async support (or friction of
building async apps) makes it unappealing for many projects. From what I
understand this is getting better, however I find the whole "async story" hard
to follow and quite honestly am not sure what the state of the async support is.

The fact that things like how async works in the language are still changing
means it can be very hard to find up to date docs on what the correct way to do
things is. This can add lots of friction when learning the language.

With all these issues I still do think Rust **could be** the future of systems
development. It's hard to argue with the performance and safety benefits of
using Rust, but it still has a ways to go before it could replace something
like C or C++ outright, and to be fair many of these problems are just growing
pains that every language experiences. I look forward to Rust in 5 years or so (hopefully less)
when the language has slowed down and essential 3rd party libraries are mature and
stable.
