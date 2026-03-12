# vibefed — Fediverse Plugin for LLM coding tools (such as Claude Code)

**vibefed** is a plugin for LLM coding tools to help create Fediverse and Social Web software.

Includes knowedge about ActivityPub and other Fediverse protocol.
Helps you detect, implement, and debug Fediverse federation in your codebase.

## What Is Included

| Skill                          | Type       | Description |
|--------------------------------|------------|-------------|
| `detect-webfinger`             | Active     | Detects WebFinger (`/.well-known/webfinger`) implementation in a codebase |
| `detect-nodeinfo`              | Active     | Detects NodeInfo (`/.well-known/nodeinfo`) implementation in a codebase |
| `kb-fediverse-following`       | Background | Follow/Accept/Reject/Undo flow, locked accounts, shared inbox, account migration |
| `kb-fediverse-hashtags`        | Background | ActivityPub hashtag representation, `@context` patterns, federation quirks |
| `kb-fediverse-http-signatures` | Background | HTTP signature construction, verification, keyId resolution, and 18 interoperability quirks |
| `kb-fediverse-liking`          | Background | Like/Undo{Like}, the `likes`/`liked` collections, emoji reactions (EmojiReact vs Misskey), stale counts |

**Active skills** are invocable as slash commands. **Background skills** load automatically when Claude detects the topic is relevant — no invocation needed.

## History

The genesis of **vibefed** is this poll:

* https://mastodon.social/@reiver/115945516148259016

## Installing

To install **vibefed** from the Claude terminal application run:

```
/plugin marketplace add reiver/vibefed
/plugin install vibefed@vibefed
```

## Author

**vibefed** was created by [Charles Iliya Krempeaux](http://reiver.link)
