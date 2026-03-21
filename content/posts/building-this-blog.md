---
title: "Building This Blog: Architecture Decisions"
date: 2026-02-28
draft: false
tags: ["hugo", "infrastructure", "meta"]
description: "Documenting the technical decisions behind this blog — Hugo, self-hosting, Giscus comments, and a minimalist design philosophy."
---

This is the inaugural post. It documents the architecture behind this site and why each decision was made.

## Why Hugo

Hugo generates static HTML. No server-side runtime. No database. The output is a directory of files that any HTTP server can serve. This means:

- **Fast builds** — Hugo builds hundreds of pages in under a second.
- **Zero runtime dependencies** — No Node.js, no PHP, no Ruby in production.
- **Trivial deployment** — Copy files to a server. Done.

## Self-hosting with Caddy

Caddy provides automatic HTTPS via Let's Encrypt, HTTP/2 out of the box, and a configuration file that fits on a napkin. For a static site, it's the simplest production-grade option.

## Comments via Giscus

Instead of managing a comment database or dealing with spam on open forms, comments are powered by GitHub Discussions through [Giscus](https://giscus.app/). Readers authenticate via GitHub. Comments live in a repository you control.

## Design philosophy

- 700px centered content width for comfortable reading
- Serif body text for long-form readability
- Sans-serif headings for visual hierarchy
- Dark mode that respects system preference
- No sidebars, no widgets, no distractions

## Code blocks

Here's an example to verify syntax highlighting:

```go
package main

import "fmt"

func main() {
    messages := []string{"Hello", "from", "the", "blog"}
    for _, msg := range messages {
        fmt.Println(msg)
    }
}
```

## What's next

More posts on systems, infrastructure, and the things I learn building software.
