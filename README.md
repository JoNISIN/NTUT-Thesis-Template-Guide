# 臺北科技大學學位論文的 LaTeX 參考模板與使用指引

這是一個基於 XeLaTeX 的臺北科技大學學位論文模板預設使用於 [Overleaf](https://www.overleaf.com/) 線上平台。

這個模板除了對於學位論文樣式的調整之外也提供了額外的排版指令以簡化使用者在內容創作外的負擔。

在此之上，本模板代碼庫之內容亦為工作區中[PDF](https://github.com/JoNISIN/NTUT-Thesis-Template-Guide/blob/main/ntut_temp_guide.pdf)編譯結果的原始代碼，其內容包含:
1. 對本模板的使用指引
2. 對 LaTeX 新手的使用指引
3. 對初次撰寫論文者的經驗引導

其中的內容大多具備完整的思路引導與文獻引用，目的是在其模板本身的工具性質之外試圖啟發使用者對於 LaTeX 排版工具的學習興趣與學術寫作的思路，以使一些創造性工作不致於在不知目的的要求下變得無味而枯燥。

對於需要僅包含本模板所提供之樣式與指令的空白模板的使用者可以到[另一個代碼庫](https://github.com/JoNISIN/NTUT-Thesis-Template-Empty/)中取得。

在這份Readme中接下來的內容會包含:
1. [本模板特色的簡要說明](#簡要說明)
2. [如何應用本模板於Overleaf](#於-Overleaf-線上使用)
3. [本模板中部分內容的聲明與提醒](#對於本模板內容的聲明與提醒)

## 簡要說明

除了更加嚴格的樣式調整之外，本模板中主要提供下面內容：
1. 中英文論文模板的快速切換
2. 基於***變數設定***的封面頁、標題頁與中英文摘要自動生成 (包含頁碼自動計算)
3. 可以套用變數設定結果或空白的學位口試審定書生成
4. 論文寫作中常用的指令腳本

在文章內容上主要包含:
1. 模板指令的使用指引
2. 論文寫作上常用的 LaTeX 語法教學
3. BibTeX 格式的使用教學
4. 美化論文排版教學
5. 數學環境中的排版教學
6. 以引用網頁為主的參考文獻格式調整教學
7. 模板格式與教學指引中所需參考的詳細文獻

## 於 Overleaf 線上使用

Overleaf 是一個功能相當完善的線上 LaTeX 平台，其中預先安裝了足夠於學術論文寫作的Package、字體、樣式並且其社群中有提供大量實用模板於學術以外的功能。

這個模板可以下面步驟直接應用於 Overleaf 上
1. 在[代碼庫頁面](https://github.com/JoNISIN/NTUT-Thesis-Template-Guide)找到下載代碼庫的*Code*按鈕
2. 以[Zip格式下載](https://github.com/ntut-xuan/NTUT-Thesis-Template/archive/refs/heads/main.zip)代碼庫
3. 在 Overleaf 主頁中點擊 *New Project*
4. 選擇 *Upload Project*
5. 直接將下載的 Zip 檔案上傳 (Overleaf 會自動解壓縮該檔案)
6. (修改上傳建立的 Project 的名稱)
7. 進入建立的 Project
8. 點擊左上角 *Menu* 並找到 *Settings*
9. 修改 *Compiler* 為 `XeLaTeX`
10. 點擊預覽區的重新編譯 (Recompile) 或在編輯區使用儲存快捷鍵即可查看編譯中文檔案結果

## 對於本模板內容的聲明與提醒

1. 本模板中僅中英文摘要與誌謝使用*AI的幽默*自動總結而成，但實操中建議嚴格人工以避免不必要的爭議。
2. 如需引用[本引導文章](https://github.com/JoNISIN/NTUT-Thesis-Template-Guide)的內容，可以參考`IEEEtran`的參考文獻樣式下網頁的引用方式
```
@misc{bibtex,
  title        = {臺北科技大學學位論文的 LaTeX 參考模板與使用指引},
  author       = {JoNISIN},
  year         = {Mar. 2025},
  url          = {[https://www.bibtex.com/e/entry-types/](https://github.com/JoNISIN/NTUT-Thesis-Template-Guide)},
  howpublished = {GitHub}
}
```

## 更新歷程

### 2025-07-31

- `env.tex` 更新
  - 實現了對於中英文與碩博士的不同排版需求的自動切換功能。
  - 添加中英文模板、碩博士模板
  - 修正封面格式模板
  - 修改標題排版方式由 `hnag` 改為 `block`
  - 根據學校需求更新摘要的格式模板
  - 修正目錄頁自身索引之頁碼錯誤問題
  - 移除部分冗余指令
  - 可以自動化生成碩博士審定書
- `style.tex` 更新
  - 修改標題排版方式由 `hnag` 改為 `block`
  - 修改代碼用字體為所有平台皆有的 `Andale Mono`
  - 移除冗余描述
  - 移動字體調整至 `main.tex` 以便於使用者調整字體
- `main.tex` 更新：
  - 字體調整移動至此檔案中，並添加註解標註各平台字體使用
  - 移除並修改已經無效的代碼
  - 相關論文格式需求添加註解提醒
  - 根據代碼修改結果，更新部分指令使用方式
  - 新增新指令的使用說明
  - 新增**離校流程**方面的說明訊息
- 新增 `.gitignore` ：
  - 針對本地 LaTeX 過程檔案新增忽略訊息