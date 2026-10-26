# Shoko Oka · `0xshooka`

Independent open-source developer and researcher in Japan. I build small, inspectable tools for life science and AI agents, with an emphasis on provenance, bounded behavior, and honest failure modes.

[Website](https://cyanos-lab.com) · [arXiv](https://arxiv.org/a/oka_s_1) · [ORCID](https://orcid.org/0009-0003-6607-1143) · [X](https://x.com/0xshooka) · [Zenn](https://zenn.dev/0xshooka) · [LinkedIn](https://linkedin.com/in/shoko-oka-71a648167/)

## Featured project: [Promethica](https://github.com/0xshooka/promethica)

**A read-only MCP server for traceable life-science data retrieval and deterministic reaction-network analysis.**

Promethica connects ChatGPT, Claude, and other MCP clients to UniProt, Rhea, ChEBI identifiers, RCSB PDB, Gene Ontology and GO-CAM, Open Targets, and ChEMBL. It provides 22 tools for protein, structure, reaction, pathway, disease, and drug data without using an LLM for retrieval or graph calculations.

The public MVP is intentionally conservative:

- API failures, valid zero results, and missing annotations remain distinct states.
- Responses are bounded and include stable identifiers, provenance, and completeness metadata where available.
- Reaction-network candidates are labeled as hypotheses, not biological conclusions.
- Local PDB access is allowlisted, path-resolved, extension-checked, and size-limited.
- The default test suite is offline and mocks external services; all 39 tests pass for the current public MVP.
- Source and data licensing are documented separately. The code is licensed under Apache-2.0.

```bash
git clone https://github.com/0xshooka/promethica.git
cd promethica
uv sync --extra dev
uv run pytest
uv run python promethica.py
```

Promethica is early-stage software. It does not evaluate compartment, thermodynamics, kinetics, expression, or organism context, and its output is not medical advice. See the [README](https://github.com/0xshooka/promethica#readme), [data-source notes](https://github.com/0xshooka/promethica/blob/main/DATA_SOURCES.md), and [contribution guide](https://github.com/0xshooka/promethica/blob/main/CONTRIBUTING.md) before relying on it.

Issues and focused pull requests are welcome—especially reproducible bug reports, parser fixtures based on documented upstream responses, and tests for scientific edge cases.

## Selected work

| | |
| --- | --- |
| **Paper** | [*Evaluating Large Language Models on the Frame and Symbol Grounding Problems: A Zero-shot Benchmark*](https://arxiv.org/abs/2506.07896) |
| **Book** | 『MCPサーバー開発大全』, 技術評論社, ISBN 978-4-297-15327-4 |
| **Code** | MCP servers, life-science tooling, and experiment harnesses in my [public repositories](https://github.com/0xshooka?tab=repositories) |
| **Applied work** | [群青研究所 / Cyanos Lab](https://cyanos-lab.com) — drug-discovery infrastructure, biomaterials, and small tools |

## How I work

- Prefer primary specifications and documented API behavior over guessed schemas.
- Keep defaults small, read-only, and reversible.
- Make uncertainty and incomplete data visible in the interface.
- Add offline regression tests before depending on live services.
- Treat security reports carefully; please report exploitable issues privately rather than publishing details in an issue.

My broader research interests include machine cognition, accessible knowledge representation, and accountability for AI agents. The philosophical questions matter to me, but I try to make the answers inspectable in code.

<details>
<summary><b>日本語</b></summary>

<br>

日本を拠点に活動する独立系のOSS開発者・研究者です(工学修士)。専門領域は生命科学とAIエージェントです。

現在の中心プロジェクトは **[Promethica](https://github.com/0xshooka/promethica)** です。ChatGPTやClaudeなどのMCPクライアントからUniProt、Rhea、RCSB PDB、Gene Ontology / GO-CAM、Open Targets、ChEMBL等を参照し、反応ネットワークを決定論的に解析できる読み取り専用のMCPサーバーです。

公開MVPでは、結果を派手に見せることよりも、次の点を優先しています。

- APIエラー、正常に得られた0件という結果、アノテーションの欠如を区別する
- 取得元と識別子、解析の完全性を示す情報を可能な限り保持する
- ネットワークから得た候補を、生物学的事実ではなく仮説として返す
- 応答サイズ、ローカルファイルアクセス、リトライを制限する
- 外部APIに依存しない回帰テストを用意する
- ソフトウェアと上流データのライセンスを分けて明記する

まだ初期段階のソフトウェアであり、医学的判断には使用できません。再現可能なバグ報告、科学的なエッジケースの共有、テストの追加などのコントリビューションを歓迎します。

</details>

---

If something here is useful, open an issue, send a focused pull request, or start a technical conversation. Clear questions are always welcome.