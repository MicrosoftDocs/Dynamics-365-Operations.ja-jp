---
title: Human Resources - Go Live の準備
description: このページでは、Dynamics 365 Human Resources の準備に関するガイダンスをあつかいます。
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: b40d6ce45aeb07724fc41d1a41923970b007fbcf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2020
ms.locfileid: "4419447"
---
# <a name="prepare-for-human-resources-go-live"></a>Human Resources - Go Live の準備

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Dynamics 365 Human Resources プロジェクトにおける go live の準備方法を説明します。 

この図には、Go-Live プロセスのフェーズが表示しています。 

![Go-live プロセス](./media/hr-admin-go-live-prepare-process.png)

次のテーブルでは、プロセスのすべてのステップと、予定期間と、誰が処理を実行するのかについて示しています。

| フェーズ | アクション | 期間/時 | 誰 | 摘要 |
| --- | --- | --- | --- |--- |
| 1 | LCS での Go-Live 日付の更新 | 遅くとも 2 ～ 3 か月前に | パートナー/顧客 | マイルストーンの日付は、継続的に最新のものにする必要があります。 |
| 2 | チェックリストの完了および送信 | ユーザー受け入れテスト (UAT) が完了した後 | パートナー/顧客 | [FastTrack Go-live アセスメントの](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment)に記載の指示に従います。 |
| 3 | プロジェクト評価 (FastTrack) | FastTrack アーキテクト* | アーキテクトは、チェックリストを受け取った後に評価を提供し、質問が明確化および軽減されるまでレビューを続行します。 |
| 4 | プロジェクト ワークショップ (FastTrack) | FastTrack アーキテクト* | |
| 5 | データ パッケージのインポート | プロジェクトによって異なります | パートナー/顧客 | [データ管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)の指示に従います。|
| 6 | 生産準備完了 | 前の手順すべてが完了した後 | パートナー/顧客 | 顧客/パートナーが引用環境を制御することができます。|
| 7 | 切替活動 | プロジェクトによって異なります | パートナー/顧客 | |
| 8 | Go live | プロジェクトによって異なります | 顧客 | |

> [!IMPORTANT]
> *手順 3 と 手順 4 は、FastTrack の対象顧客に対してのみ実行されます。

## <a name="completing-the-lcs-methodology"></a>LCS メソッドを完了しています

各実装プロジェクトにおける主要なマイルストーンは、実稼働環境への切替です。 

運用環境を確実に本番運用に使用できるようにするために、マイクロソフトでは、LCS の方法論で必要とされる活動が完了した後、実装が **運用** フェーズに近づいている場合にのみ、運用インスタンスをプロビジョニングします。 ご利用のサブスクリプションでの環境の詳細については、 [Dynamics 365 ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544) を参照してください。 

運用環境を要求するための  **構成**  ボタンが利用可能になる前に、LCS 手法で **分析**、**設計と開発**、**テスト**  フェーズを完了しておく必要があります。 LCS でフェーズを完了するには、まずそのフェーズで必要なすべてのステップを完了する必要があります。 フェーズにあるすべてのタスクが完了したら、そのフェーズ全体を完了することができます。 変更する必要がある場合、常に後からフェーズを再オープンすることができます。 詳細については、 [Finance and Operations アプリ 顧客向け Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs) を参照してください。 

ステップを完了するプロセスは 2 つの部分で成り立っています。 

- フィット ギャップ解析またはユーザー受け入れテスト (UAT) など、実際の作業を行います。 
- LCS 方法の対応するステップを完了としてマークします。 

実装の進捗状況に応じて方法のステップを完了することをお勧めします。 最後まで待たないでください。 運用環境を取得できるように、クリックするだけではいけません。 確かな実装が顧客の最高の利益となります。 

## <a name="uat-for-your-solution"></a>ソリューションの UAT

UAT のフェーズでは、実装プロジェクトのサンドボックス環境で、実装したすべてのビジネス プロセスとカスタマイズをテストする必要があります。 実稼働運用を成功させるためには、UAT フェーズを完了する際に次の点を考慮する必要があります。 

- テスト ケースは、要件の範囲全体をカバーします。 
- 移行したデータを使用してテストします。 このデータには、作業者、職務、職位などのマスター データを含める必要があります。 また、休暇および休暇の見越計上と同様に、期首残高も含めます。 最後に、現在の福利厚生の登録など、未処理のトランザクションを含めます。 データセットが確定していない場合でも、すべてのタイプのデータで完全なテストを行うことができます。 
- ユーザーに割り当てられている適切なセキュリティ ロール (既定のロールおよびカスタム ロール) を使用してテストします。 
- ソリューションが会社や業界別の規制要件に準拠していることを確認します。 
- すべての機能を文書化し、顧客の承認とサインオフを取得します。 

## <a name="fasttrack-go-live-assessment"></a>FastTrack Go-live アセスメント

FastTrack の対象となっていて、FastTrack ソリューションアーキテクトと契約しているお客様は、Microsoft FastTrack を使用した Go-live レビューを完了します。 詳細については、  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview) を参照してください。 

Go-Live の約 8 週間前に、FastTrack チームが [Go-Live チェックリスト](https://go.microsoft.com/fwlink/?linkid=2146013)への記入を依頼します。

プロジェクト マネージャーまたはプロジェクトの主要メンバーは、プロジェクトの Go-Live 前の段階の間に Go-Live チェックリストを完了する必要があります。 チェックリストは通常、稼働予定日の 4 ~ 6 週間前に完了し、UAT が完了したか、ほぼ完了したときです。 

Go-Live チェックリスト を完了したら、電子メールで、FastTrack ソリューション アーキテクトに送信します。 電子メールには、顧客からの主な関係者と実装パートナーを必ず含めます。 

チェックリストを提出した後、FastTrack ソリューション アーキテクトがプロジェクトをレビューし、潜在的なリスク、ベスト プラクティス、プロジェクトの運用を成功させるにあたっての推奨事項を記載した評価を提供します。 場合によっては、ソリューション アーキテクトがリスク要因を強調表示し、軽減計画を求める場合があります。 

## <a name="see-also"></a>参照

[Go-Live に関するよく寄せられる質問](hr-admin-go-live-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]