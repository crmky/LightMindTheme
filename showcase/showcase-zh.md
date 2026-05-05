---
title: Lightmind 主题演示
author: SunMoonTrain
date: 2026-05-06
tags: [theme, markdown, demo]
---

# Lightmind 主题演示

> 一个山林森林绿调、霞骛文楷正文、JetBrains Mono 代码的 Typora 主题。

灵感来源于山间日落与森林边缘的温暖留白——主色取自远山的绿，配色用米黄纸面承托文字，代码块沉入深海军蓝。本文档系统地展示主题在各种 Markdown 语法下的表现，可作功能验证，也作设计样张。

## 标题层级

# H1：山林森林绿
## H2：深绿细线
### H3：左侧色条点缀
#### H4
##### H5
###### H6

各级标题应当层次清晰，但不会过分突兀。H1 双线、H2 单线、H3 左侧绿色色条、H4–H6 渐弱。

## 段落与行内格式

这是一个普通段落。**这是粗体（深森林绿）**，*这是斜体*，***这是粗斜体***，~~这是删除线~~，<u>这是下划线</u>。

行内代码：`const greeting = "Hello, world"`，行内数学：$E = mc^2$，行内键位：<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>。

==这是高亮文本==，可以混合 *==斜体高亮==*。 H<sub>2</sub>O 是水的化学式，E = mc<sup>2</sup> 是质能方程。<abbr title="HyperText Markup Language">HTML</abbr> 是超文本标记语言。

[这是一个链接](https://typora.io)，链接里的 `代码`，邮箱 <noreply@example.com>。

## 引用块与警告块

> 一行普通引用。中间留 4px 山林绿左色条，米雾绿底色，圆角矩形包裹。
>
> > 嵌套引用，色调更柔和。
>
> 引用里也可以放 **粗体**、*斜体* 和 `代码`。

> [!NOTE]
> 蓝色调。用于补充说明、温馨提示。

> [!TIP]
> 主色绿。用于实用建议、最佳实践。

> [!IMPORTANT]
> 紫色调。用于关键信息，不容忽视。

> [!WARNING]
> 暖橙黄。需要注意，可能影响结果。

> [!CAUTION]
> 砖红调。危险操作或破坏性变更。

## 列表

### 无序列表

- 第一项
- 第二项
  - 嵌套：空心 marker
  - 嵌套二
    - 三层嵌套
- 第三项

### 有序列表

1. 准备食材
2. 加热油锅
   1. 倒油
   2. 等待至七成热
3. 下锅翻炒

### 任务列表

- [x] 写主题大纲
- [x] 实现配色变量
- [x] 写完代码块语法高亮
- [ ] 跨平台测试
- [ ] 上传到主题仓库

## 表格

### 基本表格

| OS         | 全球占比 | 中国占比 |
| ---------- | -------- | -------- |
| Windows    | 76.56    | 87.55    |
| macOS      | 17.10    | 5.44     |
| Linux      | 1.93     | 0.75     |
| Chrome OS  | 1.72     | 0.01     |
| 其他       | 2.69     | 6.25     |

### 对齐方式

| 左对齐 | 居中 | 右对齐 |
| :----- | :--: | -----: |
| Apple  | 苹果 |    1.0 |
| Banana | 香蕉 |    2.5 |
| Cherry | 樱桃 |   18.7 |

### 单元格里的复杂内容

| 名称 | 描述 | 状态 |
| ---- | ---- | ---- |
| **粗体名称** | 含 `行内代码` 和 *斜体* | ✅ 正常 |
| 长名称示例 | 一段较长的描述文字，看看换行表现 | ⚠️ 警告 |
| 第三行 | [带链接的](https://example.com)单元格 | ❌ 失败 |

## 代码

### 行内代码

下载 `npm install` 后运行 `npm run dev`，访问 `http://localhost:3000`。

### 代码块（多语言）

语法高亮颜色借鉴了 One Dark 主题。

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

    /// <summary>异步获取用户</summary>
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

/** 用户认证服务 */
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

## 数学公式

### 行内公式

欧拉公式 $e^{i\pi} + 1 = 0$，毕达哥拉斯定理 $a^2 + b^2 = c^2$，导数 $f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$。

### 行间公式（圆角米色卡片）

$$
m = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h} =: f'(a)
$$

$$
\iint\limits_{x^2 + y^2 \leq R^2} f(x,y)\,\mathrm{d}x\,\mathrm{d}y = \int_{\theta=0}^{2\pi} \mathrm{d}\theta \int_{r=0}^R f(r\cos\theta, r\sin\theta)\, r\,\mathrm{d}r
$$

$$
\forall \delta > 0, \exists N \in \mathbb{Z}^+, \text{s.t.} \forall n > N, |a_n - l| < \delta
$$

矩阵：

$$
A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$

## Mermaid 图表

### 流程图（Flowchart）

```mermaid
graph LR
    A(开始) --> input[/输入 a, b/] --> if{a%b == 0?}
    if -->|yes| f1[GCD = b] --> B(结束)
    if -->|no| f2["a, b = b, a % b"] --> if
```

### 序列图（Sequence）

```mermaid
sequenceDiagram
    autonumber
    participant 用户
    participant 前端
    participant 后端
    participant 数据库
    participant 缓存

    rect rgb(255, 250, 220)
    Note over 用户,缓存: 完整请求流程测试
    end

    用户->>前端: 发起请求
    前端->>后端: API 调用
    activate 后端
    后端->>缓存: 查询缓存
    alt 缓存命中
        缓存-->>后端: 返回数据
    else 缓存未命中
        后端->>数据库: 查询数据库
        数据库-->>后端: 返回数据
        后端->>缓存: 写入缓存
    end
    后端-->>前端: 响应数据
    deactivate 后端
    前端-->>用户: 渲染界面

    loop 心跳检测
        前端-)后端: ping
    end
```

### 类图（Class Diagram）

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

### 状态图（State Diagram v2）

```mermaid
stateDiagram-v2
    [*] --> 待处理
    待处理 --> 进行中: 开始任务
    进行中 --> 已完成: 完成
    进行中 --> 待处理: 暂停
    进行中 --> 失败: 出错

    state 进行中 {
        [*] --> 加载
        加载 --> 处理
        处理 --> 验证
        验证 --> [*]
    }

    已完成 --> [*]
    失败 --> 待处理: 重试
    失败 --> [*]: 放弃
```

### 实体关系图（ER）

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

### 甘特图（Gantt）

```mermaid
gantt
    dateFormat  MM-DD
    axisFormat  %m-%d
    title       项目里程碑
    excludes    weekends

    section 设计阶段
    需求调研          :done,    a1, 01-06, 3d
    原型设计          :active,  a2, after a1, 5d

    section 开发阶段
    后端开发          :crit,    b1, after a2, 8d
    前端开发          :         b2, after a2, 10d
    集成测试          :crit,    b3, after b1 b2, 3d

    section 上线
    部署              :         c1, after b3, 1d
    上线              :milestone, after c1, 0d
```

### 饼图（Pie）

```mermaid
%%{init: {'pie': {'showValues': false}}}%%
pie title 团队精力分配
    "开发"    : 45
    "会议"    : 15
    "评审"    : 12
    "文档"    : 10
    "部署"    : 8
    "其他"    : 10
```

### 用户旅程（Journey）

```mermaid
journey
    title 我的工作日
    section 通勤
      起床        : 3: 我
      早餐        : 4: 我, 家人
      地铁        : 2: 我
    section 工作
      会议        : 1: 我, 团队
      编码        : 5: 我
      午餐        : 4: 我, 同事
      Code Review : 4: 我, 团队
    section 下班
      锻炼        : 5: 我
      睡眠        : 5: 我
```

### 思维导图（Mindmap）

```mermaid
mindmap
  root((Lightmind))
    主题理念
      山林森林绿
      霞骛文楷
      JetBrains Mono
    适用场景
      技术写作
      学术笔记
      日记 / 随笔
    特性
      浅色主题
      代码块深色
      公式圆角卡片
    技术
      纯 CSS
      无外部依赖
```

### Git 图（GitGraph）

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

### 时序坐标图（XY Chart）

```mermaid
xychart
    title "月销售额（万元）"
    x-axis ["一月", "二月", "三月", "四月", "五月", "六月", "七月", "八月", "九月", "十月", "十一月", "十二月"]
    y-axis "销售额" 4 --> 11
    bar    [5, 6, 7.5, 8.2, 9.5, 10.5, 11, 10.2, 9.2, 8.5, 7, 6]
    line   [5, 6, 7.5, 8.2, 9.5, 10.5, 11, 10.2, 9.2, 8.5, 7, 6]
```

### Sankey 桑基图

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

## 图片

文字行内的图片：![](https://typora.io/img/favicon-64.png)

居中独立图片：

![Typora Logo](https://typora.io/img/favicon-128.png)

## 脚注

霞骛文楷[^1] 与 JetBrains Mono[^2] 的搭配是这个主题的核心。

[^1]: LXGW WenKai，由 lxgw 维护的开源中文字体，基于霞鹜新晰黑改造。
[^2]: JetBrains Mono，由 JetBrains 设计的等宽编程字体，支持连字。

## 警告与原始 HTML

<div class="alert alert-tip">
<p>这是用原始 HTML 写的提示框（如果版本不支持 GFM Alerts，可降级到这种写法）。</p>
</div>
## 分隔线

分隔线是渐变色。

---

## 总结

如果以上各部分都呈现得自然协调——
- 段落的呼吸节奏不卡顿
- 代码块深色不刺眼
- 公式圆角米色卡片融入页面
- 表格内外框层次分明
- 图表配色与正文呼应
- mermaid 各类图都不见违和的紫色蓝色

那么这个主题已经基本可用了。

> Made with `lightmind.css` · 山林之间，文字生长。
