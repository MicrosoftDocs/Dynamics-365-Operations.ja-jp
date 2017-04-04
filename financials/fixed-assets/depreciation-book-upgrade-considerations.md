---
title: "減価償却簿のアップグレードの概要"
description: "以前のリリースでは、固定資産からの二つの評価の概念が-価値モデルおよび減価償却簿に。 Microsoft Dynamics 365 for Operations 1611 のリリースでは、価値モデル機能および減価償却簿機能は帳簿と呼ばれる単一の概念に統合されました。 このトピックでは、アップグレードで考慮すべき点について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>減価償却簿のアップグレードの概要

以前のリリースでは、固定資産からの二つの評価の概念が-価値モデルおよび減価償却簿に。 Microsoft Dynamics 365 for Operations 1611 のリリースでは、価値モデル機能および減価償却簿機能は帳簿と呼ばれる単一の概念に統合されました。 このトピックでは、アップグレードで考慮すべき点について説明します。 

アップグレード プロセスは、既存のセットアップと既存のすべてのトランザクションを新しい帳簿構造に移動します。 価値モデルは、現在のように総勘定元帳に転記する帳簿のままになります。 減価償却簿は、[**総勘定元帳への転記**] オプションが [**いいえ**] に設定されている帳簿に移動されます。 減価償却簿仕訳帳名はに設定された転記階層に総勘定仕訳元帳の名前に移動されます**なし**。 減価償却簿トランザクションは、固定資産トランザクションに移動されます。 

データ アップグレードを実行する前に、トランザクション伝票に減価償却簿の仕訳帳明細行をアップグレードするために使用できる 2 つのオプションと、伝票シリーズに使用される番号順序を理解する必要があります。 

オプション 1: **システムで定義されている番号順序** - これはアップグレード パフォーマンスを最適化する既定のオプションです。 アップグレードは、番号順序フレームワークを使用しませんが、代わりにセット ベースのアプローチによる伝票を割り当てます。 アップグレードが適切にアップグレードされたトランザクションに基づいてと、新しい番号順序**設定される次の数**作成後に。 既定では、使用された番号順序はFADBUpgr\#\#\#\#\#\#\#\#\# 形式にあります。 この方法を使用するとフォームを調整するときに使用できるいくつかのパラメータがあります:

-   **番号順序コード** –番号順序を識別するコード。 この番号順序コードは、アップグレードによって作成されるのですることはできません。
    -   定数名: **NumberSequenceDefaultCode**
    -   既定値: 「FADBUpgr」
-   **接頭語** – 伝票番号の接頭語として使用される定数文字列値。
    -   定数名: **NumberSequenceDefaultParameterPrefix**
    -   既定値: 「FADBUpgr」
-   **英数字の長さ** – 番号順序の英数字区分の長さ。
    -   定数名: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   既定値: 9
-   **開始番号** - 番号順序で使用される最初の番号。
    -   定数名: ** NumberSequenceDefaultParameterStartNumber **
    -   既定値: 1

オプション2: **既存のユーザー定義の番号順序は- **このオプション アップグレードに使用する番号順序を定義することができます。 高度な番号順序コンフィギュレーションが必要な場合はこのオプションを使用することを検討してください。 番号順序を使用するには、次の情報のアップグレードのReleaseUpdateDB70\_クラスFixedAssetJournalDepBookRemovalDepBookJournalTransを変更する必要があります:

-   **番号順序コード** – 番号順序のコード。
    -   定数名: ** NumberSequenceExistingCode **
    -   既定値: 既定値はありません、番号順序コードを更新する必要があります。
-   **共有番号順序** – 番号順序のスコープを識別するブール値。 すべての会社間の共有番号順序には「true」を使用し、企業固有のスコープには「false」を使用します。 「false」使用する減価償却簿トランザクションを含むすべての会社に指定された名前による番号順序いない場合。 共有番号順序に減価償却簿トランザクションを含むすべてのヘッダーに表示されます。
    -   定数名: ** NumberSequenceExistingIsShared **
    -   既定値: 「true」

パラメータはReleaseUpdateDB70 FixedAssetJournalDepBookRemovalDepBookJournalTrans\_クラスの先頭にあります。 

*//既存の番号順序のcode* 
使用 
場合は、false伝票のallocation* 
の必要なアプローチを*//調整し、*//システムで定義されている番号順序 (既定) を使用するために使用する*定数ブールNumberSequenceUseExistingCode = false指定すること;  

*//システムで定義されている番号順序のアプローチを使用する場合は、指定します。番号sequence.*
のパラメータを*//新しい番号順序は、これらのparameters.*に作成されます。 定数のstr NumberSequenceDefaultCode = 「」FADBUpgr; 定数のstr NumberSequenceDefaultParameterPrefix = 「」FADBUpgr; 定数整数NumberSequenceDefaultParameterAlpanumericLength = 9; 定数整数NumberSequenceDefaultParameterStartNumber = 1;   

*//既存の番号順序のアプローチを使用する場合は、指定します。既存の番号順序code.* 
*//伝票の配賦が処理既存の行番号sequences.*の実行 定数のstr NumberSequenceExistingCode = "; *//指定された番号順序がshared* 
false既存の番号順序のcode* 
の範囲を*//調整し、*//指定します。指定された番号順序がper-company* 
*//指定された範囲の番号順序コードをfound.*である既定でシステムで定義されている番号順序が使用されます const boolean NumberSequenceExistingIsShared = true; 

定数が変更された後、クラスを含むプロジェクトを再構築します。 

自動生成された番号順序のアプローチを使用する場合 (1) オプションは、アップグレード アップグレード スクリプト パラメータに指定された伝票番号を割り当てる設定ベースの処理を使用します。 また、配賦後で指定された新しいパラメーターと番号順序を作成します。 

ユーザー定義の既存の番号順序アプローチ (オプション 2) を使用する場合は、データのアップグレードは、指定されたスコープの番号順序が減価償却簿トランザクションを持つ各パーティションおよび会社のデータベースに存在するかどうかをチェックします。 存在する場合)、アップグレードは、番号順序フレームワークを使用して番号順序で指定されるように、伝票番号を割り当てるための処理する行処理を使用します。 番号順序が指定されている範囲にある、アップグレードは伝票番号を割り当てる既定では、システムで定義されている番号順序のアプローチを使用して、選択した既定のパラメータと配賦後に新しい番号順序を作成します。

どちらのアプローチでも、データ アップグレード スクリプトは、以前の減価償却簿仕訳帳名のために作成された新しい総勘定元帳仕訳帳名の [**伝票シリーズ**] フィールドのために番号順序を使用します。


