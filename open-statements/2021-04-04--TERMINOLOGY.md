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
an organization that has fallen victim to this inconsiderate paradigm, [here]
is an example of one made on behalf of Kludge Cyber Systems to Google.

[pr]: https://github.com/kludge-cs/transparency/pulls
[here]: https://github.com/v8/v8.dev/pull/537

## Appendix (2021-04-15)

### Inclusion and Exclusion - Familiar Directives

Following a discussion with members of the [Inclusive Naming Initiative], it's
evident that "exclusion list" and "inclusion list" are currently the best
suggestions for a potential replacement. [@edwarnicke] posed the following
example:

```yaml
include: [A, B, C]
exclude: [D, E, F]
```

The example above is commonplace in software configuration (see: TSC, Google
Analytics, et cetera - most software involving filtering or file handling will
use include and exclude directives), so it follows "exclusion list" and
"inclusion list" (shorthand for "list of excluded items" and "list of included
items" respectively) introduce consistency.

These solutions come with cons \- they don't work universally. Hence, I'm not
advocating for a clean-cut X to Y substitution as that isn't the movement's
goal. Instead, I encourage readers to evaluate the terminology in use and decide
the best replacement for their usage themselves, taking translation and
accessibility into account.

[Inclusive Naming Initiative]: https://github.com/inclusivenaming
[@edwarnicke]: https://github.com/edwarnicke

###  Once Lost, Now Found

When I posed the scenario to [Kyra] once again with the new terminology, I was
glad to learn that both "inclusion list" and "exclusion list" have
understandable translations in Spanish.

```
"Inclusion list" -> Listado de inclusión (direct translation)
"Exclusion list" -> Listado de exclusión (direct translation)
"You're in the inclusion list" -> Estás en la lista de inclusión
"You're in the exclusion list" -> Estás en la lista de exclusión
```

Related translations (exempli gratia, for "You're in the excluded users list")
can be unnatural in both languages \- despite this, translators will choose
a synonym in the target language to flow better contextually while retaining the
implications (for instance, "incluidos" ["included"] -> "permitidos"
["permitted"]). Regardless, they're easily comprehensible and require no further
searching or elaboration.

### In Conclusion

To summarize, "inclusion list" and "exclusion list" carry the following
benefits:
- They are linguistically valid, as opposed to "denylist", "allowlist", et
  cetera, which are not proper English constructs.
- They're directly translatable, and accessible with no subtle nuance or
  required inference skills.
- They line up well with the field of software engineering.

Alongside this, for situations in which it isn't necessary to specify a list,
it's clearer and laconic to specify the entity class itself. For example,
"banned users" is fine linguistically, translatable, and requires less
keystrokes than "blacklisted users" or "banned user list". This works well in
computer science for object oriented programming with `users.banned` being
shorter than `users.blacklisted`, or for data oriented programming, simply
`bannedUsers` being shorter than `blacklistedUsers` or `bannedUserList`.

### A Framework for Analysis

The following framework for linguistic evaluation is derived from the
aforementioned points for measuring the effectiveness of replacement
terminology:

1. Is it a valid linguistic construct? Can it be translated?
  - Words such as "blacklist" and "whitelist" are only translatable due to
  their widespread usage. This is important to consider when producing
  alternatives. Alternatives should follow the rules of their origin language
  (ruling out "grantlist", "denylist", et cetera) so they can be parsed easily
  and so they do not appear unfamiliar to those with a lesser proficiency or
  eye for nuance.
  - For instance, applied to "inclusion list", this check passes because
  "inclusion list" is grammatically valid in English and can be translated with
  consistent meaning.
  - If your answer is no, the terminology is unsuitable.
2. Is it rooted in nuance and inference? Is it shrouded in ambiguity?
  - Words such as "blacklist" and "whitelist" create accessibility barriers to
  those of foreign linguistic backgrounds (and sometimes even require
  confirmation for native speakers) due to their ambiguity. The two words,
  without context, appear to be describing the color of a list \- when
  producing alternatives, clarity is important.
  - For instance, applied to "inclusion list", this check passes because
  "inclusion list" has no ambiguous meaning and is focused on clarity.
  - If your answer is yes, the terminology is unsuitable.
3. Is it potentially harmful?
  - Some terminology is harmful because it potentially creates undesirable
  contextual reminders for readers \- this can be observed in "whitelist" and
  "blacklist" due to their reflection of a positive-negative matrix based on an
  abstract feature. Consider this delicately when proposing alternatives.
  Picking terminology with the desired definition, but no unintended undertones
  for your audience, is a necessary skill.
  - For instance, applied to "inclusion list", this check passes because
  "inclusion list" has no abstract negativity or historical context amongst
  audiences.
  - If your answer is yes, the terminology is unsuitable.
4. Is it concise?
  - Balancing between clarity and brevity is a careful craft; challenges arise
  in selecting phrases to convey the desired implications succinctly.
  - For instance, applied to "inclusion list", this check passes because
  "inclusion list" is more concise and in some forms shorter than its
  alternatives.
  - If your answer is no, the terminology may still be valid, but consider
  carefully whether its verbosity or lack of clarity will prevent it from
  becoming a widespread solution.

If the terminology passes all of those tests, it may be considered viable for
general usage or replacement of archaic language.

### Final Statement

I'm obliged to remind you these aren't concrete solutions, and if you conceive
of better ideas I implore you to discuss them with me. At the moment, they're
the computer science community's best substitutions.
