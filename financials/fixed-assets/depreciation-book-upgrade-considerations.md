---
title: "減価償却簿のアップグレードの概要"
description: "以前のリリースでは、固定資産には 2 つの評価概念がありました - 価値モデルおよび減価償却簿。 Microsoft Dynamics 365 for Operations 1611 のリリースでは、価値モデル機能および減価償却簿機能は帳簿と呼ばれる単一の概念に統合されました。 このトピックでは、アップグレードで考慮すべき点について説明します。"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2543032fe479e56586772f345f5aacb0bb8ca1d1
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="depreciation-book-upgrade-overview"></a>減価償却簿のアップグレードの概要

[!include[banner](../includes/banner.md)]


以前のリリースでは、固定資産には 2 つの評価概念がありました - 価値モデルおよび減価償却簿。 Microsoft Dynamics 365 for Operations 1611 のリリースでは、価値モデル機能および減価償却簿機能は帳簿と呼ばれる単一の概念に統合されました。 このトピックでは、アップグレードで考慮すべき点について説明します。 

アップグレード プロセスは、既存のセットアップと既存のすべてのトランザクションを新しい帳簿構造に移動します。 価値モデルは、現在のように総勘定元帳に転記する帳簿のままになります。 減価償却簿は、[**総勘定元帳への転記**] オプションが [**いいえ**] に設定されている帳簿に移動されます。 減価償却簿の仕訳帳名は、[**なし**] に設定されている転記階層の総勘定元帳の仕訳帳名に移動されます。 減価償却簿トランザクションは、固定資産トランザクションに移動します。 

データ アップグレードを実行する前に、トランザクション伝票に減価償却簿の仕訳帳明細行をアップグレードするために使用できる 2 つのオプションと、伝票シリーズに使用される番号順序を理解する必要があります。 

オプション 1: **システムで定義されている番号順序** - これはアップグレード パフォーマンスを最適化する既定のオプションです。 アップグレードは、番号順序フレームワークを使用しませんが、代わりにセット ベースのアプローチによる伝票を割り当てます。 アップグレード後、新しい番号順序は、適切にアップグレードしたトランザクションに基づいて**次の番号セット**が作成されます。 既定では、使用される番号順序は、FADBUpgr\#\#\#\#\#\#\#\#\# 形式です。 この方法を使用するとき、形式を調整するために使用可能ないくつかのパラメーターがあります:

-   **番号順序コード** – 番号順序を識別するコード。 この番号順序コードは、アップグレードによって作成されるため存在できません。
    -   定数名: **NumberSequenceDefaultCode**
    -   既定値: 「FADBUpgr」
-   **接頭語** – 伝票番号の接頭語として使用される定数文字列値。
    -   定数名: **NumberSequenceDefaultParameterPrefix**
    -   既定値: 「FADBUpgr」
-   **英数字の長さ** – 番号順序の英数字区分の長さ。
    -   定数名: **NumberSequenceDefaultParameterAlpanumericLength **
    -   既定値: 9
-   **開始番号** - 番号順序で使用される最初の番号。
    -   定数名: **NumberSequenceDefaultParameterStartNumber **
    -   既定値: 1

オプション 2: **既存のユーザー定義の番号順序** - このオプションは、アップグレードに使用する番号順序を定義できます。 高度な番号順序のコンフィギュレーションが必要な場合はこのオプションの使用を検討してください。 番号順序を使用するには、アップグレード クラス「ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans」を次の情報で変更する必要があります:

-   **番号順序コード** – 番号順序のコード。
    -   定数名: **NumberSequenceExistingCode **
    -   既定値: 既定値はありません、番号順序コードを更新する必要があります。
-   **共有番号順序** – 番号順序のスコープを識別するブール値。 すべての会社間の共有番号順序には「true」を使用し、企業固有のスコープには「false」を使用します。 「false」を使用する場合、指定された名前の番号順序が、減価償却簿トランザクションを含むすべての会社に存在する必要があります。 減価償却簿トランザクションを含むすべてのパーティションには、共有番号順序が存在します。
    -   定数名: **NumberSequenceExistingIsShared **
    -   既定値: 「true」

パラメーターは、「ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans」クラスの先頭にあります。 

*// 伝票配賦の好ましいアプローチを指定* 
*// 「true」、既存の番号順序コードを使用する場合* 
*// 「false」、システムで定義されている番号順序 (既定) を使用する場合* const boolean NumberSequenceUseExistingCode = false;  

*// システム定義された番号順序のアプローチを使用する場合は、番号順序のパラメーターを指定します。*
*// 新しい番号順序は、これらのパラメーターで作成されます。* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// 既存の番号順序アプローチを使用する場合は、既存の番号順序コードを指定します。* 
*// 伝票の配賦は、既存の番号順序のために行ごとに移動します。* const str NumberSequenceExistingCode = ''; *// 既存の番号順序コードのスコープを指定* 
*// 「true」、指定された番号順序が共有されている場合* 
*// 「false」、指定された番号順序が会社単位である場合* 
*// 指定されたスコープの番号順序コードが見つからない場合は、既定のシステム定義の番号順序が使用されます。* const boolean NumberSequenceExistingIsShared = true; 

定数が変更された後、クラスを含むプロジェクトを再構築します。 

システム生成の番号順序アプローチ (オプション 1) を使用する場合、アップグレードは、アップグレード スクリプト パラメーターで指定された伝票番号を割り当てるためにセット ベースの処理が使用されます。 また、割り当て後に指定されたパラメーターで新しい番号順序を作成します。 

ユーザー定義の既存の番号順序アプローチ (オプション 2) を使用する場合は、データのアップグレードは、指定されたスコープの番号順序が減価償却簿トランザクションを持つ各パーティションおよび会社のデータベースに存在するかどうかをチェックします。 それが存在する場合、アップグレードは行単位の処理を使用して番号順序のフレームワークを使用し番号順序で指定される伝票番号を割り当てます。 指定したスコープで番号順序が存在しない場合、アップグレードは伝票番号を割り当てるために既定のシステムで定義された番号順序アプローチを使用し、割り当て後に指定した既定のパラメーターで新しい番号順序を作成します。

どちらのアプローチでも、データ アップグレード スクリプトは、以前の減価償却簿仕訳帳名のために作成された新しい総勘定元帳仕訳帳名の [**伝票シリーズ**] フィールドのために番号順序を使用します。




