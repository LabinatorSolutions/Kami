---
type: llm
weight: 1
focus: {source: file, path: "report.html"}
---

PASS only if all of these hold in the filled HTML equity report:
- Any derived number (market cap, EPS, growth rate, upside) is arithmetically correct from the given inputs (market cap ≈ 132 亿元, 2026E EPS ≈ 1.29 元, 38x ≈ 49 元).
- No outside data (peer companies, industry size, analyst consensus, real tickers) is introduced.
FAIL on any wrong arithmetic or invented outside figure. Whether the supplied figures survive is checked by a separate regex grader; do not judge it here.

The brief the author worked from follows. Everything it states is supplied, not invented, so judge invention only against it, and do not fail a fact because the list above omits it:

> 帮我写一份个股研究报告 PDF，放在当前目录。公司是虚构的「星衡储能」，用来做内部培训案例，数据全部以我给的为准，不要自己补充外部数据。直接做完，不用问我。HTML 源文件命名为 report.html，PDF 命名为 report.pdf。
>
> - 主营：工商业储能系统集成，2025 年收入占比：储能系统 72%、运维服务 18%、其他 10%。
> - 收入：2023 年 18.4 亿元，2024 年 26.9 亿元，2025 年 35.2 亿元。
> - 归母净利润：2023 年 1.1 亿元，2024 年 2.0 亿元，2025 年 2.9 亿元。
> - 毛利率：2023 年 17.8%，2024 年 19.6%，2025 年 21.3%。
> - 当前股价 42.6 元，总股本 3.1 亿股。
> - 我们的判断：2026 年收入 46 亿元，净利润 4.0 亿元，给 2026 年 38 倍 PE，目标价约 49 元，评级「增持」。
> - 催化剂：海外工商业订单放量（2026 上半年在手订单 12 亿元）、电芯价格下行带来毛利率提升。
> - 风险：电芯价格反弹、应收账款周转天数从 96 天升到 128 天、行业价格战。
