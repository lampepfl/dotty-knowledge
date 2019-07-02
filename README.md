# Dotty Internals Knowledge Collection
This is a place where Dotty contributors collect the knowledge about Dotty internals, procedures we follow when working with the Dotty code base, and all the other things related to the day-to-day Dotty development.

## Get Started
If you know anything useful at all about Dotty, feel free to log this knowledge by opening an issue in this repository:

[![Log Knowledge](https://img.shields.io/badge/log-knowledge-blueviolet.svg)](https://github.com/lampepfl/dotty-knowledge/issues/new/choose)

In short, no need to make it pretty, particularly human-readable or give it a particular structure. Just dump the knowledge you have and we'll take it from there.

## Motivation
Dotty code base has a lot of secrets about it. Secrets like the built-in debugging capabilities, the flags to be passed to the dotc compiler and many more! These are secrets because they are not documented anywhere (at least at the time of writing of this document – but you get the idea). And it can take you months to accidentally stumble upon them and thus increase your productivity.

This project is designed to tackle the issue of knowledge collection, so that there are less dark corners about the Dotty code base. And thus if a person new to Dotty has a desire to contribute, they will have a comprehensive, up-to-date knowledge base with the information, tips and tricks Dotty veterans use.

A comprehensive, up-to-date internals docs can also be helpful to communicate and organize technical knowledge across the team working on Dotty.

## How it works
### The problem of overhead
This project is all about tackling overhead related to knowledge collection. Normally, documentation is a tedious process, where you need to do at least the following:

1. Put your ideas in words, in a human readable way, ideally so that a completely unfamiliar person can understand.
2. Figure out the place of your piece of knowledge in the current documentation.
3. Submit your knowledge to the documentation. In case of Dotty website docs, involves creating a new markdown file with your information and submitting a PR.

All of these steps create overhead on a person, take time and energy that could otherwise be spent writing code. Because people are busy with other stuff, things often go undocumented.

### The solution
This project removes the above mentioned overhead. Quite simply, it is just an issue queue. Every issue represents a raw intent with respect to the Dotty documentation. The idea is that, although creating a fully-fledged documentation requires effort, noticing your own wants with respect to the docs - such as "oh, it would be nice to document this" or "that piece of docs is outdated" – requires much less effort. In this project's issue queue, every issue is an intent meant to describe what you want to do with the documentation. So far, three basic types of intent exist:

- __Add knowledge:__ you have learnt something while working on the Dotty compiler and you want to preserve this info. Example: you have learnt a command to run ScalaFix with a rule on your local file system against a code base. You are sure that you'll forget that command in a while and you do not want to lose it. Hence you can submit an issue specifying this intent – to preserve the mentioned command – to this issue tracker.
- __Modify documentation:__ you became aware that the knowledge base needs to be modified in some way. Example: you have a feeling that two pieces of docs have overlapping content, however you do not have the time to look deeper. You do not want to lose what you discovered, so you log it in the issue tracker.
- __Report outdated:__ you want to report that a piece of knowledge in the docs is no longer up to date. Example: an API of some Dotty class have changed, but you noticed that the docs are written against the old API. The documentation in question is too large and you do not know what the API changed to. You do not want to go through it and fix it right away, but you do not want to lose the information.

The main catch about the issues you submit is that you do not need to follow any particular structure or meet a particular quality standard. We decouple information collection and information refinement and structurization here.

Once in a while, when the contributors have spare capacity, they will go through the issue tracker and act upon people's intents. An issue is closed once the intent is acted upon – or we determine that no action is needed.
