# **1. Introduction**

## **Defining Safety**

Safetyとは、「事故が起こらない状態」ではなく、実験に伴うHazard（危険有害要因）とRiskを理解し、適切に評価し、そこで得た気づきを共有し、継続的に改善していく循環的なプロセスである。WHOのLaboratory Biosafety Manual第4版（LBM4）も、画一的な規則ではなく、リスクとエビデンスに基づいて対策を決定する「リスク・エビデンスベースのアプローチ」を採用している[^1]。

Hazardは、生物学的因子や機器・試薬など、それ自体が危害を引き起こしうる要因を指す。一方Riskは、そのHazardの発生可能性（likelihood）と影響（consequences）を、実験手順・作業環境・作業者の技量まで含めて評価して初めて定まる。したがってRisk Assessmentでは、生物学的因子そのものだけでなく、それを取り巻く実験手順・環境・人を含めて評価する必要がある[^1]。

しかし、Riskを正しく評価するだけではSafetyは維持されない。実際に起きた小さな異常やヒヤリハットを見逃さず共有し、そこから得た知見を次のRisk Assessmentや日々の実践に反映させて初めて、Safetyは改善され続ける。私たちは、このHazard/Riskの理解→適切な評価→ヒヤリハットの共有→継続的な改善というサイクルを回し続けることを、Safetyの基本的な考え方としている。

![Safety continuous cycle](https://static.igem.wiki/teams/6144/wiki/safety/safety-introduction.avif =600x)

:::c

**Fig. 11.4.1.** The continuous safety cycle at iGEM Waseda-Tokyo

:::

## **iGEM-WasedaにおけるSafety**

私たちはこのサイクルを、本ページで紹介する4つの章の取り組みとして具体化している。

* **Understand Hazards & Risks**：Our Laboratory（2章）でのSDS共有・試薬管理や、Training and Certification（3章）の教育・認定制度を通じて、全メンバーがHazardとRiskを正しく理解する  
* **Assess Risks Properly**：Risk Assessment（4章）で、Physical・Chemical・Biologicalの3観点からHazardを洗い出し、対策を講じる  
* **Near-Miss Sharing**：Our Laboratory（2章）の実験終了報告書による日々の記録や、Supervisor Certification Testのケーススタディで使う学内のヒヤリハット事例を通じて、小さな異常も見逃さず共有する  
* **Continuous Improvement**：Emergency Responses（5章）のマニュアルの定期的な見直しや、Continuing Education（3章⑤）での継続的な学びを通じて、得られた知見を次の実践に反映させる

# **2. Our laboratory**

## **Lab Overview**

　プロジェクトに関する全ての実験は、早稲田大学先端生命医科学センターTWIns内の設備を利用して実施されました。私たちが実験を行ったのはBSL-1のスペースです。また、施設共用の実験機器を操作する際には、同施設の朝日研究室の皆様にご同伴いただきました。実験環境をご提供いただいた朝日教授・竹山教授、およびご同伴いただいた朝日研究室の皆様に、あらためてお礼申し上げます。

ラボの見取り図（作成予定）：

![Floor map of our laboratory](https://static.igem.wiki/teams/6144/wiki/safety/floor-map.avif =600x)

:::c

**Fig. 11.4.2.**Floor map of our laboratory

:::

## **Equipments**

朝日研究室には、生命科学実験を行うための基本的な装置が揃っています。このうち一部の装置を共用で使用して、チームは実験を行っています。使用にあたって注意が必要な点は、必ず朝日研究室のメンバーからご教示いただき、それらを厳密に順守して日々実験しています。

![Typical equipments we use in the Asahi lab.](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-equipments.avif  =400x)

:::c

**Fig. 11.4.3.** Typical equipments we use in the Asahi lab.

:::

## **Managements**

　私たちは学部１～４年生であり、専門的な実験を行った経験が十分ではありません。そのため、安全に実験を行うにあたって複数の取り組みをしています。以下にそれらの内容とその目的を示します。

1. **実験責任者の設置**  
   　私たちのチームでは、wet実験への関与の程度と役割に応じて、メンバーを以下の3つの立場に区分しています。ラボ内で実際の操作を伴うwet実験には参加しない「非実験参加者」、一メンバーとしてwet実験を行う「実験参加者」、そしてwet実験全体を統括し、各メンバーに適切な指示を与えながら実験を進める「実験責任者」です。  
   非実験参加者から実験参加者へ、また実験参加者から実験責任者へと立場を変更するためには、それぞれ所定のテストを受け、その役割を担うために必要な知識と能力を備えていることを証明する必要があります。この認定制度の詳細については、「4. Training」のセクションで説明しています。  
   wet実験に参加するメンバーは日によって異なりますが、実験を行う際には、原則として必ず1名以上の実験責任者が立ち会うこととしています。この体制は、実験手順を適切に管理し、wet実験を円滑かつ正確に進めるためだけのものではありません。実験中に事故や機器の不具合をはじめとする安全上の問題が発生した場合に、状況を的確に判断し、必要な対応を迅速に取れるようにすることも重要な目的としています。

   ![experiment supervisor system](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-experiment-supervisor-system.avif =400x)  
   :::c  
   **Fig. 11.4.4.** Experiment supervisor system  
   :::

2. **実験終了報告書**  
   　一日の実験を問題なく終えたことの証明として、私たちは毎日実験終了報告書の記入を行っています。この報告書の内容は4段階に分かれています。  
   **I. 実験日および実験者名の記入**  
   はじめに、実験を実施した日付と、その実験に携わったメンバーの氏名を記録します。これにより、後日何らかの問題が判明した場合でも、当時の状況を確認すべきメンバーを速やかに特定することができます。ここでいう問題は、単に実験結果に関するものだけではありません。実験機器の異常や破損など安全上の問題に加え、試薬やサンプルの取り違え、保存・管理上の不備といった、後になって判明する可能性のある問題も含みます。  
   **II. 使用機器の列挙**  
   当日の実験で使用した機器を全て列挙します。また、実験終了時にはそれらの機器に問題が生じていないかを確認し、問題がなければその旨を記入します。これにより、後日共用機器に問題が発生した際に、直近で私たちがそれを使用していたかどうかを簡単に確認することができます。共用機器を使用するにあたって、誰がいつ機器を使用したかを記録することは非常に重要であり、実験をする際に必ず守らなければならないルールの一つです。実験機器の適切な終了チェックは、自分たちだけではなく、同じ機器を使用する他の実験者たちも、事故の危険から守ることに繋がります。  
   **III. チェックリストの確認**  
   実験で使用した機器や実験机の付近の環境について、問題がないかを最終確認します。この確認は必ず実験責任者が自分で行うことを徹底しています。  
   **IV. 指導者のサイン**  
   上記の記入を終了したら、実験指導者（PIである朝日教授のラボメンバー）に内容を確認いただき、サインをもらいます。このサインをもらってはじめて、その日の実験が問題なく終了したことになります。さらに、サインをいただく際に、翌日の実験予定を簡単に共有し、同伴が必要な機器を使用する際にはこのタイミングでお願いをしておきます。

   :::left  
   <div style="display: flex; justify-content: flex-end; margin: 24px 8px 24px 0;">  
   <iframe src="https://static.igem.wiki/teams/6144/wiki/safety/general-safety-igem-post-experiment-checklist-english-ver.pdf " width="80%" height ="600px"></iframe>  
   </div>  
   :::  
   :::right  
   <div style="display: flex; justify-content: flex-start; margin: 24px 0 24px 8px;">  
   <iframe src="https://static.igem.wiki/teams/6144/wiki/safety/general-safety-igem-post-experiment-checklist-japanase-ver.pdf " width="80%" height="600px"></iframe>  
   </div>  
   :::  
3. **危険試薬のSDS共有**  
   　wet実験で使用する試薬の中には、人体への有害性や引火性などの危険性をもつものが含まれています。これらの試薬を安全に取り扱うため、私たちは使用前に安全データシート（Safety Data Sheet: SDS）を確認し、その内容を実験参加者間で共有しています。共有したSDSは、実験を行うメンバーが必要なときにいつでも参照できる状態で保管しています。SDSを共有する目的は、試薬の危険性を把握することだけではありません。各試薬について、適切な保護具、安全な取扱方法、保管条件、廃棄方法、漏出・曝露時の応急措置を事前に確認し、実際の実験手順に反映させています。特に危険性の高い試薬を初めて使用する場合には、実験責任者の監督の下で取扱方法を確認してから実験を開始します。例えば、2-メルカプトエタノールは、吸入や皮膚接触などによって健康被害を引き起こす可能性があるため、SDSに基づき、適切な保護具を使用して取り扱っています。また、エタノールなどの可燃性試薬については、火気や熱源から遠ざけ、一般の試薬とは区別された所定の保管場所で管理しています。保管時には、試薬名と危険性を明確に表示するとともに、容器の密閉状態や保管場所に異常がないことを定期的に確認しています。使用後の試薬や廃液についても、性質の異なる化学物質を不用意に混合することがないよう、大学および研究室の規則に従って分別・廃棄しています。このように、SDSの共有を出発点として、試薬の使用前確認、適切な取扱い、分離保管、廃棄までを一連の安全管理として実施しています。

## **Waste Disposal**

　私たちの実験で発生する廃棄物は、早稲田大学事務所の設ける基準に従って[^2]、以下のように区分されます。

**P: プラスチック器具など廃棄物（薬品が付着したプラスチック製器具、ゴム・シリコン製器具、手袋・マスク類、ペーパー類）**

* 具体例  
  * 実験で使用したチューブ  
  * 実験で使用したチップ  
  * 薬品の付着した手袋、キムワイプ  
* 注意  
  * 遺伝子組換え生物の付着した廃棄物は、必ずA.C.滅菌後に廃棄されます

**S2: 有機固体（高分子化合物・樹脂など）**

* 具体例  
  * 電気泳動ゲル

**Ⅱ-ｈ: 水分が５％以上含まれる有機廃液（含ハロゲン有機廃液, フェロシアン・フェリシアン化合物および金属を含む廃液を除く）**

* 具体例  
  * 液体培地  
  * 滅菌後の菌液

　これらの廃棄物は、それぞれ専用の容器に廃棄した後で、所定の曜日に研究施設の廃棄場所へ運搬されます。この際、どこの研究室から発生した廃棄物であるか、具体的にどのような廃棄物が含まれているか、などの情報を書類に記入することが義務付けられています。私たちは先進理工学部生命医科学科の朝日研究室の一画をお借りしているため、廃棄物を捨てる際は必ず朝日研究室の学生に同伴いただいています。

# **3. Training and Certification**

私たちのチームでは、メンバーを「非実験参加者」「実験参加者」「実験責任者」の3区分に分け、以下の①〜④を順に通過することで実験参加者・実験責任者へと進む認定制度を設けています。目的は、全員が必要な安全知識を身につけることと、指導・監督できる人材を明確にすることです。

:::c

**Table. 11.4.1** Certification steps for wet-lab participation

:::

| ステップ | 対象 | 内容 | 通過条件 |
| ----- | ----- | ----- | ----- |
| ① Online Seminar | wet実験希望者 | 大学のオンライン遺伝子組換え実験講習会 | 受講完了 |
| ② Participant Certification Test | 実験参加者候補 | チーム内ゼミ＋確認テスト | 全問正解 |
| ③ Training | 実験参加者 | 実験責任者立ち会いの手技トレーニング | 責任者が「一人で実施可」と3回以上判断 |
| ④ Supervisor Certification Test | Training修了者 | 知識問題＋ケーススタディ | 全問正解 |

**① Online Seminar**

大学提供のオンライン講習を受講します（法令、拡散防止措置、安全な作業技術、事故対応、学内管理体制）。修了者のみ次のステップに進めます。

**② Participant Certification Test**  
「安全の手引き（TWIns）」[^3]「環境保全センター利用の手引き」[^2]「標準プロトコル（GP01〜08）」[^4]等をもとに作成した全10章の教材で、法令・拡散防止措置、遺伝子組換えの基礎と実験手順、PPE、基本操作・機器の安全な使い方、試薬・生物材料の管理、廃棄物の分別、リスクアセスメント、事故初動対応を学びます。合格基準は全問正解（100%）です。安全知識に「だいたい理解」で許される範囲はないと考えているためです。不合格の場合は該当範囲を復習し再受験します。

:::left  
<div style="display: flex; justify-content: flex-end; margin: 24px 8px 24px 0;">  
<iframe src="https://static.igem.wiki/teams/6144/wiki/safety/participant-en-forwiki.pdf" width="80%" height="600px"></iframe>  
</div>  
:::  
:::right  
<div style="display: flex; justify-content: flex-start; margin: 24px 0 24px 8px;">  
<iframe src="https://static.igem.wiki/teams/6144/wiki/safety/participant-jp-forwiki.pdf["](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-igem-post-experiment-checklist-japanase-ver.pdf") width="80%" height="600px"></iframe>  
</div>  
:::

**③ Training**  
知識だけでは身につかない操作のコツや危険を、実験責任者立ち会いのもと3段階（見学→補助あり体験→単独実施）で習得します。単独実施への移行は、責任者が「一人で正しくできる」と3回以上判断した時点です。逸脱やミスはその場で指摘し、実施状況はExcelシートで記録・管理します。

**④ Supervisor Certification Test**  
Trainingを修了し、生物・薬品の取り扱いと廃棄方法、SDS、緊急時対応を理解していることが受験条件です。Participant範囲に加え、SDS・GHS、廃棄物最終処分の手続き、Risk Group[^5]・White List[^6]・Red Flag[^7]による安全性評価、デュアルユースへの配慮、指導方法を扱います。ケーススタディには学内の実際のヒヤリハット事例（匿名化済み）を使い、知識だけでなくその場の判断力を測ります。合格基準は同じく全問正解です。

:::left  
<div style="display: flex; justify-content: flex-end; margin: 24px 8px 24px 0;">  
<iframe src="https://static.igem.wiki/teams/6144/wiki/safety/supervisor-en-forwiki.pdf" width="80%" height="600px"></iframe>  
</div>  
:::  
:::right  
<div style="display: flex; justify-content: flex-start; margin: 24px 0 24px 8px;">  
<iframe src="https://static.igem.wiki/teams/6144/wiki/safety/supervisor-jp-forwiki.pdf["](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-igem-post-experiment-checklist-japanase-ver.pdf") width="80%" height="600px"></iframe>  
</div>  
:::

**⑤ Continuing Education**  
認定後も学びを継続しています。2026年3月にはiGEMer向けバイオリスクマネジメントトレーニングや施設の安全講習に参加し、学んだ内容をチーム内で共有しました。


:::c

**Fig.11.4.5.修了証**

:::

## **Web Test Platform**

②④のテストは、自作のWebプラットフォームで実施しています。

**Waseda-Tokyoの作成したサンプルテストを受験する（どなたでも）**  
下記リンクから、名前欄で「その他」を選び受験できます（登録不要、日英切替可）。採点は即時表示され、間違えた問題の解説と分野別正答率が分かります。メンバーの受験結果は管理画面に集計され、責任者は受験状況・合格者一覧・チーム全体の弱点を確認できます。

* [Participant Certification Test]  
* [Supervisor Certification Test]

**自分たちのテストを作る（他チーム向け）**  
安全ルールはラボごとに異なるため、各チームが自分たちのテストを作れる仕組みにしました。①チーム登録→②自ラボの資料・SOPを登録（AI用プロンプトを自動生成）→③好きなAI（ChatGPT/Gemini/Claude等）で問題作成→④サイトに貼り付けて内容確認・公開→⑤受験・進捗管理。

特徴：APIキーをサイトに組み込まないため無料で使える／チームごとにデータを完全分離／言語は自由に追加可能。ソースコードとREADMEはiGEM GitLabで公開しています。

* プラットフォーム：Safety Certification Platform  
* ソースコード：iGEM GitLab

# **4.Risk Assessment**

本プロジェクトの実施にあたり、我々は実験に伴うリスクをPhysical Risk・Chemical Risk・Biological Riskの3つの観点に分類し、それぞれについてハザードを洗い出し、対応する安全対策を講じて実験を進めた。

## **①Physical Risks**

実験操作そのものに伴う物理的ハザードであり、発生頻度は低いものの日常作業で見落とされやすいため、以下の通り明文化して管理した（Table11.4.2）。

:::c

**Table. 11.4.2 Assessments for Physical Risks**

:::

| ハザード | 具体的な場面 | 対策 |
| :---- | :---- | :---- |
| やけど・引火 ![temperature-plus](https://static.igem.wiki/teams/6144/wiki/safety/general-phisical-list-temperature-plus.avif =50x) | サーマルサイクラー使用時、ヒートショック処理、火炎滅菌、オートクレーブ処理、可燃性試薬（グリセロールストック用溶液など）の分注時 | 熱くなった器具を触る際は軍手を着用する。引火性のあるものは火気の近くに置かないようにし、該当箇所には注意喚起シールを掲示。 |
| 遠心機の事故 ![rotate-clockwise]( https://static.igem.wiki/teams/6144/wiki/safety/general-phisical-list-rotate-clockwise.avif =50x) | Miniprep時の卓上遠心機、タンパク質精製時の超遠心機の使用時 | チューブは対称になるようバランスよく配置する。設定回転数に達するまでは機器の異常がないか観察を続ける。超遠心機の使用時は、さらに高重力に耐えられるチューブを用意し、使用するローターとの互換性を確認する。 |
| 鋭利なもの・ガラスによる怪我 ![bandage](https://static.igem.wiki/teams/6144/wiki/safety/general-phisical-list-bandage.avif =50x) | ガラス器具の使用・洗浄時 | 破損したガラスは専用の廃棄容器に廃棄する。使い捨てで使用するチューブやチップなどの器具にはプラスチック製のものを採用しており、ガラス器具そのものの使用機会を減らすことで破損による怪我のリスクを低減している。 |
| 転倒事故 ![fall](https://static.igem.wiki/teams/6144/wiki/safety/general-phisical-list-fall.avif =50x) | 溶液のこぼれ（特に洗い場） | 実験台や洗い場を使用する前後に、床や作業台が濡れていないか各自で確認し、濡れていたら水をふき取る。 |
| 落下物・地震 ![packages](https://static.igem.wiki/teams/6144/wiki/safety/general-phisical-list-packages.avif =50x) | 棚に保管している試薬（特にガラス瓶入りのもの） | 棚の上段にはガラス瓶に入った試薬を置かないようにし、棚の前側にはつっかえ棒を設置することで地震発生時の落下を防止している。また、使用頻度の高い試薬は手が届きやすい最下段に配置し、全体として背の低い試薬を手前側に置くことで、取り出す際の落下事故を防止している（Fig11.4.6）。 |

![The reagents on the shelf in front of the lab bench](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-reagends.avif =500x)

:::c

**Fig. 11.4.6 The reagents on the shelf in front of the lab bench**

:::

## **②Chemical Risks**

試薬の毒性・可燃性・環境負荷に伴うハザードであり、使用する試薬ごとにリスクを評価した上で以下の対策を講じた（Table11.4.3）。

:::c

**Table. 11.4.3 Assessments for Chemical Risks**

:::

| ハザード | 具体的な場面 | 対策 |
| :---- | :---- | :---- |
| 感作性・毒性 ![skull](https://static.igem.wiki/teams/6144/wiki/safety/general-chemical-list-skull.avif =50x) | 抗生物質（一部感作性・発がん性が指摘されているものを含む）、EtBrの取り扱い時 | 手袋を着用し、皮膚への直接接触を避ける。試薬の危険性はSDSで事前に確認する。また、直接皮膚に触れないように気を付ける試薬には黄色の注意喚起シールを貼付している（Fig11.4.7）。 |
| 引火性 ![flame](https://static.igem.wiki/teams/6144/wiki/safety/general-chemical-list-flame.avif =50x) | エタノールおよびエタノールを溶媒とする試薬の取り扱い時 | 火気の近くでの使用を避ける。該当する試薬容器の蓋など見やすい箇所に、ラベルの表示にかからないよう赤色の注意喚起シールを貼付している（Fig11.4.7）。 |
| 腐食性 ![droplets](https://static.igem.wiki/teams/6144/wiki/safety/general-chemical-list-droplets.avif =50x) | Cell Lysis Buffer（NaOHを含む）などの取り扱い時 | 手袋を着用し、皮膚への直接接触を避ける。万が一皮膚や眼に付着した場合は、大量の水で洗浄する。 |
| 環境汚染 ![plant](https://static.igem.wiki/teams/6144/wiki/safety/general-chemical-list-plant.avif =50x) | 廃液の取り扱い時 | シンクへ流さず、指定の化学廃液容器に廃棄し、施設のルールに従う。 |
| 試薬情報・リスクの管理不備 ![vaccine-bottle](https://static.igem.wiki/teams/6144/wiki/safety/general-chemical-list-vaccine-bottle.avif =50x) | 実験室で保有する試薬全般 | 所有する全試薬をExcelで記帳・管理し（Fig11.4.8）、SDSはオンライン上の共有ファイルで一元管理している。また、今年度使用している「試薬に関しては、SDSを印刷し実験室に保管している。使用する試薬のうち、GHS区分を持つもにについては厚生労働省のCREATE-SIMPLE[^8]を用いたリスクアセスメントを実施し、その結果をPDF化して実験室内のファイルおよびオンライン上に保管している。 |

＊CREATE-SIMPLE：厚生労働省が無料で提供している、化学物質のリスクアセスメントを簡単に行うためのExcelツール。使う試薬のSDSに書かれているGHS区分と、実際の使用量・使用時間・作業条件などをフォームに入力すると、そのばく露や火災・爆発のリスクレベルの自動判定ができ、専門知識がなくても労働安全衛生法で義務化されているリスクアセスメントの実施が可能。

![Reagent with a warning sticker](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-stickers.avif =500x)

:::c

**Fig. 11.4.7 Reagent with a warning sticker**

:::

![Reagent management list in Excel](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-list.avif =500x)

:::c

**Fig. 11.4.8 Reagent management list in Excel**

:::

## **③Biological Risks**

生物学的リスクとしては、まず使用するシャーシ生物そのものの安全性を評価した。本プロジェクトでは大腸菌(*Escherichia coli*)のDH5α株、Top10株、BL21(DE3)株の3株のみをシャーシとして使用した。DH5αおよびTop10はK-12系統由来の実験室株であり、いずれもiGEMのRisk Group guidanceにおいてリスクグループ1(健常な成人に疾病を引き起こさない微生物)に分類されている。BL21(DE3)はB系統由来の実験室株であるが、同様に非病原性でありリスクグループ1として扱われる。これら3株はいずれもiGEM White Listに掲載されている標準的な実験室株である。

その上で、組換え菌の環境流出や遺伝子拡散、取り違えといった運用上のリスクについても、以下の対策を講じた（Table11.4.4）。

:::c

**Table. 11.4.4 Assessments for Biological Risks**

:::

| ハザード | 対策 |
| :---- | :---- |
| 組換え菌の環境流出 ![biohazard](https://static.igem.wiki/teams/6144/wiki/safety/general-biological-list-biohazard.avif =50x) | 作業前後に実験台を消毒し、スピル発生時の対応手順を定めた。実験スペースと私物を置くスペースを区画化し、私物は手袋を着用した状態で触らないこととした（Fig11.4.9）。 |
| 遺伝子拡散 ![dna-2](https://static.igem.wiki/teams/6144/wiki/safety/general-biological-list-dna-2.avif =50x) | 生物材料は廃棄前にオートクレーブ処理により完全に不活化した。 |
| 取り違え・管理不 備 ![checkup-list](https://static.igem.wiki/teams/6144/wiki/safety/general-biological-list-checkup-list.avif =50x) | 寒天培地に組換え体を播種したプレート・プラスミド・グリセロールストックについて、それぞれ実験室内のノートで台帳管理を行った（Fig11.4.10）。 |

![Partitioned test bench](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-zoaning.avif=500x)

:::c

**Fig. 11.4.9 Partitioned test bench**

:::

![A ledger for managing biological materials](https://static.igem.wiki/teams/6144/wiki/safety/general-safety-ledger.avif =500x)

:::c

**Fig. 11.4.10 A ledger for managing biological materials**

:::

# **5. Emergency Responses**

実験中の事故では、起きた直後の数分間の行動で被害の大きさが変わります。そこで私たちは、「怪我」「地震」「火災」「環境への流出」の4つに対応する緊急時対応マニュアルを作りました。内容は、活動場所であるTWInsの安全のてびき[^3]と、早稲田大学環境保全センターの手引き[^2]をもとにしています。応急手当や初期消火の方法は、日本赤十字社[^9]や消防機関[^10]などの公的な資料で確認しました。また、菌液をこぼしたときの処理など、私たちの実験内容（BSL-1、大腸菌、液体窒素）に合わせた対応も入れました。

マニュアルは、5枚のYes/Noフローチャートと詳細ページでできています。「はい／いいえ」で答えていくと、誰でも迷わず次の行動にたどり着けます。地震のあとに火災が起きたときなどは、別のフローへ進めるようにつなげてあります。このマニュアルは実験室に掲示し、年に1回と、メンバーが変わったときに見直します。

:::left  
<div style="display: flex; justify-content: flex-end; margin: 24px 8px 24px 0;">  
<iframe src="[https://static.igem.wiki/teams/6144/wiki/safety/emergency-response-en-forwiki.pdf](https://static.igem.wiki/teams/6144/wiki/safety/emergency-response-en-forwiki.pdf)" width="80%" height="600px"></iframe>  
</div>  
:::  
:::right  
<div style="display: flex; justify-content: flex-start; margin: 24px 0 24px 8px;">  
<iframe src="[https://static.igem.wiki/teams/6144/wiki/safety/emergency-response-jp-forwiki.pdf](https://static.igem.wiki/teams/6144/wiki/safety/emergency-response-jp-forwiki.pdf)" width="80%" height="600px"></iframe>  
</div>  
:::

