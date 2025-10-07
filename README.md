# 為台灣打造統一災害資訊本體論 (A Unified Disaster Information Ontology for Taiwan)

這是一個旨在為台灣建立一個統一、開放、且機器可讀的災害資訊標準的開源計畫。我們的目標是打破資訊孤島，提升各單位在災害應變中的協作效率，並增強整個國家的防災韌性。

## 核心概念

本地震、颱風等災害頻繁，但現有的應變體系中，不同單位（政府、軍方、NPO、社區）間的資訊交換常缺乏共通標準，導致資料格式混亂、難以整合，延遲了「共通作戰圖像」（Common Operational Picture）的形成。

本計畫提出了一套以 **GeoJSON** 為核心的災害資訊本體論（Ontology）。這套標準：

* **結構化**：依循台灣法定的「災前預防、災中應變、災後復原」三階段進行設計。
* **功能導向**：整合了美國「社群生命線」(Community Lifelines) 等國際最佳實踐，以系統性地評估災害衝擊。
* **地理空間原生**：所有資訊都帶有地理標記，可直接應用於地圖視覺化，並與 **OpenStreetMap (OSM)** 的圖資標籤深度整合。
* **兼容並蓄**：接軌通用預警協定 (CAP)、人道主義交換語言 (HXL) 等現行國際標準。

## 為何重要？

採納此一開放標準將帶來以下效益：

* **提升互操作性**：讓不同系統與平台能「說同一種語言」，確保資訊無礙流動。
* **加速決策制定**：提供即時、標準化的情資，幫助指揮官快速掌握全局。
* **賦能協作生態系**：讓政府、民間組織與公民科技社群能基於共通的資料基礎進行協作與創新。
* **與國際接軌**：使台灣的災防資料能與國際救援團隊的系統快速對接。

## 如何貢獻

這是一個開放的專案，我們誠摯邀請所有關心台灣防災韌性的利害關係人——無論您是政府單位、非營利組織、開發者、或第一線的應變人員——共同參與。

您可以透過以下方式貢獻：

* **檢視與回饋**：在 [Issues](https://github.com/your-repo/issues) 中提出您對本體論設計的建議或問題。
* **參與討論**：分享您在實務上遇到的資料交換挑戰。
* **提交修改**：透過 Pull Request 直接貢獻您的修改建議。

讓我們共同努力，為台灣打造一個更具韌性的未來。

## 授權

本計畫內容採用 [創用 CC 姓名標示 4.0 國際 授權條款](https://creativecommons.org/licenses/by/4.0/) 進行授權。


# A Unified Disaster Information Ontology for Taiwan

This is an open-source initiative to establish a unified, open, and machine-readable data standard for disaster information in Taiwan. Our goal is to break down information silos, enhance collaboration efficiency among response units, and strengthen national disaster resilience.

## Core Concepts

Taiwan frequently faces disasters like earthquakes and typhoons. However, in the current response framework, information exchange between different units (government, military, NPOs, local communities) often lacks a common standard. This results in fragmented data formats that are difficult to integrate, delaying the formation of a Common Operational Picture (COP).

This project proposes a comprehensive disaster information ontology built on the **GeoJSON** format. This standard is:

* **Structured**: Designed according to Taiwan's legal three-phase disaster management lifecycle: Preparedness, Response, and Recovery.
* **Function-Oriented**: Integrates international best practices, such as the U.S. "Community Lifelines" framework, to systematically assess disaster impacts.
* **Geospatially Native**: Every piece of information is geotagged for direct use in map visualizations and is deeply integrated with **OpenStreetMap (OSM)** tagging conventions.
* **Interoperable**: Aligns with existing international standards like the Common Alerting Protocol (CAP) and the Humanitarian Exchange Language (HXL).

## Why It Matters

Adopting this open standard will:

* **Enhance Interoperability**: Allow different systems and platforms to "speak the same language," ensuring seamless data flow.
* **Accelerate Decision-Making**: Provide real-time, standardized intelligence to help commanders grasp the overall situation quickly.
* **Foster a Collaborative Ecosystem**: Enable government agencies, civil society, and the civic tech community to collaborate and innovate on a common data foundation.
* **Align with International Efforts**: Facilitate rapid integration of Taiwan's disaster data with systems used by international rescue teams.

## How to Contribute

This is an open project, and we sincerely invite all stakeholders passionate about Taiwan's disaster resilience—including government agencies, non-profits, developers, and first responders—to participate.

You can contribute in the following ways:

* **Review and Feedback**: Raise questions or suggestions about the ontology design in the [Issues](https://github.com/your-repo/issues) section.
* **Join the Discussion**: Share the data exchange challenges you've encountered in the field.
* **Submit Changes**: Contribute your proposed modifications directly via Pull Requests.

Let's work together to build a more resilient future for Taiwan.

## License

This work is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).


# 台湾における統一災害情報オントロジー

これは、台湾のために統一された、オープンで機械判読可能な災害情報標準を確立するためのオープンソース・イニシアティブです。私たちの目標は、情報のサイロ化を解消し、災害対応における各組織間の連携効率を高め、国家全体の防災レジリエンスを強化することです。

## 中核となる概念

台湾は地震や台風などの災害が頻発しますが、現行の対応体制では、異なる組織（政府、軍、NPO、地域社会）間の情報交換に共通の基準が欠けていることが多くあります。これにより、データ形式が断片的で統合が困難となり、「共通作戦状況図」（Common Operational Picture, COP）の形成が遅れる原因となっています。

このプロジェクトでは、**GeoJSON**を中核とした包括的な災害情報オントロジーを提案します。この標準は以下の特徴を持っています：

* **構造化**: 台湾の法規に基づく「事前準備、応急対応、復旧・復興」の三段階の災害管理サイクルに従って設計されています。
* **機能指向**: 米国の「コミュニティ・ライフライン」のような国際的なベストプラクティスを統合し、災害の影響を体系的に評価します。
* **地理空間ネイティブ**: 全ての情報が地理的にタグ付けされ、地図での可視化に直接利用でき、**OpenStreetMap (OSM)** のタギング規則と深く統合されています。
* **相互運用性**: 共通警告プロトコル（CAP）や人道支援交換言語（HXL）など、既存の国際標準と整合しています。

## なぜ重要か？

このオープンスタンダードを採用することには、以下の利点があります：

* **相互運用性の向上**: 異なるシステムやプラットフォームが「同じ言語を話す」ことを可能にし、シームレスな情報の流れを確保します。
* **意思決定の迅速化**: リアルタイムで標準化された情報を提供し、指揮官が全体の状況を迅速に把握するのを助けます。
* **協調的なエコシステムの育成**: 政府、市民社会、シビックテックコミュニティが共通のデータ基盤の上で協力し、革新を生み出すことを可能にします。
* **国際社会との連携**: 台湾の災害データを国際的な救援チームが使用するシステムと迅速に統合できるようにします。

## 貢献の方法

これはオープンなプロジェクトであり、台湾の防災レジリエンスに関心を持つすべてのステークホルダー（政府機関、非営利団体、開発者、第一線の対応者など）の皆様のご参加を心より歓迎いたします。

以下の方法で貢献できます：

* **レビューとフィードバック**: [Issues](https://github.com/your-repo/issues)セクションで、オントロジー設計に関する質問や提案を提起してください。
* **議論への参加**: 現場で遭遇したデータ交換の課題を共有してください。
* **変更の提案**: プルリクエストを通じて、直接変更案を提案してください。

台湾のよりレジリエントな未来のために、共に協力しましょう。

## ライセンス

この著作物は、[クリエイティブ・コモンズ 表示 4.0 国際 ライセンス](https://creativecommons.org/licenses/by/4.0/)の下に提供されています。


