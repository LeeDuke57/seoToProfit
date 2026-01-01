https://seotoprofit.com/t/topic/1700

Brave Software 开发团队宣布，其浏览器现在默认阻止 Windows 的 Recall 功能，防止系统对 Brave 窗口进行截图，从而更好地保护用户隐私。

Recall 是微软在 2024 年 5 月首次推出的一项 AI 功能，旨在帮助用户“回忆”他们曾在电脑上查看的所有内容。其工作方式是每隔几秒对屏幕上的所有活动窗口截图，包括浏览网页、聊天或使用其他应用，并将内容存储为可搜索记录。

该功能一经发布，就遭到了信息安全专家和隐私保护人士的广泛批评。专家们将 Recall 比作“键盘记录器”（Keylogger），并演示了它如何被用于窃取用户的敏感数据。

面对批评，微软一度推迟 Recall 的上线，并表示会加强安全性，使其成为可选功能，且数据库加密，只有用户通过 Windows Hello 身份验证后才可访问。

2024 年底，Recall 再次面向 Windows Insider 测试者开放，但用户发现 Recall 仍会保存银行卡号、社保号等敏感信息，即使这些内容在设置中已被禁用，因此再次引发争议【来源](Функция Recall в Windows делает скриншоты номеров банковских карт — Хакер)】。

2025 年春季，微软通过 Windows 11 KB5055627 更新开始将 Recall 推送至搭载 Copilot+ 的电脑，随后凡是安装了 5 月份更新的用户也获得了该功能【来源](Copilot+ PCs are the most performant Windows PCs ever built, now with more AI features that empower you every day | Windows Experience Blog)】。

Brave 浏览器开发者表示，他们已提前采取措施，防止 Recall 捕捉 Brave 浏览器的窗口内容：

「考虑到 Brave 一直以隐私优先为核心，并且 Recall 会记录完整的浏览历史，我们决定默认阻止 Recall 捕捉 Brave 的标签页。我们认为浏览器活动不应轻易被写入可能被滥用的永久数据库，尤其是在某些敏感场景下，例如家暴。」

开发团队还在 GitHub 上说明，他们通过调用微软的 SetInputScope API，并为所有浏览器窗口设定 IS_PRIVATE 属性，从而通知 Windows 不应捕捉或索引这些内容。

「微软表示，浏览器可以通过设置 SetInputScope 为 IS_PRIVATE，让 Recall 不记录其浏览内容。我们现在强制对所有窗口应用该设置。」

这一改动已在 Brave Nightly 测试版本中实现，并将在接下来的稳定版本中全面上线。

值得一提的是，今年 5 月，Signal 也做出类似决定，默认屏蔽 Recall，称「微软根本没留给我们其他选择」【来源](Signal блокирует работу Windows Recall — Хакер)】。
