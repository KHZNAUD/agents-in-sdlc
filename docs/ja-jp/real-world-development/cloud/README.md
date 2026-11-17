---
slug: ja-jp/real-world-development/cloud
title: "GitHub Copilot クラウド エージェント"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

[GitHub Copilot クラウド エージェント](https://docs.github.com/copilot/concepts/agents/cloud-agent/about-cloud-agent)を使うと、GitHub Copilot がクラウドで非同期に作業できます。GitHub で作業を割り当てると、クラウド エージェントがバックグラウンドでリポジトリを調べ、変更を行い、プル リクエストを作成します。その間、別の作業を進められます。

各演習では、クラウド エージェントが従うカスタム指示を追加し、GitHub Issue を割り当てて実装を依頼します。カスタム エージェントを確認してそのアプローチを調整し、エージェント ダッシュボードからセッションを監視して指示を出します。最後に、作成されたプル リクエストをレビューし、結果を改善します。

## 演習

| 演習 | トピック | 説明 |
|----------|-------|-------------|
| [0. 前提条件][ex0] | セットアップ | リポジトリと Codespace を作成します |
| [1. カスタム指示][ex1] | コンテキスト | クラウド エージェントが従うカスタム指示を追加します |
| [2. クラウド エージェント][ex2] | 非同期エージェント | GitHub Copilot クラウド エージェントに Issue を割り当てます |
| [3. カスタム エージェント][ex3] | 専門エージェント | カスタム エージェントを確認して使用します |
| [4. エージェントの管理][ex4] | 監視 | エージェント セッションを監視し、指示を出します |
| [5. 反復][ex5] | レビュー | プル リクエストをレビューし、Copilot の作業を改善して、次のステップを選びます |

## 前提条件

このワークショップに参加する前に、次の準備をしてください。

- [ ] 有効な **Copilot Student、Pro、Pro+、Business、Enterprise** プランを利用できる GitHub アカウント
- [ ] アカウントまたは組織で GitHub Copilot クラウド エージェントが有効になっていること

> [!TIP]
> 有料プランを利用していませんか？認証済みの学生は[GitHub Education][callout-student-plan-education]から GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使うエージェント、MCP、コード レビュー、Copilot CLI の機能が含まれているため、どのハーネスでも完了できます。

[callout-student-plan-education]: https://github.com/education/students

> [!NOTE]
> クラウド エージェントは **Copilot Student、Pro、Pro+、Business、Enterprise** で利用できます。Copilot Free では利用できません。Copilot Business または Enterprise では、管理者が組織で有効にする必要があります。

> [!NOTE]
> このハーネスでは MCP を扱いません。Copilot で MCP サーバーを使う方法については、[CLI ハーネス](../cli/)または [VS Code ハーネス](../vscode/)を参照してください。

## 開始

**[演習 0: 前提条件から開始 →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-custom-instructions/
[ex2]: 2-cloud-agent/
[ex3]: 3-custom-agents/
[ex4]: 4-managing-agents/
[ex5]: 5-iterating/
