# "Inclusive Language" - A Statement

## Foreword

I'll preface this statement with refreshing words of reassurance - **this isn't
an attack** on people seeking to replace terminology with more inclusive
variants within the computer science community. In lieu, I wish to make
"inclusive language" genuinely inclusive.

**Software engineering should be accessible to all, no matter the abstract
factors of their background.**

## What's the problem?

Numerous organizations recently opted to replace potentially insensitive
terminology with more "inclusive" variants, including the decision to remove
"whitelist" / "blacklist" and similar terms \- exempli gratia, [Google's v8
"Respectful Code" guidelines][v8-guidelines].

[v8-guidelines]: https://github.com/v8/v8.dev/blob/e7a89dea53af0e6dbf835da73d3736623d449e48/src/docs/respectful-code.md

## Surely there's nothing wrong with that?

Despite the various arguments for and against those terms and their freedom of
historical racial charge, I won't discuss them here because they solve nothing.
Individuals will continue to associate these terms with a racial bias for the
duration of their use, so resistance is pointless. We should aim to fix it \-
and with that, let's examine the problem.

**Replacing the terms is fine, but their designated replacements are not.**

Common replacements for those terms include "blocklist" / "denylist" for
"blacklist", "allowlist" or "grantlist" for "whitelist", et cetera. These are
perfectly viable replacements on the surface; however, that notion fails to
consider that English isn't the only language spoken on our Earth.

## Lost in Translation

Let's take Spanish for example (there are other languages in which this
applies, but a talented developer and respectable acquaintance, [Kyra], helped
by providing examples from his native language).


Typically, to inform someone they're "whitelisted" or "blacklisted" in Spanish,
you'd use the following:

```
"You're in the whitelist" -> "Estás en la lista de usuarios permitidos" ("You're in the permitted user list")
"You're in the blacklist" -> "Estás en la lista de usuarios no permitidos" ("You're in the prohibited user list")
```

Note that "lista blanca" ("whitelist") and "lista negra" ("blacklist") are
considered higher-level vocabulary and aren't understandable to a majority of
Spanish speakers. By that logic, using "whitelist" and "blacklist" themselves
is also harmful, so this problem existed before. We must use our opportunity to
change the vocabulary to fix these issues, rather than making them worse.

Observant readers may notice a lack of direct or well-known translation for the
proposed alternatives. Alternative phrases for "whitelist" and "blacklist"
exist in English, and neologisms are less accessible, if not at all
incomprehensible, to non-native speakers. Therefore, they arguably do more harm
than good.

If we're to fix this properly, we need a better, more permanent solution. Since
I'm against speaking about issues without proposing solutions, here are my
suggested alternatives:

| <u>**Vocabulary**</u> |       <u>**Alternative**</u>       |
|:---------------------:|:----------------------------------:|
|      "whitelist"      |   "list of allowed / permitted x"  |
|      "blacklist"      |   "list of banned / prohibited x"  |
|     "whitelisted"     |   "authorized", "permitted", etc.  |
|     "blacklisted"     | "unauthorized", "prohibited", etc. |

[Kyra]: https://github.com/kyranet

## Character Counting

The aforementioned proposed alternatives for "whitelist" and "blacklist" aren't
perfect \- they're comparatively verbose. Hence, this isn't a concrete solution
\- I'm asking those engaged in facing this problem to consider accessibility to
wider audiences when making these changes (not solely this particular example).
After all, inclusion is our goal, not exclusion.

If you wish to co-sign this statement or make better suggestions, I encourage
you to [create a pull request][pr] and thank you in advance for your help.

Furthermore, if you wish to support this movement by making a pull request to
an organization you know that has fallen victim to this inconsiderate paradigm,
[here] is an example of one made on behalf of Kludge Cyber Systems to Google.

[pr]: https://github.com/kludge-cs/transparency/pulls
[here]: https://github.com/v8/v8.dev/pull/537
