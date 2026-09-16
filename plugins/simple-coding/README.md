# Simple Coding

AIコーディングにおける過剰実装・過剰設計・不要な抽象化・依頼外変更を抑えるためのプラグインです。依頼の範囲と完了条件を明確にし、必要最小限の変更を検証して止めます。

## 使い方

ChatGPTで `+` → `More` → **Simple Coding** を選択してから、コーディングの依頼を送ります。通常チャットでは自動適用せず、必要なときだけ使う設計です。

## ChatGPTワークスペースへの導入

このリポジトリをGitHubへpushしたあと、管理ワークスペースで次の操作を行います。

1. `Workspace settings` → `Plugins` → `Add` → `Import marketplace` を開く。
2. `Source` にこのGitHubリポジトリのURLを入力する。
3. `Path` に `.agents/plugins` を入力してマーケットプレイスをインポートする。
4. インポート結果で **Simple Coding** を確認し、利用可能なメンバーへ公開する。
5. ChatGPTのチャットで `+` → `More` から選択する。

利用できる項目や作成・導入権限は、プラン、地域、ワークスペースの設定、ロールによって異なります。個人アカウントで表示されない場合は、ワークスペース管理者による導入が必要です。

## コーディングで適用する4原則

1. まず考え、前提を隠さない
2. 最小十分な成果物を選ぶ
3. 変更は局所的にする
4. 成功条件を決め、確認して止める

## 失敗ループの停止条件

同一原因・同一状態で2回進展がなければ、その診断・検証を終了します。新しい事実がない限り3回目は行いません。目的へ戻れる場合は別の経路へ戻り、戻れない場合だけ原因と制約を1回報告して停止します。

## 制約

このプラグインはAIコーディングの行動指針を提供するもので、モデルの返答やコード変更を機械的に強制するものではありません。完了条件と実施した検証結果を確認してください。

## ライセンス

このプラグインの新規の適応・構成・パッケージング部分はMITライセンスで提供します。

## Attribution

Simple Coding is inspired by the four principles in [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills), which is based on Andrej Karpathy's observations about common failure modes in LLM-assisted coding.

This plugin adapts those principles for AI-assisted coding in ChatGPT.

Original adaptation and plugin implementation:

Copyright (c) 2026 E-COM Co., Ltd.
