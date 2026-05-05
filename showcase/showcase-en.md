---
title: Lightmind Theme Showcase
author: SunMoonTrain
date: 2026-05-06
tags: [theme, markdown, demo]
---

# Lightmind Theme Showcase

> A Typora theme with mountain forest greens, LXGW WenKai for body text, and JetBrains Mono for code.

Inspired by the warm space at the edge of a forest at sunset — accent color drawn from distant mountain greens, cream paper holding the text, code blocks sinking into a deep navy. This document systematically demonstrates how the theme handles every Markdown element. It works as a functional check and a design sample.

## Heading Hierarchy

# H1: mountain forest green
## H2: thin deep-green line
### H3: left-side color bar accent
#### H4
##### H5
###### H6

Heading levels should feel clearly differentiated, but not overwhelming. H1 has a double-line, H2 a single line, H3 a green bar on the left, H4–H6 fade gracefully.

## Paragraph & Inline Formatting

This is a regular paragraph. **This is bold (deep forest green)**, *this is italic*, ***this is bold-italic***, ~~this is strikethrough~~, <u>this is underline</u>.

Inline code: `const greeting = "Hello, world"`, inline math: $E = mc^2$, inline keys: <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>.

==This is highlighted text==, mixable with *==italic highlight==*. H<sub>2</sub>O is the chemical formula for water, E = mc<sup>2</sup> is the mass-energy equivalence. <abbr title="HyperText Markup Language">HTML</abbr> is HyperText Markup Language.

[This is a link](https://typora.io), `code` inside a link, email <noreply@example.com>.

## Blockquotes & Alerts

> A regular blockquote. 4px green left bar, misty meadow background, rounded card.
>
> > Nested quote, slightly softer tone.
>
> Quotes can also contain **bold**, *italic*, and `code`.

> [!NOTE]
> Blue tone. For supplementary information or friendly reminders.

> [!TIP]
> Theme green. For practical advice or best practices.

> [!IMPORTANT]
> Purple tone. For critical information not to be ignored.

> [!WARNING]
> Warm orange. Pay attention — this may affect outcomes.

> [!CAUTION]
> Brick red. Dangerous operations or destructive changes.

## Lists

### Unordered List

- First item
- Second item
  - Nested: hollow marker
  - Nested two
    - Three levels deep
- Third item

### Ordered List

1. Prepare ingredients
2. Heat the wok
   1. Pour oil
   2. Wait until 70% hot
3. Stir-fry

### Task List

- [x] Draft theme outline
- [x] Implement color tokens
- [x] Finalize syntax highlighting
- [ ] Cross-platform testing
- [ ] Publish to theme repo

## Tables

### Basic Table

| OS         | Global % | China % |
| ---------- | -------- | ------- |
| Windows    | 76.56    | 87.55   |
| macOS      | 17.10    | 5.44    |
| Linux      | 1.93     | 0.75    |
| Chrome OS  | 1.72     | 0.01    |
| Other      | 2.69     | 6.25    |

### Alignment

| Left   | Center | Right |
| :----- | :----: | ----: |
| Apple  | apple  |   1.0 |
| Banana | banana |   2.5 |
| Cherry | cherry |  18.7 |

### Cells with Complex Content

| Name | Description | Status |
| ---- | ---- | ---- |
| **Bold name** | Contains `inline code` and *italic* | ✅ OK |
| Long name example | A longer description to see how wrapping behaves | ⚠️ Warning |
| Third row | A [linked](https://example.com) cell | ❌ Failed |

## Code

### Inline Code

Run `npm install` then `npm run dev`, and visit `http://localhost:3000`.

### Code Blocks (Multi-language)

The syntax highlighting palette is inspired by the One Dark theme.

```rust
// Rust
fn main() {
    let s = String::from("hello");
    let len = calculate_length(&s);
    println!("'{}' has length {}", s, len);
}

fn calculate_length(s: &String) -> usize {
    s.len()
}
```

```C#
// C#
using System.Threading.Tasks;

[Serializable]
public class UserService<T> where T : class, new()
{
    public const int MaxRetries = 3;

    /// <summary>Asynchronously fetch a user.</summary>
    public async Task<T?> GetAsync(int id, string token = "")
    {
        if (id <= 0) throw new ArgumentException(nameof(id));
        var url = $"/api/users/{id:X}?t={token}";
        return await _http.GetFromJsonAsync<T>(url);
    }
}
```

```typescript
// TypeScript
import { Injectable } from '@nestjs/common';
import type { AuthToken } from './types';

/** Authentication service */
@Injectable()
export class AuthService {
    public static readonly MAX_ATTEMPTS = 5;
    private cache = new Map<string, AuthToken>();

    async login(email: string, pwd: string): Promise<AuthToken | null> {
        if (!email.includes('@') || pwd.length < 8)
            throw new Error(`Invalid: ${email}`);
        return { token: 'abc', expiresIn: 3600, valid: true };
    }
}
```

## Math

### Inline Math

Euler's identity $e^{i\pi} + 1 = 0$, the Pythagorean theorem $a^2 + b^2 = c^2$, the derivative $f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$.

### Display Math (rounded cream cards)

$$
m = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h} =: f'(a)
$$

$$
\iint\limits_{x^2 + y^2 \leq R^2} f(x,y)\,\mathrm{d}x\,\mathrm{d}y = \int_{\theta=0}^{2\pi} \mathrm{d}\theta \int_{r=0}^R f(r\cos\theta, r\sin\theta)\, r\,\mathrm{d}r
$$

$$
\forall \delta > 0, \exists N \in \mathbb{Z}^+, \text{s.t.} \forall n > N, |a_n - l| < \delta
$$

Matrix:

$$
A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$

## Mermaid Diagrams

### Flowchart

```mermaid
graph LR
    A(Start) --> input[/Input a, b/] --> if{a%b == 0?}
    if -->|yes| f1[GCD = b] --> B(End)
    if -->|no| f2["a, b = b, a % b"] --> if
```

### Sequence

```mermaid
sequenceDiagram
    autonumber
    participant User
    participant Frontend
    participant Backend
    participant Database
    participant Cache

    rect rgb(255, 250, 220)
    Note over User,Cache: Full request flow demo
    end

    User->>Frontend: Send request
    Frontend->>Backend: API call
    activate Backend
    Backend->>Cache: Query cache
    alt Cache hit
        Cache-->>Backend: Return data
    else Cache miss
        Backend->>Database: Query database
        Database-->>Backend: Return data
        Backend->>Cache: Write cache
    end
    Backend-->>Frontend: Response
    deactivate Backend
    Frontend-->>User: Render UI

    loop Heartbeat
        Frontend-)Backend: ping
    end
```

### Class Diagram

```mermaid
classDiagram
    class Animal {
        +String name
        +int age
        +eat()
        +sleep()
    }
    class Dog {
        +String breed
        +bark()
    }
    class Cat {
        +bool indoor
        +meow()
    }
    class Owner {
        +String name
        +List~Animal~ pets
    }

    Animal <|-- Dog : extension
    Animal <|-- Cat : extension
    Owner o-- Animal : aggregation
    Dog *-- Collar : composition
    Owner ..> VetService : dependency

    class Collar
    class VetService
```

### State Diagram v2

```mermaid
stateDiagram-v2
    [*] --> Pending
    Pending --> InProgress: start
    InProgress --> Done: finish
    InProgress --> Pending: pause
    InProgress --> Failed: error

    state InProgress {
        [*] --> Loading
        Loading --> Processing
        Processing --> Validating
        Validating --> [*]
    }

    Done --> [*]
    Failed --> Pending: retry
    Failed --> [*]: abandon
```

### Entity-Relationship Diagram

```mermaid
erDiagram
    USER ||--o{ ORDER : places
    USER {
        int id PK
        string name
        string email
    }
    ORDER ||--|{ LINE-ITEM : contains
    ORDER {
        int id PK
        int user_id FK
        date created_at
    }
    LINE-ITEM {
        int id PK
        int order_id FK
        int product_id FK
        int quantity
    }
    PRODUCT ||--o{ LINE-ITEM : "appears in"
    PRODUCT {
        int id PK
        string name
        decimal price
    }
```

### Gantt

```mermaid
gantt
    dateFormat  MM-DD
    axisFormat  %m-%d
    title       Project Milestones
    excludes    weekends

    section Design
    Requirements survey   :done,    a1, 01-06, 3d
    Prototyping           :active,  a2, after a1, 5d

    section Development
    Backend implementation :crit,    b1, after a2, 8d
    Frontend implementation:         b2, after a2, 10d
    Integration testing    :crit,    b3, after b1 b2, 3d

    section Release
    Deploy            :         c1, after b3, 1d
    Launch            :milestone, after c1, 0d
```

### Pie

```mermaid
%%{init: {'pie': {'showValues': false}}}%%
pie title Team Effort Distribution
    "Development" : 45
    "Meetings"    : 15
    "Review"      : 12
    "Docs"        : 10
    "Deploy"      : 8
    "Other"       : 10
```

### Journey

```mermaid
journey
    title My Working Day
    section Commute
      Wake up      : 3: Me
      Breakfast    : 4: Me, Family
      Subway       : 2: Me
    section Work
      Meetings     : 1: Me, Team
      Coding       : 5: Me
      Lunch        : 4: Me, Coworker
      Code Review  : 4: Me, Team
    section After work
      Workout      : 5: Me
      Sleep        : 5: Me
```

### Mindmap

```mermaid
mindmap
  root((Lightmind))
    Theme philosophy
      Mountain forest green
      LXGW WenKai
      JetBrains Mono
    Use cases
      Technical writing
      Academic notes
      Diary / essays
    Features
      Light theme
      Dark code blocks
      Rounded math cards
    Tech
      Pure CSS
      No external deps
```

### Git Graph

```mermaid
gitGraph
    commit id: "init"
    commit id: "v0.1"
    branch develop
    checkout develop
    commit id: "feat: tables"
    commit id: "feat: alerts"
    checkout main
    merge develop tag: "v0.2"
    branch hotfix
    checkout hotfix
    commit id: "fix: cursor"
    checkout main
    merge hotfix tag: "v0.2.1"
    commit id: "v0.3"
```

### XY Chart

```mermaid
xychart
    title "Monthly Sales (10k$)"
    x-axis ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]
    y-axis "Sales" 4 --> 11
    bar    [5, 6, 7.5, 8.2, 9.5, 10.5, 11, 10.2, 9.2, 8.5, 7, 6]
    line   [5, 6, 7.5, 8.2, 9.5, 10.5, 11, 10.2, 9.2, 8.5, 7, 6]
```

### Packet Diagram

```mermaid
---
title: "TCP Packet"
---
packet
0-15: "Source Port"
16-31: "Destination Port"
32-63: "Sequence Number"
64-95: "Acknowledgment Number"
96-99: "Data Offset"
100-105: "Reserved"
106: "URG"
107: "ACK"
108: "PSH"
109: "RST"
110: "SYN"
111: "FIN"
112-127: "Window"
128-143: "Checksum"
144-159: "Urgent Pointer"
160-191: "(Options and Padding)"
192-255: "Data (variable length)"
```

## Images

Inline image: ![](https://typora.io/img/favicon-64.png)

Centered standalone image:

![Typora Logo](https://typora.io/img/favicon-128.png)

## Footnotes

The pairing of LXGW WenKai[^1] with JetBrains Mono[^2] is the heart of this theme.

[^1]: LXGW WenKai — an open-source Chinese font maintained by lxgw, derived from FZ Xinkai.
[^2]: JetBrains Mono — a monospaced programming font designed by JetBrains, with ligatures.

## Alerts via Raw HTML

<div class="alert alert-tip">
<p>This is a tip block written in raw HTML (a fallback for older Typora versions that don't render GFM Alerts).</p>
</div>

## Horizontal Rule

The horizontal rule is a soft gradient.

---

## Conclusion

If everything above renders harmoniously —
- Paragraphs breathe naturally without friction
- Code blocks feel deep but not harsh
- Math cards melt into the page background
- Tables have clear inner / outer hierarchy
- Diagrams echo the body's color palette
- Mermaid diagrams show no out-of-place purples or blues

then the theme is ready to use.

> Made with `lightmind.css` · words growing among the mountains.
