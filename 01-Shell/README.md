# 🐚 Shell 學習筆記

> Shell 是你和作業系統之間的翻譯官。  
> 不管是打指令、執行腳本，還是讓程式自動化，都離不開它。

---

## 一、Shell 是什麼？

Shell 是一種操作作業系統的工具，負責接收指令並與作業系統（特別是 Kernel）溝通。

```
人類（打指令 / 按按鈕）→ Shell → 作業系統（Kernel）→ 執行結果
```

Shell 的主要功能：

- 接收使用者輸入的指令（不論是打的還是由程式產生的）
- 解析並執行這些指令
- 管理程式執行、檔案操作、流程控制等

> 🌉 Shell 是「溝通者」，負責將來自人類或程式的操作轉交給作業系統執行。

---

## 二、Shell、Terminal、CLI、GUI 的關係

| 名詞 | 中文說法 | 是什麼 | 比喻 |
| --- | --- | --- | --- |
| **Shell** | 殼程式 / 指令解譯器 | 實際解析、執行指令的程式（如 bash、zsh） | 翻譯官 |
| **Terminal** | 終端機 | 讓你跟 Shell 互動的視窗程式 | 翻譯官的辦公室 |
| **CLI** | 命令列介面 | 用打字方式操作電腦的「模式」 | 靠說話溝通的方式 |
| **GUI** | 圖形使用者介面 | 用滑鼠點按操作的介面 | 靠手勢/按鈕溝通 |

簡化流程圖：

```
人類 → CLI（打字）  ─┐
     → GUI（按鈕）  ─┤→ Shell → 作業系統
應用程式 → 程式呼叫 ─┘
```

> 💡 你打開 Terminal，裡面跑的那個東西就是 Shell。  
> GUI 的按鈕（例如 VS Code 的「執行」按鈕）背後也常常觸發 Shell 指令。

---

## 三、誰可以操作 Shell？

### 人類

- 透過 **CLI**：開啟 Terminal，打 `cd`、`ls`、`git push` 等指令
- 透過 **GUI**：點選「Build 專案」、「發佈網站」等按鈕，背後可能觸發 Shell 腳本

### 應用程式

```python
# Python 呼叫 Shell 指令
import subprocess
subprocess.run(["ls", "-al"])
```

```javascript
// Node.js 呼叫 Shell 指令
const { exec } = require("child_process");
exec("ls -al");
```

```c
// C 語言呼叫 Shell 指令
system("ls -al");
```

> 例如你在 Visual Studio 按下「打包」，實際上執行的是 `msbuild` 或 `dotnet publish`。

---

## 四、常見的 Shell 類型

| Shell 名稱 | 適用平台 | 特點 |
| --- | --- | --- |
| **bash** | Linux / macOS | 最常見，支援腳本與變數操作 |
| **zsh** | macOS 預設 | 語法進階、自動補全美化 |
| **fish** | 跨平台 | 即時提示、簡化語法、無需配置 |
| **PowerShell** | Windows / Linux / macOS | 支援物件導向、整合 .NET |
| **cmd** | Windows | 傳統命令列介面，功能有限但常見 |

> 每種 Shell 就像是不同的翻譯器，幫你把你的想法交給系統處理。

---

## 五、Command-Line Tools 是什麼？

Command-Line Tools 是在 CLI 環境中使用的工具或應用程式。它們**不是 Shell 本身**，而是 Shell 呼叫來執行的外部程式。

常見例子：

| 工具 | 用途 |
| --- | --- |
| `git` | 版本控制 |
| `node` | 執行 JavaScript |
| `python` | 執行 Python |
| `curl` | 發送 HTTP 請求 |
| `docker` | 容器管理 |
| `npm` | Node.js 套件管理 |

> 🛠️ Shell 是主持人，Command-Line Tools 是被叫上台表演的來賓。

---

## 六、REPL 是什麼？

REPL（Read-Eval-Print Loop）是一種互動式的程式語言執行環境。輸入一段程式語法，它會馬上執行並印出結果。

| REPL 指令 | 對應語言 |
| --- | --- |
| `node` | JavaScript |
| `python` | Python |
| `irb` | Ruby |

**REPL vs Shell 的差異：**

| | Shell | REPL |
| --- | --- | --- |
| **控制範圍** | 整個作業系統 | 只限於該程式語言 |
| **能用 `cd`、`ls`？** | ✅ | ❌ |
| **比喻** | 系統操作員 | 語言的互動沙盒 |

---

## 七、Shell Script

Shell script 是把多條 Shell 指令寫進一個 `.sh` 檔案，讓系統一次自動執行整段流程。

```bash
#!/bin/bash
mkdir my_project
cd my_project
touch index.html
echo "專案建立完成！"
```

常見用途：

- 自動部署、建置
- 系統備份、檔案管理
- 開發流程簡化（建資料夾、打包等）

> 📜 Shell script 就像是一份「操作流程清單」，讓系統一次完成你要的任務。

---

## 八、總結

| 概念 | 一句話說明 |
| --- | --- |
| **Shell** | 執行系統指令的工具，是人與程式都能派任務給它的「系統操作員」 |
| **Terminal** | 啟動 CLI / Shell 的視窗程式 |
| **CLI** | 用文字輸入與 Shell 互動的方式 |
| **GUI** | 用圖形介面操作，背後也可能呼叫 Shell |
| **Command-Line Tools** | Shell 呼叫來完成任務的外部程式（如 git、node） |
| **REPL** | 語言層級的互動執行介面，不等同於 Shell |
| **Shell Script** | 將多條指令寫成檔案，讓系統自動執行 |
