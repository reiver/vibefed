# vibefed — Fediverse Plugin for LLM coding tools (such as Claude Code)

**vibefed** is a plugin for LLM coding tools to help create Fediverse and Social Web software.

Includes knowedge about ActivityPub and other Fediverse protocol.
Helps you detect, implement, and debug Fediverse federation in your codebase.

## Quick Install

If you just want to install **vibefed** right now, run the following 2 commands from inside the Claude Code terminal application:

```
/plugin marketplace add reiver/vibefed
/plugin install vibefed@vibefed
```

## Examples

You can use **vibefed** by prompting the LLM coding tool about some topic covered by this plugin.
For example:

> What do I need to do to make Fediverse/ActivityPub emoji reactions work in the source-code of this Fediverse software?

Or:

> Does this software implement nodeinfo? And, if it does, is it doing it correctly?

## What Is Included

Here is what is included in **vibefed**:

**Active skills** are invocable as slash commands.
**Background skills** load automatically when Claude detects the topic is relevant — no invocation needed.

### Dual Technical Knowledge + SlashCommands (What is Included)


| Skill              | Type   | Description |
|--------------------|--------|-------------|
| `detect-nodeinfo`  | Active | Detects NodeInfo (`/.well-known/nodeinfo`) implementation in a codebase |
| `detect-webfinger` | Active | Detects WebFinger (`/.well-known/webfinger`) implementation in a codebase |

### Technical Knowledge (What is Included)

| Skill (Background Knowledge)   | Type       | Description |
|--------------------------------|------------|-------------|
| `kb-fediverse-actor-statuses`  | Background | FEP-82f6 Actor statuses, short non-interactable profile text, ActorStatus type, endTime expiration, attachment metadata, Remove vs Delete, status history |
| `kb-fediverse-activity-intents` | Background | FEP-3b86 Activity Intents, WebFinger URL templates for cross-server Follow/Like/Announce/Create, oStatus history, workflow callbacks, security |
| `kb-fediverse-federation-md`   | Background | FEP-67ff FEDERATION.md convention, documenting federation behavior, suggested template, DOAP companion (FEP-c893), 40+ implementations |
| `kb-fediverse-following`       | Background | Follow/Accept/Reject/Undo flow, locked accounts, shared inbox, account migration |
| `kb-fediverse-group-federation` | Background | FEP-1b12 Group actors, audience property, Announce wrapping, moderation, Announce(Activity) vs Announce(Object), FEP-400e comparison |
| `kb-fediverse-hashtags`        | Background | ActivityPub hashtag representation, `@context` patterns, federation quirks |
| `kb-fediverse-http-signatures` | Background | HTTP signature construction, verification, keyId resolution, and 18 interoperability quirks |
| `kb-fediverse-json-ld`         | Background | `@id` vs `id` aliasing, value form variability, `@context` handling, expansion/compaction, defensive parsing, content types |
| `kb-fediverse-liking`          | Background | Like/Undo{Like}, the `likes`/`liked` collections, emoji reactions (EmojiReact vs Misskey), stale counts |
| `kb-fediverse-long-form-text`  | Background | FEP-b2b8 Article type for blog posts/articles, Article vs Note, preview fallback, summary guidance, allowed HTML, interop matrix |
| `kb-fediverse-nodeinfo-extensions` | Background | FEP-6481 (WITHDRAWN) extension discovery via NodeInfo, FEP-9fde successor, capability discovery landscape, custom types debate |
| `kb-fediverse-openwebauth`    | Background | FEP-61cf OpenWebAuth federated SSO, 5-step token handshake, Magic Auth history, authentication vs authorization, cross-server identity |
| `kb-fediverse-portable-objects` | Background | FEP-ef61 server-independent identifiers, ap:// URI scheme with DIDs, gateways, integrity proofs (FEP-8b32), nomadic identity |
| `kb-fediverse-relays`          | Background | Relay subscription handshake, Mastodon vs LitePub protocols, Announce wrapping, relay software, topic-based relays |
| `kb-fediverse-webfinger-discovery` | Background | FEP-2c59 reverse WebFinger discovery, `webfinger` property on actors, domain mismatch, `preferredUsername` limitations, validation rules |

### Software Knowledge (What is Included)

| Skill (Software Knowledge)     | Type       | Description |
|--------------------------------|------------|-------------|
| `kb-friendica`                 | Background | Friendica multi-protocol bridge (ActivityPub + DFRN + Diaspora), DFRN protocol details, addon/plugin system, privacy ACLs, 200K-char posts, hub-and-spoke DB schema, Mastodon API compat, Bluesky/Tumblr/email connectors, Hubzilla lineage |
| `kb-kbin`                      | Background | Kbin/Mbin decentralized content aggregator + microblogging (Reddit+Mastodon hybrid), magazines as Group actors with Announce relay, threads as Page + microblogs as Note dual content model, downvotes do NOT federate, Mbin community fork (C4 governance), Kbin vs Lemmy comparison, Threadiverse ecosystem |
| `kb-lemmy`                     | Background | Lemmy Community as Group actor, Announce relay, Post as Page, Comment as Note, Like/Dislike voting, moderation activities, JSON-LD context, strict parsing, Threadiverse ecosystem |
| `kb-loops`                     | Background | Loops short-form video platform, Note objects with video attachments (not Video type), graph-walking comment validator, For You feed, duets, PeerTube comparison, Pixelfed lineage |
| `kb-misskey`                   | Background | Misskey Japanese-origin microblogging platform, ActivityPub extensions (`_misskey_reaction` emoji reactions, `_misskey_quote` quotes, `isCat`), MFM markup language, Drive file management, Antennas, Deck UI, Note visibility levels, extensive fork ecosystem (Sharkey, Firefish, Iceshrimp), Mastodon comparison |
| `kb-peertube`                  | Background | PeerTube two-tier actor model (Person/Group channels), Video object type, CacheFile redundancy, Dislike activity, live streaming, P2P delivery, FEP-5624 comment approval |
| `kb-piefed`                    | Background | PieFed Python/Flask Threadiverse platform, Feed actor (FEP-1d80), private/anonymous voting via proxy profiles, EmojiReact/ChooseAnswer/PollVote/Event activities, 95% Lemmy-compatible API, trust & safety (3K+ domain blocklist, AI labeling, attitude tracking), cross-post deduplication |
| `kb-pixelfed`                  | Background | Pixelfed ActivityPub implementation, extensions (capabilities, commentsEnabled, Stories, blurhash), Mastodon API compat, federation quirks |


## Installation (Claude Code)

Here are the steps to install **vibefed** into Claude Code:

### Step 1: Add Marketplace

Either run the following from inside a session in the Claude Code terminal application:

```
/plugin marketplace add reiver/vibefed
```

Or alternatively, from your terminal shell run:

```bash
claude plugin marketplace add reiver/vibefed
```

### Step 2: Install The Plugin

Either run the following from inside a session in the Claude Code terminal application:

```
/plugin install vibefed@vibefed
```

Or alternatively, from your terminal shell run:

```bash
claude plugin install vibefed@vibefed
```

## History

The genesis of **vibefed** is this poll:

* https://mastodon.social/@reiver/115945516148259016

## Author

**vibefed** was created by [Charles Iliya Krempeaux](http://reiver.link)
