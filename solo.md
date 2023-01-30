---
title: "Solo Game Projects"
description: null
---

## Hobby Engine

A C++ engine built nearly from scratch, capable of supporting small-to-medium sized
indie game projects in 2D or 3D. Uses a DirectX 11 based render pipeline along with
other toolkit pieces required to build a game such as physics, networking, data-driven
asset loading, and game object lifetime management.

There have been multiple times where I've considered porting my hobby engine to the
Rust programming language in order to experience firsthand the difficulties and benefits
of moving an existing C++ project to Rust, but I haven't been able to find the time
to follow through yet, unfortunately. The exercise of considering it has helped me
concretize some perspective on engine design, though, and I'm following the development
of [Bevy](https://bevyengine.org/) with great interest.

## Simpleminer

A Minecraft-alike built in the Hobby Engine. Supports infinite generated and
user-manipulable worlds based on a chunk system and a dynamic lighting system.

## FMOD-rs

Bindings to the FMOD audio library for the Rust programming language. Provides
access to the standard FMOD API (officially usable from C, C++, C#, and JS) in
a manner idiomatic to the Rust programming language, utilizing a mixture of
code generation techniques and manually authored API translations.

At the current time, this project is exclusively a personal project, but when I
manage to find some more time to polish up the interface a bit, I plan to release
the bindings under a permissive open-source license. (FMOD itself is of course
still paid software.)

## Unreal Rust Tool

An extention to the Unreal Engine build system (Unreal Header Tool and Unreal
Build Tool) that adds Rust as a supported development language for game modules.
Disclaimer: extremely proof-of-concept, and only functional for basic use cases.

In the current prototype, I have mostly manual bindings allowing the implementation
of a basic `UCLASS` in Rust with the header interface still defined in C++. The
prototype targets Unreal Engine 4, but I have a sketch laid out for full integration
into UHT and UBT in Unreal Engine 5. Progress is slow, however, as doing a lot of
code generation and integration into an underdocumented (publicly, at least) system
requires a significant effort for small pieces of progress, and best practices on
how to integrate Rust into a dynamically loaded system like UE are still evolving.
