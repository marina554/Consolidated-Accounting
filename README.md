Consolidated Accounting Models (Parent & Subsidiary)
Overview

This repository provides Python scripts for simulating consolidated accounting for a parent company and its subsidiary.

It covers different levels of complexity:

Simple Consolidation Model – Eliminates intercompany transactions and calculates basic consolidated B/S.

B/S + P/L Consolidation Model – Eliminates intercompany transactions and calculates both B/S and P/L, including operating income and net income distribution.

Full Consolidation with Investment & Equity Elimination – Adds elimination of parent’s investment in the subsidiary against subsidiary equity and calculates Non-Controlling Interest (NCI) accurately.

Purpose: Educational and illustrative. These scripts help learners understand the mechanics of consolidation, intercompany transaction elimination, and NCI.

Features Comparison
Feature	Simple Model	B/S + P/L Model	Full Investment Model
Intercompany transaction elimination	✅	✅	✅
Consolidated B/S	✅	✅	✅
Consolidated P/L	❌	✅	✅
Investment & Equity elimination	❌	❌	✅
Non-Controlling Interest (NCI)	Basic	Calculated	Accurate
Output format	pandas DataFrame	pandas DataFrame	pandas DataFrame
Educational focus	Beginner	Intermediate	Advanced
Workflow Diagram
                 Parent & Subsidiary Accounts
                          |
        +-----------------+-----------------+
        |                 |                 |
Simple Model       B/S + P/L Model     Full Investment Model
(Eliminate AR/AP)  (Eliminate AR/AP)  (Eliminate AR/AP + Investment & Equity)
        |                 |                 |
        v                 v                 v
   Consolidated B/S    Consolidated B/S   Consolidated B/S
                        Consolidated P/L
                             |
                             +--> Non-Controlling Interest (NCI)
                             +--> Net Income Attributable to Parent

How to Use

Install dependencies:

pip install pandas


Clone the repository:

git clone <repository_url>


Run any of the scripts:

Simple Model:

python simple_consolidation.py


B/S + P/L Model:

python bs_pl_consolidation.py


Full Investment & Equity Model:

python full_consolidation.py


Output:
All scripts print consolidated financial statements as pandas DataFrames.

Example (Full Model)

==== CONSOLIDATED BALANCE SHEET (B/S) ====
                     Cash  Accounts Receivable  Inventory  Accounts Payable  Non-Controlling Interests
Consolidated         1300                  600       400              550                    140

==== CONSOLIDATED INCOME STATEMENT (P/L) ====
                     Sales  COGS  SG&A  Operating Income  Net Income Attributable to NCI  Net Income Attributable to Parent
Consolidated         2500  1000   400             1100                           60                        1040

Notes

These models are simplified and educational, not for actual accounting reporting.

Intercompany transactions are assumed to be equal in all models.

Ownership ratio can be adjusted in the scripts (ownership = 0.6 by default).

The Full Investment Model shows how parent investment is eliminated against subsidiary equity and how NCI is calculated.

Recommended Usage

Beginners: Start with Simple Model to understand basic AR/AP elimination.

Intermediate: Use B/S + P/L Model to learn about operating income and net income consolidation.

Advanced: Use Full Investment Model to understand full consolidation including investment and equity elimination.

License

MIT License

------------------------------Japanese--------------------------------------------------

連結会計モデル（親会社＋子会社）
概要

このリポジトリには、親会社と子会社の連結会計をPythonでシミュレーションするスクリプトが含まれています。

3つのレベルのモデルを提供しています：

シンプル連結モデル – 親子間取引の消去と基本的な連結B/Sの作成

B/S＋P/L連結モデル – 親子間取引の消去に加え、B/SとP/L（営業利益・当期純利益）を作成

投資・資本消去付きフル連結モデル – 親会社の子会社投資を子会社資本と相殺し、正確な非支配株主持分（NCI）を計算

目的: 学習・教育用。連結会計の仕組み、親子間取引の消去、NCIの計算方法を理解するための教材。

特徴比較
特徴	シンプルモデル	B/S＋P/Lモデル	投資・資本消去モデル
親子間取引消去	✅	✅	✅
連結B/S作成	✅	✅	✅
連結P/L作成	❌	✅	✅
投資・資本消去	❌	❌	✅
非支配株主持分 (NCI)	基本	計算済み	正確
出力形式	pandas DataFrame	pandas DataFrame	pandas DataFrame
学習対象	初心者	中級者	上級者
処理フロー図
                 親会社・子会社の財務データ
                          |
        +-----------------+-----------------+
        |                 |                 |
  シンプルモデル      B/S＋P/Lモデル     投資・資本消去モデル
  (売掛金/買掛金消去)   (売掛金/買掛金消去) (売掛金/買掛金 + 投資・資本消去)
        |                 |                 |
        v                 v                 v
   連結B/S            連結B/S            連結B/S
                        連結P/L
                             |
                             +--> 非支配株主持分 (NCI)
                             +--> 親会社帰属当期純利益

使用方法

pandasをインストール:

pip install pandas


リポジトリをクローン:

git clone <repository_url>


スクリプトを実行:

シンプルモデル:

python simple_consolidation.py


B/S＋P/Lモデル:

python bs_pl_consolidation.py


投資・資本消去モデル:

python full_consolidation.py


出力例（投資・資本消去モデル）:

==== 連結貸借対照表 (B/S) ====
                     現金  売掛金  棚卸資産  買掛金  非支配株主持分
連結                 1300   600     400     550            140

==== 連結損益計算書 (P/L) ====
                     売上高  売上原価  販管費  営業利益  非支配株主持分当期純利益  親会社帰属当期純利益
連結                 2500    1000     400    1100               60                    1040

注意事項

このモデルは簡略化されており教育目的で作成されています。実務会計には使用できません。

親子間取引はすべて同額と仮定しています。

持分比率はスクリプト内で調整可能 (ownership = 0.6 がデフォルト)。

投資・資本消去モデルでは、親会社投資と子会社資本を相殺し、非支配株主持分（NCI）を正確に計算しています。

推奨使用方法

初心者: シンプルモデル → 売掛金/買掛金の消去を理解

中級者: B/S＋P/Lモデル → 営業利益・当期純利益の連結を学習

上級者: 投資・資本消去モデル → 投資相殺・NCI計算を含むフル連結を理解

ライセンス

MIT License
