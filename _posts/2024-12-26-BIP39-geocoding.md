---
layout: post
title:  "Geocoding with BIP39"
description: "Building a simple geocoding algorithm : your location is encoded in 4 words"
date: 2025-08-08
author: 
-  Moreau
published: true  
---
While reading about [What3Words](https://what3words.com) recently, I was struck by the clever idea of encoding GPS coordinates into three memorable words. This immediately reminded me of BIP39 - the standard that encodes cryptographic keys into mnemonic 12 or 24 words. The concept of making complex data human-readable through simple words is powerful and can be applied to location.

Traditional postal address systems attempt to solve this problem but have significant flaws - they require shared understanding between the physical location and the address notation, often failing in areas without established addressing infrastructure. Moreover, postal addresses don't provide the precision or universal coverage that GPS coordinates offer.

Naturally curious about the implementation, I went looking for What3Words' algorithm, expecting to find clear documentation and open implementations. What I discovered instead was that What3Words operates as a complete black box. You send GPS coordinates to their service, and it returns three words. No algorithm transparency, no open implementation. Yes, it's 2025 and some people think this can be a good business model...

## The Closed Box Problem

Digging deeper, I found that What3Words has actively pursued lawsuits and takedowns against open-source alternatives. The [OpenStreetMap Wiki page on What3Words](https://wiki.openstreetmap.org/wiki/What3words) documents extensive criticism of their closed system, including patent enforcement, DMCA takedowns, and legal threats against researchers. For a company built on such a fundamentally simple concept - mapping coordinates to words - this aggressive protection of what should be public knowledge seemed counterproductive.

Then what would it actually take to build something similar? Could AI help me prototype this quickly?

## Building an Open Alternative: A Two-AI Workflow

I decided to test how quickly I could build a geocoding system using AI. My approach involved a two-step process: cracking the spec, building the prototype.

### Step 1: Algorithm Design with ChatGPT

I started with ChatGPT to design the core algorithm. Here's the prompt I used:

```
Create a simple geocoding algorithm that converts GPS coordinates (latitude, longitude) 
into 4 memorable words using the BIP39 word list. The algorithm should:
1. Take lat/lng coordinates as input
2. Convert them into a deterministic hash
3. Map the hash to 4 words from the BIP39 word list
4. Be reversible (4 words back to approximate coordinates)
5. Provide reasonable geographic precision
```

ChatGPT helped me refine the requirements and specifications. We iterated on the algorithm design, discussing edge cases, precision trade-offs, and implementation approaches. This conversation became the foundation for the actual implementation.

### Step 2: Implementation with Cursor

Once I had a solid algorithm design, I switched to Cursor for implementation. Here's where the workflow got interesting: I provided the entire ChatGPT conversation as context to Cursor, and it was able to understand the full design discussion and implement the solution based on that context.

This handoff between AI tools was seamless - Cursor picked up exactly where ChatGPT left off, translating the algorithm design into working code.

## The Results Were Staggering

This two-AI workflow demonstrated the power of specialized AI tools working together. Within a single session, I had:

1. **A refined algorithm specification** through ChatGPT's conversational design process
2. **Clean, working code** implemented by Cursor based on the design discussion
3. **Two functional web applications** demonstrating the concept
4. **Adjustable precision levels** and error handling

The speed was remarkable, but more importantly, the quality was high because each AI tool played to its strengths - ChatGPT for ideation and refinement, Cursor for implementation.

## Technical Implementation

The algorithm works by:
- Converting lat/lng to a normalized grid system
- Generating a deterministic hash from the grid coordinates
- Mapping hash segments to BIP39 words (2048 word vocabulary)
- Providing configurable precision levels

Design inspired by: [ChatGPT Canvas discussion](https://chatgpt.com/canvas/shared/689650f10ac88191a6837e29632502dc).


Unlike What3Words' opaque system, this approach is completely transparent and could be implemented by anyone.

You can find the complete implementation and demo at: [https://github.com/nmoreau/BIP39Geocoding](https://github.com/nmoreau/BIP39Geocoding)

## Lessons

The key lesson from this experiment isn't just about speed - it's about communication. Successfully working with AI agents requires understanding when to be broad versus when to be surgical in your instructions.

**When to be broad**: Initial concept exploration and brainstorming work well with high-level prompts. "Build a geocoding system" was sufficient to start the conversation with ChatGPT.

**When to be specific**: Implementation details require the same precision you'd use with a human developer. The numbered requirements in my prompt weren't optional - they were essential for getting a working solution.


## What does this prove (at least to me)

This experiment highlights three important trends:

**AI-Powered Prototyping**: The barrier to building functional prototypes has collapsed. Complex ideas can be tested and validated in minutes, not months.

**The Communication Skill Premium**: Success with AI tools depends heavily on your ability to articulate requirements clearly. This is becoming as important as traditional coding skills.

**The Case for Open Standards**: When fundamental utilities like location encoding are kept proprietary, innovation suffers. Open implementations allow for community improvement, standardization, and broader adoption.

## Conclusion

I (or anyone) can build a working alternative to a company's core simple product. This isn't to diminish What3Words' business achievement, but to highlight how AI democratizes building and how open approaches can rapidly advance innovation. In this particular case, an open standard is a much better alternative to a closed source, walled garden alternative.

Additionally, can we agree on a standard for this?


*You can find the complete implementation and try the demo at [https://github.com/nmoreau/BIP39Geocoding](https://github.com/nmoreau/BIP39Geocoding) - this is a very naive implementation*
