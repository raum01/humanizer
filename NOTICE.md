# Attribution

This repository is a fork of [blader/humanizer](https://github.com/blader/humanizer)
by [blader](https://github.com/blader), used under the MIT License. The original
LICENSE is preserved unchanged.

The 35 patterns, their examples and the false-positive list are the original
author's work, derived in turn from
[Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
maintained by WikiProject AI Cleanup.

## What this fork changes

Everything below was found by running the skill's own rules over its own text and
by an adversarial review from an independent model (GLM-5.2), then verified
against the source before being acted on.

1. **Language scope.** The original never states which language it applies to,
   while seven of its rules act on English mechanics. Two of those damage other
   languages rather than merely being inert: §14 deletes the Russian predicate
   dash (*Москва — столица России*), which is required punctuation and not a
   flourish, and §19 normalized «ёлочки» toward ASCII quotes, which is the
   typewriter register in Russian. Both are now scoped, and §8 and §13 carry
   notes about misfiring by analogy.

2. **§14 no longer removes dashes that carry meaning.** Numeric ranges
   (`1990–2005`, `10–20 ms`), grammar-required dashes, and dashes inside
   quotations and proper names are kept. The rule targets the decorative prose
   dash it was written for.

3. **§2's example no longer contradicts the skill.** Its "after" text dropped a
   follower count and two of four named outlets, while the rewrite process
   defines a lost claim as an error. The example now keeps every fact and cuts
   only the padding, which is what the rule is actually about.

4. **Claim preservation is checked rather than asserted.** It was a question the
   model asked itself after the fact, which reliably answers "no". It is now a
   comparison of two lists, source against rewrite. This matters most in Embedded
   and File mode, where nobody ever sees the intermediate output.

No pattern was removed, renamed or renumbered. Upstream fixes should still apply.
